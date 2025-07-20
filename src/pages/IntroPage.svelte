<script>
  import NavBar from "../components/NavBar.svelte";
  import StartButton from "../components/StartButton.svelte";
  import { fade } from 'svelte/transition';
  export let fadeDuration = 400;
  
  export let onStart = () => {};
</script>

<div class="intro-wrapper" in:fade={{ duration: fadeDuration }} out:fade={{ duration: fadeDuration }}>
  <img class="intro-bg" src="/public/LandingPage/intro.gif" alt="Intro GIF"/>
  <div class="intro-content">
    <NavBar />
    <StartButton onStart={onStart} left="62%" top="75%" />
  </div>
</div>


<style>
  .intro-wrapper {
    width: 100vw;
    height: 100vh;
    background-color: black;  /* black bars */
    display: flex;
    justify-content: center;  /* center horizontally */
    align-items: center; 
  }

  .intro-bg {
    position: absolute; 
    top: 0; 
    left: 0; 
    width: 100vw; 
    height: 100vh; 
    object-fit: contain; 
    background: rgba(253,201,122,255); 
    z-index: 0;
  }

  .intro-content {
    max-width: 100%;
    max-height: 100%;
    object-fit: contain; 
  }

  .scene-wrapper {
    width: 100vw;
    height: 100vh;
    background-color: black;  /* black bars */
    display: flex;
    justify-content: center;  /* center horizontally */
    align-items: center;      /* center vertically */
  }

  .scene-image {
    max-width: 100%;
    max-height: 100%;
    object-fit: contain;      /* scale image inside container without cropping */
  }
</style>
