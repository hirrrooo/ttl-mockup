<script lang="ts">
  import type { Snippet } from 'svelte';
  let { children }: { children?: Snippet } = $props();
</script>

<main class="flex-1 p-8 md:p-16 lg:p-24">
  <div class="max-w-4xl mx-auto space-y-24">
    {@render children?.()}
  </div>
</main>
