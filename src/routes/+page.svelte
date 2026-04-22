<script lang="ts">
  import Sidebar from '$lib/components/Sidebar.svelte';
  import MainContent from '$lib/components/MainContent.svelte';
  import ColorSwatch from '$lib/components/ColorSwatch.svelte';
  import TypographyScale from '$lib/components/TypographyScale.svelte';
</script>

<div class="flex flex-col md:flex-row min-h-screen">
  <Sidebar>
    <section>
      <h3 class="text-sm font-sans font-bold uppercase tracking-wider text-dusty-olive mb-4 border-b border-khaki-beige/30 pb-2">Color Palette</h3>
      
      <div class="space-y-4">
        <h4 class="font-sans text-xs font-semibold text-camel uppercase">Primary Browns</h4>
        <ColorSwatch name="Dark Walnut" hex="#582f0e" className="bg-dark-walnut" />
        <ColorSwatch name="Saddle Brown" hex="#7f4f24" className="bg-saddle-brown" />
        <ColorSwatch name="Toffee Brown" hex="#936639" className="bg-toffee-brown" />
        
        <h4 class="font-sans text-xs font-semibold text-camel uppercase mt-6">Accents</h4>
        <ColorSwatch name="Dry Sage" hex="#a4ac86" className="bg-dry-sage" />
        <ColorSwatch name="Dusty Olive" hex="#656d4a" className="bg-dusty-olive" />
        <ColorSwatch name="Khaki Beige" hex="#b6ad90" className="bg-khaki-beige" />
      </div>
    </section>

    <section>
      <h3 class="text-sm font-sans font-bold uppercase tracking-wider text-dusty-olive mb-4 border-b border-khaki-beige/30 pb-2 mt-8">Typography</h3>
      <TypographyScale />
    </section>
  </Sidebar>
  
  <MainContent>
    <!-- Usage Examples will go here -->
  </MainContent>
</div>