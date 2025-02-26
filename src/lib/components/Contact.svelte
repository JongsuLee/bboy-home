<script lang="ts">
    import Footer from "./Footer.svelte";
import Header from "./Header.svelte";


</script>

<Header />
<main class="container">
  <h2>최고의 무대를 선사하겠습니다.</h2>
  <div class="contact">
    <figure class="map">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3163.3960056318633!2d126.72996287632236!3d37.54573282531992!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x357c82649611079d%3A0x1dce8daa838e7d04!2z7J247LKc6rSR7Jet7IucIOqzhOyWkeq1rCDsnoTtlZnshJzroZwgMzI!5e0!3m2!1sko!2skr!4v1740540082833!5m2!1sko!2skr" width="100%" height="450" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </figure>
    <address>
      <p>인천광역시 계양구 임학서로32</p>
      <p>빅브라더 스튜디오</p>
      <p>Email: <a href="mailto:leaguematter@naver.com">leaguematter@naver.com</a></p>
      <p>Tel: <a href="tel:010-9015-2071">010-9015-2071</a></p>
    </address>
  </div>
</main>
<Footer />

<style lang="scss">
  .contact {
    display: flex;
    gap: 50px;
    
    figure, address {
      width: 50%;
    }

    address {
      font-style: normal;
    }

    a {
      color: inherit;
    }
  }

  .container {
    background-color: #fff;
  }
</style>