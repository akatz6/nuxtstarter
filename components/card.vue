<!--CARD.VUE TEMPLATE-->
<template lang="html">
  <section>


<article class="card">

    <h2 class="card_title">{{insect.nameString}}</h2>
    <p class="card_copy">{{insect.status}}</p>

  </article>
</section>
</template>

<script>
export default {
  props: {
   insect: Object
  }
}

</script>

<style lang="css" scoped>
</style>
