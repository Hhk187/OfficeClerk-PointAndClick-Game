<script>
  import IntroPage from './pages/IntroPage.svelte';
  import VideoScene from './pages/VideoScene.svelte';
  import ImageScene from './pages/ImageScene.svelte';
  let fadeDuration = 400;

  let started = false;
  let videoEnded = false;
  
</script>


{#if !started}
  <IntroPage onStart={() => {started = true}} />
{:else if !videoEnded}
  <VideoScene onEnded={() => {videoEnded = true}} />
{:else if videoEnded}
  <ImageScene src="public/Chapters/chapter1/chap1_begins.png" alt="Scene 1" />
{/if}