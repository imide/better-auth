<script lang="ts">
import { Command as CommandPrimitive } from "cmdk-sv";
import { cn } from "$lib/utils";

type $$Props = CommandPrimitive.ItemProps & {
	class?: string | null | undefined;
};

export let asChild = false;

let className: string | undefined | null = undefined;
export { className as class };
</script>

<CommandPrimitive.Item
	{asChild}
	class={cn(
		"aria-selected:bg-accent aria-selected:text-accent-foreground relative flex cursor-default select-none items-center rounded-sm px-2 py-1.5 text-sm outline-none data-[disabled]:pointer-events-none data-[disabled]:opacity-50",
		className
	)}
	{...$$restProps}
	let:action
	let:attrs
>
	<slot {action} {attrs} />
</CommandPrimitive.Item>
