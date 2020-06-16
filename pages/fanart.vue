<template lang="html">
  <section class="container">
<div class="fan-title">
  <nuxt-link to="/" class="fanlinks">Butterfly Home</nuxt-link>
    <nuxt-link to="/butterfly-zoo" class="fanlinks">Butterfly Museum</nuxt-link>
  <h1 class="butter-title">Fan Art</h1>
  <h4>Photos from butterfly Fans</h4>

<div class="wrap">
  <div class="thumbnails">
  <img v-b-tooltip.hover title="photos of the week" width="90%" v-for="(photo, index) in photos"
  :key="index"
  :src="photo"
  @click="activePhoto = index"
  :class="{'active': activePhoto == index}"
  :style="'background-image: url('+photo+');'"
  />
</div>
</div>
</div>
</section>
</template>

<script>
export default {
  data() {
    return {
      photos: [
        'https://images.unsplash.com/photo-1526336024174-e58f5cdd8e13?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80 ',
        'https://images.unsplash.com/photo-1571030905044-7458c2a7ac24?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80',
        'https://images.unsplash.com/photo-1512384581201-653524dbe0c4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=309&q=80',
        'https://images.unsplash.com/photo-1512384714738-48bc147e56a5?ixlib=rb-1.2.1&auto=format&fit=crop&w=364&q=80',
        'https://images.unsplash.com/photo-1495232416988-d26458b7a5fb?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=317&q=80',
        'https://images.unsplash.com/photo-1548984363-d6e54c098bc5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80',
        'https://images.unsplash.com/photo-1540256817643-88ca55778eb6?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=751&q=80',
        'https://images.unsplash.com/photo-1560263816-d704d83cce0f?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80',
        'https://images.unsplash.com/photo-1486916856992-e4db22c8df33?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=667&q=80',
         'https://images.unsplash.com/photo-1557912407-eb2900cf49e8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80'
      ]
    }
  },
}
</script>
<style>
.fan-title {
  background-color: #5c4084;
  padding: 25px;
}

.fanlinks {
  color: magenta;
  text-decoration: none;
  padding: 2%;
}

.wrap {
  margin: auto;
  padding: 6px;
  background-color: #fff;
  border-radius: 8px;
  max-width: 800px;
  box-shadow: 0 5px 8px #0000007a;
}

.butter-title {
color: magenta;
text-shadow:  2px 2px black;
}

h4 {
  padding: 2px;
}

/*
.butter-title {
  background: -webkit-linear-gradient(#fff, lighten(#5c4084, 20%));
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
  text-align: center;
  margin: 0 0 5px 0;
  font-weight: 900;
  font-size: 4rem;
  color: #fff;
}
h4 {
  color: lighten(#5c4084, 20%);
  text-align: center;
  margin: 0 0 35px 0;
  font-weight: 400;
  font-size: 24px;
}
*/
.thumbnails {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
  grid-gap: 5px;


  img {
    width: 100%;
    height: 100%;
    border: 2px solid #fff;
    outline: 2px solid #fff;
    cursor: pointer;
    padding-bottom: 65%;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    opacity: 1;
    &:hover {
      opacity: 0.6;
    }
    &:active {
      outline-color: magenta;
      opacity: 1;
    }
  }

}

</style>
