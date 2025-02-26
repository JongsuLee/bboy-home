<script lang="ts">
    import { getNews } from "../../assets/news";
  import Footer from "./Footer.svelte";
  import Header from "./Header.svelte";

  export let params: {id: number}

  const news = getNews(params.id)
</script>

<Header />
<main class="container">
  <div class="main-header">
    <h2>{news?.title}</h2>
    <p class="date">{news?.date}</p>
    <img src={news?.detailImgUrl} alt="">
  </div>
  <article>
    <p>{@html news?.desc}</p>
  </article>
</main>
<Footer />

<style lang="scss">
  .main-header {
    h2 {
      margin-bottom: 10px;
    }

    .date {
      margin-bottom: 20px;
      font-size: 15px;
      color: #666;
    }
  }

  article {
    margin-top: 50px;
  }
</style>