<script>
  import { paintings } from '../paintings';  
  console.log(paintings);
</script>

<div class="grid">
  {#each paintings as painting}
  <div class="thumbnail" style="background-image: linear-gradient(to bottom, rgba(0,0,0,0) 20%, rgba(0,0,0,1)), url({painting.images.hero.small})">
    <div class="painting-info">
      <p class="name">{painting.name}</p>
      <p class="artist">{painting.artist.name}</p>
    </div>
  </div>
  {/each}
</div>

<style>
  .grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 2rem;
  }

  .thumbnail {
    background-size: cover;
    background-repeat: no-repeat;
    width: 100%;
    height: 190px;
  }

  .painting-info {
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: end;
    padding: 0 1.5rem;
  }

  p {
    margin: 0;
    color: white;
  }

  .name {
    font-weight: 500;
    font-size: 1.6rem;
    margin-bottom: 0.3rem;
  }

  .artist {
    margin-bottom: 1.4rem;
    opacity: 0.7;
  }
  </style>