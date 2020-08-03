<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About Carrie"
      subtitle="Example About Page"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>Carrie</h3>
          <p>
            <strong>Short Bio</strong>
          </p>
          <p>
            Carrie Gardner is a Cyber Security Engineer with the Carnegie Mellon
            University Software Engineering Institute (SEI). Carrie specializes
            in data curation and analysis, and loves designing and engingeering
            risk intelligence products to provide customers insight and
            recommendations, enabling evidence-based decision making.
          </p>
          <p>
            <strong>Long Bio</strong>
          </p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit!
          </p>
          <quote-card />
          <h3>Cedar &amp; Willow</h3>
        </div>
        <template>
          <b-carousel>
            <b-carousel-item v-for="(carousel, i) in carousels" :key="i">
              <section :class="`hero is-medium is-${carousel.color}`">
                <div class="hero-body has-text-centered">
                  <h1 class="title">
                    {{ carousel.text }}
                  </h1>
                </div>
              </section>
            </b-carousel-item>
          </b-carousel>
        </template>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard },
  data() {
    return {
      carousels: [
        { text: 'Slide 1', color: 'primary' },
        { text: 'Slide 2', color: 'info' },
        { text: 'Slide 3', color: 'success' },
        { text: 'Slide 4', color: 'warning' },
        { text: 'Slide 5', color: 'danger' }
      ]
    }
  }
}
</script>
