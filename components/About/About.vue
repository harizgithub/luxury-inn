<template>
  <div>
    <v-layout row wrap>
      <v-flex class="img hidden-sm-and-down" md12 lg6>
        <v-img :height="750" src="https://res.cloudinary.com/hariztek/image/upload/v1541144763/luxury%20inn/mb.jpg" />
      </v-flex>
      <v-flex lg6 py-5>
        <v-container class="text-xs-center pl-5 pr-5">
          <h4 class="font-weight-thin">
            Affluent in atmosphere yet affordable in price. We are close to many great attractions around the Dallas
            area; Our Attractions page contains a list of local area activities, entertainment, and dining. Each room
            at the Luxury Inn Dallas includes Local telephone calls, Wakeup call, High-Speed Wireless Internet Access
            with 40" LED TV including Local, Movies and Sports channels. They are simply decorated and have a work
            desk. Some rooms have a spa bath, Micro, fridge and in-room coffee maker. Also, includes 24-hour front desk
            services. The hotel offers immediate access to Highway 67, loop 12 and Interstate 35, 20 and 45.
            Dallas/Fort Worth International Airport is 26 miles, and Dallas Love Field Airport is 13 Miles away. The
            Dallas Zoo is 5 minutes’ drive from the Hotel. The Dallas Convention Center is 9 miles away. Conveniently
            close to Dallas Downtown, State Fair of Texas and 20 miles from AT&T Dallas Cowboys Stadium.
          </h4>
        </v-container>
      </v-flex>
    </v-layout>
  </div>
</template>

<style lang="scss">
  .img {
    margin-top: -7%;
    position: relative;

  }

  h4 {
    font-size: 1.5em;
  }

  @media only screen and (min-width:960px) {
    .img {
      margin-top: -22%;
    }

    @media only screen and (min-width:1263px) {
      .img {
        margin-top: -10%;
      }
    }
  }

</style>
