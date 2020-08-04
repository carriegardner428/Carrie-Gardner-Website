<template>
  <div id="home-page" class="page-wrapper home-page">
    <!-- <site-hero :title="title" :subtitle="subtitle" :image="featureImage">
    </site-hero> -->
    <main-section theme="sidebar-left">
      <template v-slot:sidebar>
        <figure>
          <img
            :src="require('~/assets/uploads/carrie/carrie-2019.png').src"
            :srcset="require('~/assets/uploads/carrie/carrie-2019.png').srcSet"
          />
        </figure>
      </template>
      <template v-slot:default>
        <section class="hero is-medium">
          <div class="hero-body">
            <div class="container">
              <h1 class="title">
                Carrie Gardner
              </h1>
              <div class="content">
                <p>
                  <!-- eslint-disable-next-line -->
                  <font-awesome-icon icon="terminal" /> &emsp; Researcher &amp; Developer &#64; <span><a class="has-text-info" href="https://www.sei.cmu.edu" target="_blank">Carnegie Mellon University Software Engineering Institute</a></span>
                </p>
                <!-- eslint-disable-next-line -->
                <p><font-awesome-icon icon="user-graduate" /> &emsp; MBA Student &#64; <span class="font-family:Arial"><a class="has-text-info" href="https://www.cmu.edu/tepper/" target="_blank">Tepper School of Business</a></span></p>
                <p><font-awesome-icon icon="biking" /> &emsp; Fitness Lover</p>
                <p>
                  <font-awesome-icon icon="seedling" /> &emsp;
                  <!-- eslint-disable-next-line -->
                  <span>Gard<span class="has-text-success is-uppercase has-text-weight-bold" style="transform: rotate(45deg);-webkit-transform: rotate(45deg);">e</span>ner</span>
                </p>
                <!-- eslint-disable-next-line -->
                <p><font-awesome-icon icon="paw" /> &emsp; Dog Mom to <a class="has-text-info" href="https://www.instagram.com/cedarandwilllow/">Cedar &amp; Willow</a></p>
              </div>
            </div>
          </div>
        </section>
      </template>
    </main-section>
  </div>
</template>

<script>
import { mapState } from 'vuex'
import { setPageData } from '../helper'

export default {
  name: 'HomePage',
  head() {
    return {
      title: `Home | ${this.$siteConfig.siteName}`
    }
  },
  computed: {
    ...mapState(['title', 'subtitle', 'featureImage'])
  },
  fetch({ store, params }) {
    setPageData(store, { slug: 'home' })
  }
}
</script>

<style>
.home-page .under-subtitle {
  border-top: none;
}
</style>
