<script lang="ts">
  import type { HTMLInputAttributes } from 'svelte/elements';

  interface Props extends HTMLInputAttributes {
    label?: string;
    id?: string;
  }
  
  let { 
    label = '', 
    id = '',
    value = $bindable(50),
    min = 5,
    max = 500,
    step = 5,
    ...rest 
  }: Props = $props();
</script>

<div class="flex flex-col gap-2">
  {#if label}
    <div class="flex justify-between items-end">
      <label for={id || 'amount-slider'} class="font-sans font-semibold text-sm text-saddle-brown">{label}</label>
      <span class="font-sans font-bold text-dark-walnut text-lg">${value}</span>
    </div>
  {/if}
  <input 
    type="range"
    id={id || 'amount-slider'} 
    {min}
    {max}
    {step}
    bind:value
    {...rest}
    class="w-full h-2 bg-khaki-beige/50 rounded-lg appearance-none cursor-pointer accent-saddle-brown" 
  />
  <div class="flex justify-between font-mono text-[10px] text-dusty-olive mt-1">
    <span>${min}</span>
    <span>${max}</span>
  </div>
</div>
