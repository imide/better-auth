<script lang="ts">
import { Toggle as TogglePrimitive } from "bits-ui";
import { toggleVariants, type Size, type Variant } from "./index.js";
import { cn } from "$lib/utils";

type $$Props = TogglePrimitive.Props & {
	variant?: Variant;
	size?: Size;
};
type $$Events = TogglePrimitive.Events;

let className: any = undefined;
export let variant: $$Props["variant"] = "default";
export let size: $$Props["size"] = "default";
export let pressed: $$Props["pressed"] = undefined;
export { className as class };
</script>

<TogglePrimitive.Root
	bind:pressed
	class={cn(toggleVariants({ variant, size, className }))}
	{...$$restProps}
	on:click
	on:keydown
>
	<slot />
</TogglePrimitive.Root>
