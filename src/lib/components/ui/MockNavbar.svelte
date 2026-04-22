<script lang="ts">
  import { base } from '$app/paths';
</script>

<div class="bg-white border-b border-paper px-6 py-4 flex items-center justify-between rounded-t-lg">
  <div class="flex items-center gap-2">
    <img src="{base}/logo.png" alt="Take The Lead Home" class="h-8 w-auto" />
    <span class="font-sans font-bold text-dark-walnut hidden sm:inline">Take The Lead</span>
  </div>
  <nav class="hidden md:flex gap-6 font-sans text-sm font-semibold text-charcoal-brown">
    <a href="#" class="hover:text-saddle-brown">Fundraisers</a>
    <a href="#" class="hover:text-saddle-brown">Start a Campaign</a>
    <a href="#" class="hover:text-saddle-brown">Guides</a>
    <a href="#" class="text-saddle-brown border-b-2 border-saddle-brown pb-1">Contact</a>
  </nav>
  <button class="bg-saddle-brown text-white px-4 py-1.5 rounded text-sm font-sans font-bold hover:bg-dark-walnut transition-colors">
    Sign In
  </button>
</div>
