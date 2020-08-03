<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <!-- <site-hero
      title="About Carrie"
      subtitle="Example About Page"
      image="/uploads/about-hero.jpg"
    ></site-hero> -->
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <h3 class="subtitle is-3">
          Carrie
        </h3>
        <div class="content">
          <p class="has-text-weight-bold">
            Short Bio
          </p>
          <p>
            Carrie Gardner is a Cyber Security Engineer with the Carnegie Mellon
            University Software Engineering Institute (SEI). Carrie specializes
            in data curation and analysis, and loves designing and engingeering
            risk intelligence products to provide customers insight and
            recommendations, enabling evidence-based decision making.
          </p>
          <blockquote class="has-text-weight-bold is-size-4 has-text-right">
            "I design, develop, and transition products, tools, and strategies
            to to enable my customers to achieve advantage in cyber."
          </blockquote>
          <!-- <p class="has-text-weight-bold">
            Long Bio
          </p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit! Lorem ipsum dolor sit amet, consectetur
            adipisicing elit. Adipisci eligendi impedit inventore ipsa
            laboriosam libero magnam modi odio, sunt temporibus. Distinctio
            doloremque eum magni nostrum quasi ratione rem repudiandae sit!
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit! Lorem ipsum dolor sit amet, consectetur
            adipisicing elit. Adipisci eligendi impedit inventore ipsa
            laboriosam libero magnam modi odio, sunt temporibus. Distinctio
            doloremque eum magni nostrum quasi ratione rem repudiandae sit!
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit! Lorem ipsum dolor sit amet, consectetur
            adipisicing elit. Adipisci eligendi impedit inventore ipsa
            laboriosam libero magnam modi odio, sunt temporibus. Distinctio
            doloremque eum magni nostrum quasi ratione rem repudiandae sit!
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit!
          </p> -->
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <!-- <posts-grid :per-row="1" :number="2" /> -->
        <p>Coming Soon</p>
      </template>
    </main-section>
  </div>
</template>
<script>
// import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  }
  // components: { QuoteCard },
}
</script>
