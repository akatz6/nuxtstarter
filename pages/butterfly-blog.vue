<template>
  <section class="container">
<!--blog Page for the World of Butterflies - page 3-->

<!--header stuff this slot will insert the Butterfly Header component text-->
<butterflyHeader></butterflyHeader>

 <!--nav bar-->
  <div class="nav" style="background-color: #eb34e5;">
    <img src="https://image.flaticon.com/icons/png/512/13/13148.png" class="butter-logo" alt="black butterfly icon">
      <div class="nav-brand">
    <h3>Our Menu</h3>
  </div>
      <nuxt-link to="/" class="butterlinks">Butterfly Home</nuxt-link>
      <nuxt-link to="/butterfly-zoo" class="butterlinks">Buttery Museum</nuxt-link>
       <nuxt-link to="/butterfly-faq" class="butterlinks">Butterfly FAQ</nuxt-link>
    </div>
<!--blog template will be inserted here.-->
    <mrblog v-bind:blogs="blogs"></mrblog>

  </section>
  </template>

    <script>
    import butterflyHeader from '@/components/butterflyHeader'
    import mrblog from '@/components/mrblog'

    export default {
    components: {
    'butterflyHeader': butterflyHeader,
    'mrblog': mrblog
    },

    data () {
    return {
    //this is the array of blog titles and paragraphs of text.
    blogs: [
       {
        title: 'Buterfly Love',
        text: 'Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers, formerly the superfamily Hesperioidea, and the most recent analyses suggest it also contains the moth-butterflies. Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers (formerly the superfamily "Hesperioidea"), and the most recent analyses suggest it also contains the moth-butterflies.'
        },
       {

       title: 'The Care and Feeding of Your Butterfly',
       text: 'Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers (formerly the superfamily "Hesperioidea"), and the most recent analyses suggest it also contains the moth-butterflies. Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers (formerly the superfamily "Hesperioidea"), and the most recent analyses suggest it also contains the moth-butterflies.'
       },

      {
      title: 'Why butterflies make the best pets',
      text: 'Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers (formerly the superfamily "Hesperioidea"), and the most recent analyses suggest it also contains the moth-butterflies. Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers (formerly the superfamily "Hesperioidea"), and the most recent analyses suggest it also contains the moth-butterflies.'
       },

      {
       title: 'Know your butterflies',
       text: 'Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers (formerly the superfamily "Hesperioidea"), and the most recent analyses suggest it also contains the moth-butterflies. Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers (formerly the superfamily "Hesperioidea"), and the most recent analyses suggest it also contains the moth-butterflies.'
       },
      {
      title: 'Which is the right butterfly for you?',
      text: 'Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers (formerly the superfamily "Hesperioidea"), and the most recent analyses suggest it also contains the moth-butterflies. Butterflies are insects in the macrolepidopteran clade Rhopalocera from the order Lepidoptera, which also includes moths. Adult butterflies have large, often brightly coloured wings, and conspicuous, fluttering flight. The group comprises the large superfamily Papilionoidea, which contains at least one former group, the skippers (formerly the superfamily "Hesperioidea"), and the most recent analyses suggest it also contains the moth-butterflies.'
       }
    ]
    }
    }

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


#bBlog div {
  display: flex;
  flex-direction: column;
  margin: 6px 8px;
}

.blog-box {
 display: flex;
  flex-direction: row;
  margin: 50px;
  background-color: white;
}

.blog-title {
  color: purple;
  margin-left: 50px;
  font-weight: bold;
}

</style>
