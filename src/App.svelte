<script lang="ts">
	import Header from './Header.svelte';
	import Gallery from './Gallery.svelte';
	let isShowingSlideShow = false;
</script>

<main>
	<Header isShowingSlideShow={isShowingSlideShow}></Header>
	<Gallery />
</main>
