<script lang="ts">
  import type { HTMLAttributes } from 'svelte/elements'
  import { cn } from '../utils'
  type $$Props = HTMLAttributes<HTMLTableSectionElement>

  let className: $$Props['class'] = undefined
  export { className as class }
</script>

<!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
<thead
  class={cn('[&_tr]:border-b bg-neutral-50 border-t border-neutral-200', className)}
  {...$$restProps}
  on:click
  on:keydown
>
  <slot />
</thead>
