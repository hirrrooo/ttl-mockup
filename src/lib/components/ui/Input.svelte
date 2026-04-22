<script lang="ts">
  import type { HTMLInputAttributes } from 'svelte/elements';
  
  interface Props extends HTMLInputAttributes {
    label?: string;
  }

  let { 
    label = '', 
    id = '',
    value = $bindable(''),
    class: className = '',
    ...rest 
  }: Props = $props();

  const fallbackId = 'input-' + Math.random().toString(36).substring(2, 9);
  const inputId = $derived(id || fallbackId);
</script>

<div class="flex flex-col gap-1.5 {className}">
  {#if label}
    <label for={inputId} class="font-sans font-semibold text-sm text-saddle-brown">{label}</label>
  {/if}
  <input 
    id={inputId}
    bind:value
    class="px-4 py-2 bg-white border border-khaki-beige rounded font-serif text-charcoal-brown focus:outline-none focus:ring-2 focus:ring-dusty-olive focus:border-dusty-olive transition-colors placeholder:text-khaki-beige shadow-inner" 
    {...rest}
  />
</div>
