<!--THIS IS THE CODING FOR BUTTERFLY-HEADER.VUE-->

<template>
  <!--this is the basic template for the header of the Butterfly pages-->
<div class="header">
<h1 class="header-title">{{title | uppercase}}</h1>
<h2>{{message | uppercase}}</h2>
<slot></slot>
</div>

</template>


<script>
export default {
  data() {
    return {
      title: 'Welcome to the World of Butterflies',
      message: 'Your source for All Things Buttery that Fly'
    };
  },

filters: {
 uppercase: function(value) {
   return value.toUpperCase();
    }
  }
};

</script>
<style>

.header {
  display: block;
  width: 100%;
  padding: 3%;
  background-color: #33ff33;
  color: white;
}

.header-title {
  font-size: 300%;
  font-family: "Trebuchet MS", Helvetica, sans-serif;
  color: white;
}


</style>
