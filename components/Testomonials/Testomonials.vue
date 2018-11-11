<template>
  <section class="pa-5 testi-sec">
    <v-container>
      <h1 class="display-2 pb-5 text-xs-center">What Our Customers Say</h1>
    </v-container>
    <!-- card -->
    <v-container fluid grid-list-md>
      <v-layout row wrap>
        <v-flex lg3 md6 sm6 xs12 v-for="card in cards" :key="card.title">
          <v-card class="pa-5 review-card">
            <div class="text-xs-center">
              <v-avatar size="80" class="avater" color="grey lighten-4">
                <img :src="card.src" alt="avatar">
              </v-avatar>
              <p class="text-xs-center title pt-2" v-text="card.title"></p>
              <v-divider></v-divider>
              <v-rating class="pt-2 pb-2" color="secondary" v-model="card.rating"></v-rating>
              <span class="text-xs-center subheading" v-text="card.review"></span>
            </div>
          </v-card>
        </v-flex>
      </v-layout> 
    </v-container>
    <!-- end card -->
    <div class="text-xs-center">
          <v-btn href="https://www.google.com/maps/place/Luxury+Inn/@32.6777915,-96.8237977,17z/data=!4m7!3m6!1s0x864e973a47aa047b:0xc973bf06b2f79a15!8m2!3d32.677787!4d-96.821609!9m1!1b1" target="_blank">via Google</v-btn>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.testi-sec {
  background-color: #0097A7;
  color: white;
}

.avater {
  margin-top: -35%;
  position: relative;
}

 @media only screen and (max-width: 600px)  {
    
  }
</style>


<script>
  export default {
    data: () => ({
      cards: [{
          src: 'https://lh3.googleusercontent.com/-gOLFNeKPvCE/AAAAAAAAAAI/AAAAAAAAAAA/J4UqYvHt_hI/w90-h90-p-rp-mo-ba3-br100/photo.jpg',
          title: 'preciousmck84',
          review: 'My favorite place. Great customer service.  Clean and they know me. When I come',
          rating: 5
        },
        {
          src: 'https://lh3.googleusercontent.com/-GqCXDmYUkAI/AAAAAAAAAAI/AAAAAAAAAAA/seQxuSAY4vM/w90-h90-p-rp-mo-br100/photo.jpg',
          title: 'Michael Edwards',
          review: 'Hello world this is a great spot. Prices quality and quantity is great. Proper room service and all. My name is Averie a guest with Michael.',
          rating: 5
        },
        {
          src: 'https://lh4.googleusercontent.com/-T7Z5QfU5hhE/AAAAAAAAAAI/AAAAAAAAAAA/zge3DcAc0Yk/w90-h90-p-rp-mo-br100/photo.jpg',
          title: 'Gabriel Clark',
          review: 'Great Price, Clean rooms, fast Wi-Fi, no bedbugs, friendly staff what more are you looking for in a room?',
          rating: 5
        },
        {
          src: 'https://lh4.googleusercontent.com/-95IYUEt4kiU/AAAAAAAAAAI/AAAAAAAAAAA/uoGk7z7MP5Y/w90-h90-p-rp-mo-br100/photo.jpg',
          title: 'Gloria Potts',
          review: 'Its clean and nice i always come here the staff is nice and friendly',
          rating: 5
        },
      ]
    })
  }

</script>
