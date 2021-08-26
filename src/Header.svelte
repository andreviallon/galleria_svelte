<script lang="ts">
  let logo = 'images/logo.svg';
  export let isShowingSlideShow = false;
</script>

<div class="header">
  <img src={logo} alt="logo"/>
  {#if isShowingSlideShow}
    <a href="/" class="exit">Stop Slideshow</a>  
    {:else}<a href="/" class="exit">Start Slideshow</a>
  {/if}
</div>
<hr />

<style>
  .header {
    display: flex;
    justify-content: space-between;
  }
  img {
    width: 8rem;
  }
  .exit {
    text-transform: uppercase;
    color: #7D7D7D;
    letter-spacing: 2.5px;
    display: flex;
    align-items: center;
  }

  hr {
    color: #E5E5E5;
    margin: 2rem 0;
    border-bottom: 0;
  }
</style>