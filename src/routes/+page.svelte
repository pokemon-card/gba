<script lang="ts">
    import mainLogo from "$lib/images/GBA_3_main.png";
    let hovered = false;

    //include all old titles here, maybe change occasionally?
    let titles = [
        "Svelte??? What's this...",
        "Guess who's back, back again?",
        "Welcome back!",
        "I see you...",
        "Ready to play?",
        "Let's go!",
        "You're back!",
        "42",
        "Cattn here!",
        "Time to play!",
        "Best GBA Emulator!",
        "Best NES Emulator!",
        "Best SNES Emulator!",
        "Best N64 Emulator!",
        "Best DS Emulator!",
        "Wii when!?!??!?"
    ];
    
    import { Button } from "$lib/components/ui/button";
    import { base } from '$app/paths';
  </script>
<svelte:head>
  <title>GBA2.0</title> 
</svelte:head>
  <div class="flex align-center justify-center mt-44">
    <img
      src={mainLogo}
      alt="Gray by Drew Beamer"
      class="h-1/4 w-1/4 rounded-md object-cover"
      class:hovered
      on:mouseenter={() => {
          hovered = true;
      }}
      on:mouseleave={() => {
          hovered = false;
      }}
    />
  </div>

  <h1 class="scroll-m-20 text-3xl font-bold tracking-tight lg:text-3xl mt-4 text-center italic">
    Ready To Play?
  </h1>

    <div class="flex justify-center mt-6">
    <div class="flex gap-2">
        <Button href="{base}/library">Add a Library</Button>
        <Button variant="secondary" href="{base}/singleplayer">Play!</Button>
    </div> 
    </div>
    <div class="flex justify-center mt-2">
    <h1>This is the </h1> <Button class=" pl-1 pr-0 pt-0 pb-0 m-0 h-auto" variant="link" href="https://pokemon-card.github.io/blank/">library (Copy the link).</Button>
    </div>
  <style>
    .hovered {
      filter: brightness(1.4);
      transition: 0.5s ease;
    }
  </style>
