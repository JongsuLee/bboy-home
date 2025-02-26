<script lang="ts">
    import Footer from "./Footer.svelte";
    import Header from "./Header.svelte";


</script>

<Header />
<main class="container">
  <video 
    autoplay
    loop
    muted
    src="/videoes/5362374-uhd_3840_2160_25fps.mp4"></video>
</main>
<Footer />

<style>
  video {
    width: 100%;
    aspect-ratio: 2.35/1;
    object-fit: cover;
    object-position: center;
  }
</style>
