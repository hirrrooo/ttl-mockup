<script lang="ts">
  import type { Snippet } from 'svelte';
  
  let { 
    variant = 'primary', 
    disabled = false,
    children
  }: {
    variant?: 'primary' | 'secondary';
    disabled?: boolean;
    children?: Snippet;
  } = $props();
  
  const baseClasses = "px-6 py-2.5 rounded font-sans font-bold transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-parchment shadow-sm active:shadow-none active:translate-y-px";
  
  const variants = {
    primary: "bg-saddle-brown hover:bg-dark-walnut text-white focus:ring-saddle-brown",
    secondary: "bg-paper border-2 border-dusty-olive text-charcoal-brown hover:bg-dusty-olive hover:text-white focus:ring-dusty-olive",
  };
  
  const disabledClasses = "opacity-50 cursor-not-allowed bg-khaki-beige text-white hover:bg-khaki-beige shadow-none active:translate-y-0";
</script>

<button 
  class="{baseClasses} {disabled ? disabledClasses : variants[variant]}"
  {disabled}
>
  {@render children?.()}
</button>
