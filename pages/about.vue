<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <!-- <site-hero
      title="About Carrie"
      subtitle="Example About Page"
      image="/uploads/about-hero.jpg"
    ></site-hero> -->
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
          </p>
          <quote-card />
          <h3>Cedar &amp; Willow</h3>
        </div>
        <template>
          <b-carousel
            :autoplay="false"
            with-carousel-list
            :indicator="true"
            :overlay="gallery"
          >
            <b-carousel-item v-for="(item, i) in carouselItems" :key="i">
              <div class="card">
                <div class="card-image">
                  <figure
                    class="image is-covered is-1by1"
                    @click="switchGallery(true)"
                  >
                    <img
                      class="img-responsive"
                      :src="require('~/assets' + item.image).src"
                      :srcset="require('~/assets' + item.image).srcSet"
                      :alt="item.text"
                    />
                  </figure>
                </div>
              </div>
            </b-carousel-item>
            <span
              v-if="gallery"
              class="modal-close is-large"
              @click="switchGallery(false)"
            />
            <template slot="list" slot-scope="props">
              <b-carousel-list
                v-model="props.active"
                :data="carouselItems"
                :config="al"
                :refresh="gallery"
                as-indicator
                @switch="props.switch($event, false)"
              />
            </template>
            <template slot="overlay">
              <div class="has-text-centered has-text-white">
                Cedar &amp; Willow
              </div>
            </template>
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
      gallery: false,
      al: {
        hasGrayscale: true,
        itemsToShow: 2,
        drag: true,
        gray: true,
        breakpoints: {
          768: {
            hasGrayscale: false,
            itemsToShow: 4
          },
          960: {
            hasGrayscale: true,
            itemsToShow: 6
          }
        }
      },
      carouselItems: [
        { text: 'Car Ride', image: '/uploads/cedar-willow/car-ride.png' },
        {
          text: 'Cedar Big Ears',
          image: '/uploads/cedar-willow/cedar-big-ears.png'
        },
        {
          text: 'Cedar at Lake Grapevine',
          image: '/uploads/cedar-willow/cedar-lake-grapevine.png'
        },
        {
          text: 'Cedar Model Shot',
          image: '/uploads/cedar-willow/cedar-model-shot.png'
        },
        {
          text: 'Little Willow',
          image: '/uploads/cedar-willow/lil-willow.jpg'
        },
        {
          text: "Pups in Mom's Office",
          image: '/uploads/cedar-willow/pups-in-moms-office.png'
        },
        {
          text: 'Trouble Pups',
          image: '/uploads/cedar-willow/trouble-pups.png'
        },
        { text: 'Willow Kiss', image: '/uploads/cedar-willow/willow-kiss.png' },
        {
          text: 'Willow Kisses',
          image: '/uploads/cedar-willow/willow-kisses.png'
        },
        {
          text: 'Willow Show Time',
          image: '/uploads/cedar-willow/willow-shower-time.png'
        }
      ]
    } // return
  },
  methods: {
    switchGallery(value) {
      console.log('gallery switch')
      this.gallery = value
      if (value) {
        return document.documentElement.classList.add('is-clipped')
      } else {
        return document.documentElement.classList.remove('is-clipped')
      }
    }
  }
}
</script>
