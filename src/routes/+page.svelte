<script lang="ts">
  import Sidebar from '$lib/components/Sidebar.svelte';
  import MainContent from '$lib/components/MainContent.svelte';
  import ColorSwatch from '$lib/components/ColorSwatch.svelte';
  import TypographyScale from '$lib/components/TypographyScale.svelte';
  import Button from '$lib/components/ui/Button.svelte';
  import Input from '$lib/components/ui/Input.svelte';
  import Card from '$lib/components/ui/Card.svelte';
  import MockNavbar from '$lib/components/ui/MockNavbar.svelte';
</script>

<div class="flex flex-col md:flex-row min-h-screen">
  <Sidebar>
    <section>
      <h3 class="text-sm font-sans font-bold uppercase tracking-wider text-dusty-olive mb-4 border-b border-khaki-beige/30 pb-2">Color Palette</h3>
      
      <div class="space-y-4">
        <h4 class="font-sans text-xs font-semibold text-camel uppercase">Primary Browns</h4>
        <ColorSwatch name="Dark Walnut" hex="#582f0e" class="bg-dark-walnut" />
        <ColorSwatch name="Saddle Brown" hex="#7f4f24" class="bg-saddle-brown" />
        <ColorSwatch name="Toffee Brown" hex="#936639" class="bg-toffee-brown" />
        
        <h4 class="font-sans text-xs font-semibold text-camel uppercase mt-6">Accents</h4>
        <ColorSwatch name="Dry Sage" hex="#a4ac86" class="bg-dry-sage" />
        <ColorSwatch name="Dusty Olive" hex="#656d4a" class="bg-dusty-olive" />
        <ColorSwatch name="Khaki Beige" hex="#b6ad90" class="bg-khaki-beige" />
      </div>
    </section>

    <section>
      <h3 class="text-sm font-sans font-bold uppercase tracking-wider text-dusty-olive mb-4 border-b border-khaki-beige/30 pb-2 mt-8">Typography</h3>
      <TypographyScale />
    </section>
  </Sidebar>
  
  <MainContent>
    <section>
      <h2 class="text-4xl text-dark-walnut mb-2">Usage Examples</h2>
      <p class="text-dusty-olive text-lg mb-12">How the brand identity translates into practical UI components.</p>
      
      <div class="space-y-16">
        
        <!-- Buttons Section -->
        <div>
          <h3 class="text-xl text-saddle-brown font-sans font-bold border-b border-khaki-beige/40 pb-2 mb-6">Interactive Elements</h3>
          <div class="bg-white p-8 rounded-lg shadow-sm border border-paper flex flex-wrap gap-6 items-end">
            <div class="flex flex-col gap-2">
              <span class="font-mono text-xs text-khaki-beige">Primary</span>
              <Button variant="primary">Take Action</Button>
            </div>
            <div class="flex flex-col gap-2">
              <span class="font-mono text-xs text-khaki-beige">Secondary</span>
              <Button variant="secondary">Learn More</Button>
            </div>
            <div class="flex flex-col gap-2">
              <span class="font-mono text-xs text-khaki-beige">Disabled</span>
              <Button disabled>Not Available</Button>
            </div>
          </div>
        </div>

        <!-- Forms Section -->
        <div>
          <h3 class="text-xl text-saddle-brown font-sans font-bold border-b border-khaki-beige/40 pb-2 mb-6">Form Fields</h3>
          <div class="bg-white p-8 rounded-lg shadow-sm border border-paper max-w-md space-y-4">
            <Input id="name" label="Full Name" placeholder="Jane Doe" />
            <Input id="email" label="Email Address" placeholder="jane@example.com" />
            <div class="pt-2">
              <Button variant="primary">Submit Request</Button>
            </div>
          </div>
        </div>

        <!-- Cards Section -->
        <div>
          <h3 class="text-xl text-saddle-brown font-sans font-bold border-b border-khaki-beige/40 pb-2 mb-6">Content Cards</h3>
          <div class="bg-paper/50 p-8 rounded-lg border border-khaki-beige/20 grid grid-cols-1 md:grid-cols-2 gap-6">
            <Card title="Training Basics">
              Establishing a strong foundation of trust and respect with your dog begins with consistent positive reinforcement.
            </Card>
            <Card title="Nutrition Guide">
              Understanding what fuels your dog's energy and maintains their health is crucial for a long, happy life together.
            </Card>
          </div>
        </div>

        <!-- Navigation Section -->
        <div>
          <h3 class="text-xl text-saddle-brown font-sans font-bold border-b border-khaki-beige/40 pb-2 mb-6">Page Navigation</h3>
          <div class="bg-paper/30 p-8 rounded-lg border border-khaki-beige/20 relative shadow-inner">
             <div class="shadow-lg rounded-lg overflow-hidden border border-black/5">
                <MockNavbar />
                <div class="bg-parchment h-32 p-6 flex items-center justify-center text-khaki-beige font-sans italic">
                   Page Content Area
                </div>
             </div>
          </div>
        </div>

      </div>
    </section>
  </MainContent>
</div>