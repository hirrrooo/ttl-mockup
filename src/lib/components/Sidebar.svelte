<script lang="ts">
  import type { Snippet } from 'svelte';
  let { children }: { children?: Snippet } = $props();
</script>

<aside class="w-full md:w-80 lg:w-96 bg-paper border-r border-khaki-beige/30 md:h-screen md:sticky top-0 overflow-y-auto p-8 flex flex-col gap-12 shadow-[4px_0_24px_rgba(0,0,0,0.02)]">
  <div class="logo-container">
    <img src="/logo.png" alt="Take The Lead Logo" class="w-48 h-auto mb-4 drop-shadow-sm" />
    <p class="text-sm text-saddle-brown font-sans font-semibold tracking-widest uppercase">Brand Guidelines</p>
  </div>
  
  {@render children?.()}
</aside>
