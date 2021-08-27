<script>
  import { paintings } from '../paintings';  
  console.log(paintings);
</script>

<div class="grid">
  {#each paintings as painting}
    <div class="painting-container">
      <div class="painting-img-holder" style="background-image: linear-gradient(to bottom, rgba(0,0,0,0) 20%, rgba(0,0,0,1)), url({painting.images.gallery})"></div>
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
    grid-template-columns: repeat(5, minmax(0, 1fr));
    gap: 2rem;
  }

  @media only screen and (max-width: 1600px) {
      .grid {
        grid-template-columns: repeat(4, minmax(0, 1fr));
      }
  }
  
  @media only screen and (max-width: 1000px) {
      .grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
  }

  @media only screen and (max-width: 600px) {
      .grid {
        grid-template-columns: repeat(1, minmax(0, 1fr));
      }
  } 

  .painting-container {
    cursor: pointer;
    width: 100%;
    height: 300px;
    overflow: hidden;
    position: relative;
  }

  .painting-img-holder {
    width: 100%;
    height: 100%;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
  }
  .painting-container:hover > .painting-img-holder {
    transform: scale(1.15);
  }

  .painting-info {
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: end;
    position: absolute;
    bottom: 0;
    padding: 1rem;
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
    margin-bottom: 0.8rem;
    opacity: 0.7;
  }
  </style>