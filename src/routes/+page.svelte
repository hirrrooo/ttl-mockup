<script lang="ts">
  import ColorSwatch from '$lib/components/ColorSwatch.svelte';
  import TypographyScale from '$lib/components/TypographyScale.svelte';
  import Button from '$lib/components/ui/Button.svelte';
  import Input from '$lib/components/ui/Input.svelte';
  import Card from '$lib/components/ui/Card.svelte';
  import MockNavbar from '$lib/components/ui/MockNavbar.svelte';
  import Slider from '$lib/components/ui/Slider.svelte';
  
  let donationAmount = $state(50);
</script>

<div class="min-h-screen bg-parchment pb-24">
  
  <!-- Header / Hero -->
  <header class="bg-paper py-16 border-b border-khaki-beige/30 mb-16 px-6 text-center">
    <div class="max-w-4xl mx-auto flex flex-col items-center gap-6">
      <img src="/logo.png" alt="Take The Lead Logo" class="h-24 w-auto drop-shadow-md" />
      <div>
        <h1 class="text-3xl md:text-4xl font-sans font-bold text-dark-walnut tracking-widest uppercase mb-2">Brand Guidelines</h1>
        <p class="text-dusty-olive font-mono text-sm uppercase tracking-widest">Take The Lead - Pet Fundraising</p>
      </div>
    </div>
  </header>

  <!-- Main Content Container -->
  <main class="max-w-4xl mx-auto px-6 space-y-24">
    
    <!-- Core Identity -->
    <section class="space-y-12">
      <h2 class="text-3xl text-dark-walnut border-b-2 border-saddle-brown inline-block pb-2">Core Identity</h2>
      
      <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
        <!-- Colors -->
        <div>
          <h3 class="text-sm font-sans font-bold uppercase tracking-wider text-dusty-olive mb-6 border-b border-khaki-beige/30 pb-2">Color Palette</h3>
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
        </div>

        <!-- Typography -->
        <div>
          <h3 class="text-sm font-sans font-bold uppercase tracking-wider text-dusty-olive mb-6 border-b border-khaki-beige/30 pb-2">Typography</h3>
          <TypographyScale />
        </div>
      </div>
    </section>

    <!-- Component Usage -->
    <section class="space-y-12">
      <h2 class="text-3xl text-dark-walnut border-b-2 border-saddle-brown inline-block pb-2">UI Components</h2>
      
      <div class="space-y-16">
        <!-- Buttons -->
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

        <!-- Forms -->
        <div id="forms-section">
          <h3 class="text-xl text-saddle-brown font-sans font-bold border-b border-khaki-beige/40 pb-2 mb-6">Donation Form</h3>
          <div class="bg-white p-8 rounded-lg shadow-sm border border-paper grid grid-cols-1 md:grid-cols-2 gap-8 items-start">
            <div class="space-y-4">
               <Input id="name" label="Full Name" placeholder="Jane Doe" />
               <Input id="email" label="Email Address" placeholder="jane@example.com" />
            </div>
            
            <div class="space-y-6">
              <div class="pt-2">
                 <Slider label="Donation Amount" bind:value={donationAmount} min={10} max={1000} step={10} />
              </div>

              <div class="pt-4">
                <Button variant="primary" class="w-full">Donate ${donationAmount}</Button>
              </div>
            </div>
          </div>
        </div>

        <!-- Cards -->
        <div>
          <h3 class="text-xl text-saddle-brown font-sans font-bold border-b border-khaki-beige/40 pb-2 mb-6">Campaign Cards</h3>
          <div class="bg-paper/50 p-8 rounded-lg border border-khaki-beige/20 grid grid-cols-1 md:grid-cols-2 gap-6">
            <Card title="Help Buster Walk Again">
              Buster is a 4-year-old Golden Retriever who needs emergency spinal surgery after an accident. Help us cover his medical bills.
            </Card>
            <Card title="Emergency Surgery for Luna">
              Luna swallowed a toy and needs immediate surgery to remove the blockage. Any contribution helps our little fighter.
            </Card>
          </div>
        </div>

        <!-- Navbar -->
        <div>
          <h3 class="text-xl text-saddle-brown font-sans font-bold border-b border-khaki-beige/40 pb-2 mb-6">Navigation</h3>
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

  </main>
</div>