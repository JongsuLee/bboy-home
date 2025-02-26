<script lang="ts">
  import Footer from "./Footer.svelte";
  import Header from "./Header.svelte";
  import { news } from "../../assets/news";
</script>

<Header />
<main class="container">
  <h2>비보이 브라더스 활동</h2>
  <div class="news">
    {#each news as newsData, i}
        <a class="news-item" href={`#/detail/${i}`}>
          <img src={newsData.imgUrl} alt="">
          <div class="item-text">
            <h3>{newsData.title}</h3>
            <p class="date">{newsData.date}</p>
            <div class="hashtag">
              {#each newsData.hashtag as hashtag}
                <span>#{hashtag}</span>&nbsp;
              {/each}
            </div>
          </div>
        </a>
    {/each}
  </div>
</main>
<Footer />

<style lang="scss">
  .news {
    display: flex;
    gap: 20px;

    .news-item {
      width: calc(100% / 3);
      box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.2);

      img {
        width: 100%;
      }

      .item-text {
        padding: 20px;

        h3 {
          margin-bottom: 10px;
        }
  
        p {
          margin-bottom: 4px;
        }
  
        .date, .hashtag {
          font-size: 15px;
          color: #666;
        }
      }

    }
  }

  a {
    color: inherit;
    text-decoration: none;
  }
</style>