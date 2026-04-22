<script lang="ts">
  let { 
    label = '', 
    placeholder = '', 
    id = '' 
  } = $props();
</script>

<div class="flex flex-col gap-1.5">
  {#if label}
    <label for={id} class="font-sans font-semibold text-sm text-saddle-brown">{label}</label>
  {/if}
  <input 
    {id} 
    {placeholder}
    class="px-4 py-2 bg-white border border-khaki-beige rounded font-serif text-charcoal-brown focus:outline-none focus:ring-2 focus:ring-dusty-olive focus:border-dusty-olive transition-colors placeholder:text-khaki-beige shadow-inner" 
  />
</div>
