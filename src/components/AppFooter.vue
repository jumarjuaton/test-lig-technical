<template>
  <footer>
    <div class="footer__div">
      <nav class="footer__nav">
        <a href="https://iioffice.liginc.co.jp/cebu/" target="_blank"
          >運営会社</a
        >
        <a href="https://iioffice.liginc.co.jp/cebu/" target="_blank"
          >個人情報保護について</a
        >
      </nav>
      <div id="footer-copyright">&#169;2016 Sample</div>
      <BackToTop></BackToTop>
    </div>
  </footer>
</template>

<script>
import BackToTop from "./BackToTop.vue";

export default {
  name: "AppFooter",
  components: {
    BackToTop
  }
};
</script>
