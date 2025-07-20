<script>
  import { onMount } from 'svelte';
  import { fade } from 'svelte/transition';

  export let fadeDuration = 400;
  export let onEnded = () => {};
  /**
     * @type {HTMLVideoElement}
     */
  let videoRef;

  onMount(() => {
    videoRef.currentTime = 0;
    videoRef.play();
  });
</script>
<video
  bind:this={videoRef}
  src="/public/Chapters/intro/intro.mp4"
  preload="auto"
  playsinline
  muted
  on:canplay={() => videoRef && videoRef.play()}
  on:ended={onEnded}
  style="position: absolute; 
  top: 0; 
  left: 0; 
  width: 100vw; 
  height: 100vh; 
  object-fit: contain; 
  background: black; 
  z-index: 0;"
  in:fade={{ duration: fadeDuration }} out:fade={{ duration: fadeDuration }}
></video>


<style>
  .overlay {
    position: absolute;
    top: 60%;
    left: 50%;
    transform: translate(-50%, -50%);
    display: flex;
    flex-direction: column;
    gap: 10px;
    background: rgba(0, 0, 0, 0.7);
    padding: 16px;
    border-radius: 8px;
    color: white;
    font-size: 18px;
    text-align: center;
  }

  button {
    padding: 10px 20px;
    font-size: 18px;
    cursor: pointer;
  }
</style>
