<script lang="ts">
import { cn } from "$lib/utils";
import { Calendar as CalendarPrimitive } from "bits-ui";

type $$Props = CalendarPrimitive.HeaderProps;

let className: $$Props["class"] = undefined;
export { className as class };
</script>

<CalendarPrimitive.Header
	class={cn("relative flex w-full items-center justify-between pt-1", className)}
	{...$$restProps}
>
	<slot />
</CalendarPrimitive.Header>
