<script lang="ts">
  let logo = 'images/logo.svg';
  export let isShowingSlideShow = false;

  console.log('isShowingSlideShow', isShowingSlideShow);
  
</script>

<div class="header">
  <img src={logo} alt="logo"/>
  {#if isShowingSlideShow}
    <a href="/" class="exit">Stop Slideshow</a>  
    {:else}<a href="/" class="exit">Start Slideshow</a>
  {/if}
</div>

<style>
  .header {
    display: flex;
    justify-content: space-between;
    margin: 2rem;
  }
  img {
    width: 8rem;
  }
  .exit {
    text-transform: uppercase;
  }
</style>