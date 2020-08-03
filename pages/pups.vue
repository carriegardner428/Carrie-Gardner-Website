<template>
  <div id="pups-page" class="page-wrapper pups-page content-page">
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <h3 class="subtitle is-3">
          Cedar &amp; Willow
        </h3>
        <template>
          <b-carousel-list
            v-model="test"
            :data="items"
            :items-to-show="2"
            :repeat="true"
            :arrow="true"
          >
            <template slot="item" slot-scope="props">
              <div class="card">
                <div class="card-image">
                  <figure class="image is-5by4">
                    <img
                      :src="require('~/assets/uploads/' + props.list.image).src"
                      :srcset="
                        require('~/assets/uploads/' + props.list.image).srcSet
                      "
                    />
                  </figure>
                </div>
                <div class="card-content">
                  <div class="content">
                    <p class="title is-6">
                      {{ props.list.title }}
                    </p>
                  </div>
                </div>
              </div>
            </template>
          </b-carousel-list>
        </template>
      </template>
    </main-section>
  </div>
</template>
<script>
export default {
  head() {
    return {
      title: `Pups | ${this.$siteConfig.siteName}`
    }
  },
  data() {
    return {
      test: 0,
      items: [
        {
          title: 'Car Ride',
          image: 'cedar-willow/car-ride.png'
        },
        {
          title: 'Cedar Big Ears',
          image: 'cedar-willow/cedar-big-ears.png'
        },
        {
          title: 'Cedar at Lake Grapevine',
          image: 'cedar-willow/cedar-lake-grapevine.png'
        },
        {
          title: 'Cedar Model Shot',
          image: 'cedar-willow/cedar-model-shot.png'
        },
        {
          title: 'Little Willow',
          image: 'cedar-willow/lil-willow.jpg'
        },
        {
          title: "Pups in Mom's Office",
          image: 'cedar-willow/pups-in-moms-office.png'
        },
        {
          title: 'Trouble Pups',
          image: 'cedar-willow/trouble-pups.png'
        },
        {
          title: 'Willow Kiss',
          image: 'cedar-willow/willow-kiss.png'
        },
        {
          title: 'Willow Kisses',
          image: 'cedar-willow/willow-kisses.png'
        },
        {
          title: 'Willow Show Time',
          image: 'cedar-willow/willow-shower-time.png'
        }
      ]
    } // return
  },
  methods: {
    info(value) {
      this.test = value
    }
  }
}
</script>
