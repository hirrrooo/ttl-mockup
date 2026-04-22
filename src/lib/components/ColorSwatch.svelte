<script lang="ts">
  let { name = '', hex = '', className = '' } = $props();
</script>

<div class="flex items-center gap-3">
  <div class="w-10 h-10 rounded-md shadow-inner border border-black/5 {className}"></div>
  <div class="flex flex-col">
    <span class="font-sans font-semibold text-sm capitalize">{name.replace('_', ' ')}</span>
    <span class="font-mono text-xs text-dusty-olive uppercase">{hex}</span>
  </div>
</div>