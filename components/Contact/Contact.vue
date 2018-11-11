<template>
  <v-layout row wrap>
    <v-flex lg6 id="contact-section" class="contact-section">
      <gmap-map class="hidden-sm-and-down" :options="{styles:styles}" :center="center" :zoom="11" style="width: 100%; height: 750px">
        <gmap-marker :key="index" v-for="(m, index) in markers" :position="m.position" :clickable="true" :draggable="false"
          @click="center=m.position"></gmap-marker>
      </gmap-map>
    </v-flex>
    <v-flex lg6 xs12 class="pa-5 text-xs-center">

      <h1 class="display-2">Contact Us</h1>
      <v-hover>
        <v-card slot-scope="{ hover }" :class="`elevation-${hover ? 12 : 2}`" color="cyan darken-2" class="ma-5 pa-5">
          <v-icon class="icn">phone</v-icon> <a class="card-link pl-2" href="telno:+1 214 371 0727">+1 214 371 0727</a>
        </v-card>
      </v-hover>
      <v-hover>
        <v-card slot-scope="{ hover }" :class="`elevation-${hover ? 12 : 2}`" color="cyan darken-2" class="ma-5 pa-5">
          <v-icon class="icn">email</v-icon> <a class="card-link pl-2" href="mailto:contact@luxuryinndallas.com">contact@luxuryinndallas.com</a>
        </v-card>
      </v-hover>
      <v-hover>
        <v-card slot-scope="{ hover }" :class="`elevation-${hover ? 12 : 2}`" color="cyan darken-2" class="ma-5 pa-5">
          <v-icon class="icn">location_on</v-icon> <a class="card-link pl-2" href="https://goo.gl/maps/MgHGy7f3P7q">5606
            S R. L. Thornton Fwy Dallas, TX 75232</a>
        </v-card>
      </v-hover>
    </v-flex>
  </v-layout>
</template>

<style lang="scss" scoped>
  .card-link {
    text-decoration: none;
    font-size: 2em;
    color: white;
  }

  .icn {
    font-size: 2em;
    color: white;
  }

</style>


<script>
  import * as VueGoogleMaps from '~/node_modules/vue2-google-maps/src/main'
  import Vue from 'vue';

  Vue.use(VueGoogleMaps, {
    load: {
      key: 'AIzaSyCD3ZSWJFah8OXDnYKSdUN6KnDC_yRriVg',
      v: 'OPTIONAL VERSION NUMBER',
    }
  });

  export default {
    data() {
      return {
        center: {
          lat: 32.555000,
          lng: -96.857650
        },

        markers: [{
          position: {
            lat: 32.555000,
            lng: -96.857650
          }
        }],

        styles: [{
            "featureType": "administrative",
            "elementType": "labels.text.fill",
            "stylers": [{
              "color": "#444444"
            }]
          },
          {
            "featureType": "landscape",
            "elementType": "all",
            "stylers": [{
              "color": "#f2f2f2"
            }]
          },
          {
            "featureType": "poi",
            "elementType": "all",
            "stylers": [{
              "visibility": "off"
            }]
          },
          {
            "featureType": "road",
            "elementType": "all",
            "stylers": [{
                "saturation": -100
              },
              {
                "lightness": 45
              }
            ]
          },
          {
            "featureType": "road.highway",
            "elementType": "all",
            "stylers": [{
              "visibility": "simplified"
            }]
          },
          {
            "featureType": "road.arterial",
            "elementType": "labels.icon",
            "stylers": [{
              "visibility": "off"
            }]
          },
          {
            "featureType": "transit",
            "elementType": "all",
            "stylers": [{
              "visibility": "off"
            }]
          },
          {
            "featureType": "water",
            "elementType": "all",
            "stylers": [{
                "color": "#0097A7"
              },
              {
                "visibility": "on"
              }
            ]
          }
        ]
      }
    }
  }

</script>
