<template>
  <v-footer
    light
    height="auto"
  >
    <v-card
      flat
      tile
      class="white--text text-xs-center"
      width="100%"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-3 black--text"
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="black--text">
        &copy; <strong>2018 - 2012  Luxury Inn Dallas, Texas</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      icons: [
        'fab fa-facebook'
      ]
    })
  }
</script>