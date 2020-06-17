<template>
  <section class="container">
<!--faq Page for the World of Butterflies - page 4-->

<!--header stuff this slot will insert the Butterfly Header component text-->
<butterflyHeader></butterflyHeader>


 <!--nav bar-->
  <div class="nav" style="background-color: #eb34e5;">
      <div class="nav-brand">
    <img src="https://image.flaticon.com/icons/png/512/13/13148.png" class="butter-logo" alt="black butterfly icon">
    <h3>Our Menu</h3>
  </div>
      <nuxt-link to="/" class="butterlinks">Butterfly Home</nuxt-link>
      <nuxt-link to="/butterfly-zoo" class="butterlinks">Buttery Museum</nuxt-link>
       <nuxt-link to="/butterfly-blog" class="butterlinks">Butterfly Blog</nuxt-link>
    </div>

<!--my special spiffy FAQ accordian to make sweet, sweet question answering music-->
<!--this will connect to my components pages for the accordion-->
<h1 class="faq-header">Frequently Asked Questions</h1>
<p>Click on each question to find your answer.</p>
<br/>
    <accordian/>

<!--this is the Join Our Club button-->
<div>
    <p v-if="show">Sign up today!!</p>
    <p v-else>Click Here if you like Butterfiles</p>
 <span v-if="show">
   <h1>Join Our Club</h1>
    <p>Enter your email address here and we will put you on our mailing list.</p>
 </span>
    <textarea v-if="show"></textarea>
    <button @click="show = ! show">Press to Join</button>
</div>


    </section>
  </template>

<script>
import butterflyHeader from '@/components/butterflyHeader'
//This will connect my faq page with the accodion component - which will then connect to the baseAccordian component.
import accordian from '@/components/accordian';
export default {
  components: {
      'butterflyHeader': butterflyHeader,
    'accordian': accordian
  },
  data() {
    return {
      show: false
    }
  }
};

</script>

  <style>
  .container {
    min-height: 100vh;
    background-color: #b8d4fc;
  }

  .faq-header {
    font-size: 250%;
  }

</style>
