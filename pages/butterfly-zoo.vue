<template>
  <section class="container">
<!--image Page for the World of Butterflies - page 2-->


<!--header stuff this slot will insert the Butterfly Header component text-->
<butterflyHeader></butterflyHeader>

 <!--nav bar-->
  <div class="nav" style="background-color: #eb34e5;">
      <div class="nav-brand">
    <img src="https://image.flaticon.com/icons/png/512/13/13148.png" class="butter-logo" alt="black butterfly icon">
    <h3>Our Menu</h3>
  </div>
      <nuxt-link to="/" class="butterlinks">Butterfly Home</nuxt-link>
      <nuxt-link to="/butterfly-blog" class="butterlinks">Buttery Blog</nuxt-link>
       <nuxt-link to="/butterfly-faq" class="butterlinks">Butterfly FAQ</nuxt-link>
    </div>

   <div>
       <h1>Welcome to the Butterfly Museum</h1>
      <carousel />
    </div>

<nuxt-link to="/fanart">Click here to see Fan Art!</nuxt-link>
   </section>
  </template>

<script>
import butterflyHeader from "@/components/butterflyHeader";
import carousel from "@/components/carousel.vue";

export default {
  components: {
   'butterflyHeader': butterflyHeader,
   'carousel': carousel
    },
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

  .nav {
    background-color: #eb34e5;
    width: 100%;
    padding: 2%;
    color: white;
    }

h1 {
  color: magenta;
  font-size: 300%;
  font-family: "Trebuchet MS", Helvetica, sans-serif;
  padding: 2%;
}
  </style>
