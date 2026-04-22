<script lang="ts">
  import type { Snippet } from 'svelte';
  
  let { title = '', children }: { title?: string, children?: Snippet } = $props();
</script>

<div class="bg-white rounded-xl shadow-md border border-paper overflow-hidden transition-transform hover:-translate-y-1 duration-300">
  <div class="h-32 bg-khaki-beige/20 border-b border-paper flex items-center justify-center text-dusty-olive font-sans">
    Image Placeholder
  </div>
  <div class="p-6">
    <h4 class="text-lg font-sans font-bold text-dark-walnut mb-2">{title}</h4>
    <p class="text-sm text-charcoal-brown/80 mb-4 line-clamp-3">
      {@render children?.()}
    </p>
    <a href="#" class="font-sans font-semibold text-saddle-brown text-sm hover:text-dark-walnut flex items-center gap-1">
      Read Article &rarr;
    </a>>
  </div>
</div>
