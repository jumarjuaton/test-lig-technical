<template>
  <section>
    <article class="article">
      <ul>
        <li v-for="n in 10">
          <div v-for="item in ArticleList">
            <a href="/">
              <img :src="item.src" :alt="item.date" />

              <small>{{ item.date }}</small>
              <h3>
                <strong>{{ item.text }}</strong>
              </h3>
              <p>{{ item.text }}</p>
            </a>
          </div>
        </li>
      </ul>
    </article>
  </section>
</template>
<script>
export default {
  name: "AppSection",
  data() {
    return {
      ArticleList: [
        {
          src: "https://i.ibb.co/Kxp0K3j/img-item.png",
          date: "2016.01.01",
          text:
            "サンプルテキストサンプルテキストサンプルテキストサンプルテキストサンプルテキスト サンプルテキストサンプルテキスト"
        }
      ]
    };
  }
};
</script>
