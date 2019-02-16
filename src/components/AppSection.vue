<template>
  <section>
    <article class="article__container">
      <ul class="article__list-main">
        <li v-for="n in 10">
          <a
            href="https://iioffice.liginc.co.jp/cebu/"
            title="Article List"
            v-for="item in ArticleList"
          >
            <small>{{ item.dateMain }}</small>
            <h3>
              <strong>{{ item.titleMain }}</strong>
            </h3>
            <p>{{ item.excerpt }}</p>
          </a>
        </li>
      </ul>
      <button
        type="button"
        class="button-more"
        onclick="window.location.href='https://iioffice.liginc.co.jp/cebu/'"
      >
        More
      </button>
    </article>
    <aside>
      <a
        class="sidebar-banner"
        href="https://iioffice.liginc.co.jp/cebu/"
        title="Dummy Banner"
      >
        <img
          src="https://i.ibb.co/72QkFpr/img-banner.jpg"
          title="Dummy Banner"
        />
      </a>
      <h3 class="h3__title--recommended"><strong>Recommend</strong></h3>
      <hr />
      <ul class="article__list-recommend">
        <li v-for="n in 3">
          <a
            href="https://iioffice.liginc.co.jp/cebu/"
            title="Recommend List"
            v-for="item in ArticleList"
          >
            <p>{{ item.titleBSmall }}</p>
            <small>{{ item.dateBSmall }}</small>
          </a>
        </li>
      </ul>
      <ul class="list-banner--small">
        <li v-for="n in 3">
          <a href="https://iioffice.liginc.co.jp/cebu/" title="Dummy Banner"
            ><img src="https://i.ibb.co/qCKkp8Z/img-banner-small.jpg"
          /></a>
        </li>
      </ul>
    </aside>
  </section>
</template>
<script>
export default {
  name: "AppSection",
  data() {
    return {
      ArticleList: [
        {
          dateMain: "2016.01.01",
          dateBSmall: "2016.03.26",
          titleMain:
            "サンプルテキストサンプルテキストサンプルテキストサンプルテキストサンプルテキスト",
          titleBSmall:
            "サンプルテキストサンプルテキストサンプルテキストサンプルテキスト",
          excerpt:
            "サンプルテキストサンプルテキストサンプルテキストサンプルテキストサンプルテキスト サンプルテキストサンプルテキスト..."
        }
      ]
    };
  }
};
</script>
