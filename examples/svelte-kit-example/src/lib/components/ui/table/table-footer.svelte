<script lang="ts">
import { cn } from "$lib/utils";
import type { HTMLAttributes } from "svelte/elements";

type $$Props = HTMLAttributes<HTMLTableSectionElement>;

let className: $$Props["class"] = undefined;
export { className as class };
</script>

<tfoot class={cn("bg-primary text-primary-foreground font-medium", className)} {...$$restProps}>
	<slot />
</tfoot>
