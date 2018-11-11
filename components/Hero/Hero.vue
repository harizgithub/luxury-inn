<template>
  <div>
    <v-parallax class="hero-img" dark src="https://images.unsplash.com/photo-1507221540848-a93c073b63be?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=a204f864d7a70dee5c56e9ebc16f344a&auto=format&fit=crop&w=1600&q=80">
      <v-layout align-center justify-center>
      </v-layout>
    </v-parallax>
    <v-flex xs8 offset-xs2 class="pa-5 heading">
      <h1 class="text-xs-center display-2 mb-3">Welcome to Luxury Inn Dallas Texas</h1>
      <h4 class="text-xs-center title font-weight-thin  pt-2">
        Where Warm hospitality and comfortable accommodation awaits you
      </h4>
    </v-flex>
  </div>
</template>

<style lang="scss" scoped>
  .hero-img {
    z-index: 1;
  }
  .overlay {
    background: rgba($color: #000000, $alpha: 0.5);
    padding: 2%;
  }

  .heading {
    margin-top: -5%;
    padding-top: 10px;
    z-index: 1;
    position: relative;
    background: white;
    color: #000000;
    -webkit-box-shadow: 10px 10px 111px -7px rgba(0, 0, 0, 0.42);
    -moz-box-shadow: 10px 10px 111px -7px rgba(0, 0, 0, 0.42);
    box-shadow: 10px 10px 111px -7px rgba(0, 0, 0, 0.42);
  }

</style>
