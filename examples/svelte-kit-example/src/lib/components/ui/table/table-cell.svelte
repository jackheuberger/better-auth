<script lang="ts">
import { cn } from "$lib/utils";
import type { HTMLTdAttributes } from "svelte/elements";

type $$Props = HTMLTdAttributes;

let className: $$Props["class"] = undefined;
export { className as class };
</script>

<td
	class={cn(
		"p-2 align-middle [&:has([role=checkbox])]:pr-0 [&>[role=checkbox]]:translate-y-[2px]",
		className
	)}
	{...$$restProps}
	on:click
	on:keydown
>
	<slot />
</td>
