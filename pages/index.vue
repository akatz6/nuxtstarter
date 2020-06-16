<template>
<div>

  <div class="header">
    <slot name="butterfly-header"></slot>
  </div>
  <div class="nav" style="background-color: #eb34e5;">
    <img src="https://image.flaticon.com/icons/png/512/13/13148.png" class="butter-logo" alt="black butterfly icon">
    <h3>Our Menu</h3>
    <nuxt-link to="/butterfly-zoo" class="butterlinks">Butterfly Museum</nuxt-link>
    <nuxt-link to="/butterfly-blog" class="butterlinks">Buttery Blog</nuxt-link>
    <nuxt-link to="/butterfly-faq" class="butterlinks">Butterfly FAQ</nuxt-link>
  </div>
  <div class="wrapper">
              <h1 class="heading">Names of Species</h1>
              <section class="container" v-if="insects">
                <card v-for="insect of insects"
                :key="insect.id"
                :insect="insect"/>
                 </section>
        </div>
</div>
</template>

<script>

import butterflyHeader from "@/components/butterflyHeader"
import axios from 'axios'
export default {
  components: {
    'butterflyHeader': butterflyHeader
  },
  data() {
    return {
      loading: true,
      insects: null,
      errored: false
    }
  },
  mounted() {
    axios.get("https://api.gbif.org/v1/species?datasetKey=ca515b82-e301-43ff-9f69-2c0116e1c95b&sourceId=6B773CF4C72F0995A4228111BFAA28B8.taxon")
      .then(response => {
        this.insects = response.data
        console.log(this.insects);
        debugger;
      })
      .catch(error => {
        this.errored = true
      })
      .finally(() => this.loading = false)
    }
  }
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
