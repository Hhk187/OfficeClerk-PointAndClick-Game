<script>
    import { fade } from 'svelte/transition';
    export let fadeDuration = 400;

  export let src = '';
  export let alt = 'Scene Image';
</script>

<style>
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

<div class="scene-wrapper" in:fade={{ duration: fadeDuration }} out:fade={{ duration: fadeDuration }}>
  <img class="scene-image" {src} {alt} />
</div>