<template>
  <v-footer light height="auto">
    <v-card flat tile class="white--text text-xs-center" width="100%">
      <v-layout row wrap>
        <v-flex xs6>
          <v-card-text>
            <v-btn v-for="icon in icons" :key="icon" class="mx-3 black--text" icon>
              <v-icon size="50px">{{ icon }}</v-icon>
            </v-btn>
          </v-card-text>
        </v-flex>
        <v-flex xs6>
           <span>
              <img class="card-icon" src="~/assets/icons/visa.svg" alt="visa">
              <img class="card-icon" src="~/assets/icons/discover.svg" alt="discover">
              <img class="card-icon" src="~/assets/icons/mastercard.svg" alt="mastercard">
              <img class="card-icon" src="~/assets/icons/american_express.svg" alt="american express">
            </span>
        </v-flex>
      </v-layout>

      <v-divider></v-divider>
      <v-card-text class="black--text">
        &copy; <strong>2018 - 2012 Luxury Inn Dallas, Texas</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<style lang="scss" scoped>
.card-icon {
  width: 10%;
}
</style>


<script>
  export default {
    data: () => ({
      icons: [
        'fab fa-facebook'
      ]
    })
  }

</script>

//
