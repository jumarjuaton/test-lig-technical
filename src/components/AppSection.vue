<template>
  <section>
    <article>
      <ul>
        <li v-for="n in 10">
          <div v-for="item in ArticleList">
            <img
              :src="item.defaultImg"
              @mouseover="mouseOver"
              v-show="!active"
              @mouseout="item.hoveredImg = item.defaultImg;"
              :alt="item.date"
            />
            <small>{{ item.date }}</small>
            <h3>
              <strong>{{ item.title }}</strong>
            </h3>
            <p>{{ item.excerpt }}</p>
          </div>
        </li>
      </ul>
      <button type="button" onclick="alert('Hello world!')">More</button>
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
      <h3 class="title-recommended"><strong>Recommend</strong></h3>
      <hr style="margin: 0 20px 20px; border: 2px solid #000;" />
      <ul class="sidebar-list">
        <li v-for="n in 3">
          <div v-for="item in SidebarList">
            <div class="sidebar-list-img">
              <img
                :src="item.defaultImg"
                @mouseover="mouseOver"
                v-show="!active"
                @mouseout="item.hoveredImg = item.defaultImg;"
                :alt="item.date"
              />
            </div>
            <div class="sidebar-list-details">
              <p>{{ item.title }}</p>
              <small>{{ item.date }}</small>
            </div>
          </div>
        </li>
      </ul>
      <ul>
        <li v-for="n in 3" class="list-banner-small">
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
          defaultImg: "https://i.ibb.co/Kxp0K3j/img-item.png",
          hoveredImg: "https://i.ibb.co/3RYGpFG/img-item-hovered.png",
          date: "2016.01.01",
          title:
            "サンプルテキストサンプルテキストサンプルテキストサンプルテキストサンプルテキスト サンプルテキストサンプルテキスト",
          excerpt:
            "サンプルテキストサンプルテキストサンプルテキストサンプルテキストサンプルテキスト サンプルテキストサンプルテキスト..."
        }
      ],
      SidebarList: [
        {
          defaultImg: "https://i.ibb.co/Kxp0K3j/img-item.png",
          hoveredImg: "https://i.ibb.co/3RYGpFG/img-item-hovered.png",
          date: "2016.03.26",
          title:
            "サンプルテキストサンプルテキストサンプルテキストサンプルテキスト"
        }
      ]
    };
  }
};
</script>
