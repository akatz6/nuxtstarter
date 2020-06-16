<!--THIS IS MR. BLOG WHICH IS THE COMPONENT TO BUTTERFLY-BLOG.VUE-->
<template>
  <section class="container">

<!--this is the blog template for whatever needs to go into each blog box-->
  <h1>Buttery Blog</h1>

<div id="bBlog">
  <span class="blog-box" v-for="entry in blogs" :key="entry.title">
    <div v-tooltip="'Butterfly of the month'">
      <img v-b-tooltip.hover title="Butterfly of the Month" src="https://images.unsplash.com/photo-1550103685-da83caf1f0c8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80" width="300" alt="brown butterfly orange flower">
    </div>
    <div>
      <h3 class="blog-title"> {{entry.title}} </h3>
      <p>{{entry.text}} </p>
    </div>
</span>
</div>
</section>
</template>

<script>
export default {

  props: {
    blogs: {
      type: Array,
      required: true,
      }
  }
}
</script>
<style>
</style>
