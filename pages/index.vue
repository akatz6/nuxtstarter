<template>
  <section class="container">
<!--Index or Main Page for the World of Butterflies - page 1-->

  <meta property="og:url" content="https://www.si.edu/spotlight/buginfo/butterfly" />
<meta property="og:type" content="website" />
<meta property="og:title" content="Smithsonian Butterflies" />
<meta property="og:description" content="A Site to learn about butterflies"
/>
<meta property="og:image" content="https://www.si.edu/spotlight/buginfo/butterfly">

<!--header stuff this slot will insert the Butterfly Header component text-->

<butterfly-header></butterfly-header>

 <!--nav bar - styled with pink background-->
  <div class="nav" style="background-color: #eb34e5;">
    <div class="nav-brand">
    <img src="https://image.flaticon.com/icons/png/512/13/13148.png" class="butter-logo" alt="black butterfly icon">
    <h3>Our Menu</h3>
  </div>
      <nuxt-link to="/butterfly-zoo" class="butterlinks">Butterfly Museum</nuxt-link>
      <nuxt-link to="/butterfly-blog" class="butterlinks">Buttery Blog</nuxt-link>
       <nuxt-link to="/butterfly-faq" class="butterlinks">Butterfly FAQ</nuxt-link>
   </div>

<!--This is the template for the fun and pithy expression - which was never said by Oscar Wilde - and a button for it's disclaimer-->

 <div>
<p v-if="show"></p>
<h1 v-else>{{title}}</h1>
<span v-if="show">
<h2>{{text}}</h2>
</span>
<!--tried to put a show = !show mixin here, but couldn't get it to work - don't why so took out to leave object functional-->
<button @click="show = !show">*Disclaimer</button>
</div>
<br>
        <img src="https://images.unsplash.com/photo-1465505041184-f383907cc134?ixlib=rb-1.2.1&auto=format&fit=crop&w=778&q=80" class="intro-image" alt="a white butterfly sits on a purple flower">

<!--facebook button to share a butterfly facebook page-->
    <div id="fb-root"></div>

      <script>
        (function(d, s, id) {
        var js, fjs = d.getElementsByTagName(s)[0];
        if (d.getElementById(id)) return;
        js = d.createElement(s); js.id = id;
        js.src =
        "https://connect.facebook.net/en_US/sdk.js#xfbml=1&version=v3.0";
        fjs.parentNode.insertBefore(js, fjs);
        }(document, 'script', 'facebook-jssdk'));

      </script>
        <!-- Your share button code -->
      <div class="fb-share-button" data-href="https://www.si.edu/spotlight/buginfo/butterfly" data-layout="button_count">
      </div>

<!--API stuff this is the template for the API cards-->
      <div class="wrapper">
          <h1 class="heading">Names of Species</h1>
          <section class="container" v-if="insects">
            <card v-for="insect of insects"
            :key="insect.id"
            :insect="insect"/>

           <!--name of species on biodiversity site
           https://api.gbif.org/v1/species?datasetKey=ca515b82-e301-43ff-9f69-2c0116e1c95b&sourceId=6B773CF4C72F0995A4228111BFAA28B8.taxon-->

       <!--butterfly atlas api
       https://species-ws.nbnatlas.org/species/NHMSYS0000841034.json
       catagories: "nameString" and "status"-->
          </section>
        </div>

  </section>
</template>

<script>
import butterflyHeader from '@/components/butterfly-header'
import buttonmixin from '@/components/buttonmixin'
//import axios from 'axios'
import card from '@/components/card'

export default {
  components: {
    'butterfly-header': butterflyHeader,
  //   'axios': axios
  //turned off axios until I get it loaded to program
            },
        data() {
          return {
            show: false,
            title: 'Let decadence be your guide. - Oscar Wilde*',
            text: '*Something he would have said.',
                 loading: true,
                 insects: null,
                 errored: false
          }
        },
//will turn this back on when I load up axios
  // mounted() {
    // axios.get('https://api.gbif.org/v1/species?datasetKey=ca515b82-e301-43ff-9f69-2c0116e1c95b&sourceId=6B773CF4C72F0995A4228111BFAA28B8.taxon')
    //  .then(response =>(this.insect = response.data))
    //   .catch( error => {
    //     this.errored = true
    //   })
    //   .finally(() => this.loading = false)
  //  }
}



</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  text-align: center;
  background-color: #b8d4fc;
}

.header {
  display: block;
  width: 100%;
  padding: 3%;
  background-color: 08fc3d;
  color: white;
}

.butterlinks {
  color: white;
  text-decoration: none;
  padding: 2%;
}

.nav-brand {
  margin-left: 10%;
  display: flex;
  flex-direction: row;
  align-items: flex-end;
}

.butter-logo {
  width: 4%;
  }

.links {
  padding-top: 15px;
}

.intro-image {
  margin: auto;
  width: 60%;
}

</style>
