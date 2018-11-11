<template>
  <section>
    <v-card class="test">
      <v-container fluid grid-list-md>
        <v-layout row wrap>
          <v-flex v-for="card in cards" v-bind="{ [`md${card.flex}`]: true }" :key="card.title">
            <v-card color="" class="text-xs-center pt-3" height="100%">
              <v-icon class="icon black--text" v-html="card.icon" />
              <v-container fill-height fluid pa-2>
                <v-layout fill-height>
                  <v-flex xs12 align-end flexbox>
                    <span class="black--text title font-weight-light" v-text="card.title"></span>
                  </v-flex>
                </v-layout>
              </v-container>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </v-card>
  </section>
</template>

<style lang="scss" scoped>
    .icon {
        font-size: 3em;
    }

    .test {
        background-image: url(https://images.unsplash.com/photo-1518144591331-17a5dd71c477?ixlib=rb-0.3.5&s=413d2357b5302d2e3deb46adc8e570b8&auto=format&fit=crop&w=700&q=80);
        background-size: cover;
        padding: 5%;
    }
</style>


<script>
  export default {
    data: () => ({
      cards: [{
          title: '40" Led TV with 100+ Extended channels including HD',
          icon: 'tv',
          flex: 3
        },
        {
          title: 'Complementary High Speed wireless Internet Access',
          icon: 'wifi',
          flex: 3
        },
        {
          title: 'Affordable Daily / Weekly / Monthly Rates',
          icon: 'attach_money',
          flex: 3
        },
        {
          title: 'Daily Housekeeping',
          icon: 'room_service',
          flex: 3
        },
        {
          title: 'Free Parking 24 h Monitored',
          icon: 'local_parking',
          flex: 3
        },
        {
          title: 'Fridge / Mirco(on request)',
          icon: 'kitchen',
          flex: 3
        },
        {
          title: 'Local Calls',
          icon: 'local_phone',
          flex: 3
        },
        {
          title: 'Vending Machine (Drinks & Snacks)',
          icon: 'free_breakfast',
          flex: 3
        },
      ]
    })
  }

</script>
