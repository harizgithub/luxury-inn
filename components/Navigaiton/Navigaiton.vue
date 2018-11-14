<template>
<div id="navigation">
  
  <!--Navigation Toolbar-->
  <v-toolbar>
    <v-toolbar-side-icon class="hidden-md-and-up" @click="drawer = !drawer" />
    <img class="nav-brand hidden-sm-and-down" width="100" src="~/assets/img/nnewlogo.png" alt="">
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-sm-and-down">
      <v-btn primary flat nuxt to="/">Home</v-btn>
      <v-btn primary flat nuxt to="/hotelpolicies">Hotel Policies</v-btn>
      <v-btn primary flat nuxt to="/contact">Contact</v-btn>
    </v-toolbar-items>
    <img class="nav-brand-mobile hidden-md-and-up" width="100" src="~/assets/img/nnewlogo.png" alt="">
  </v-toolbar>  
  <!-- Navigation Drawer -->
    <v-navigation-drawer
    class=""
    light
    temporary
     v-model="drawer"
    absolute
  >
    <v-list>
       <v-list-tile
          v-for="(item, i) in items"
          :to="item.to"
          :key="i"
          router
          exact
        >
        <v-list-tile-action>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-tile-action>

        <v-list-tile-content>
          <v-list-tile-title>{{ item.title }}</v-list-tile-title>
        </v-list-tile-content>
      </v-list-tile>
    </v-list>
  </v-navigation-drawer>
</div>  
</template>


<script>
  export default {
    data () {
      return {
        // use this value to connect drawer icon to toggler
        drawer: false,
        scrolled:false,
        items: [
          { title: 'Home', icon: 'home',  to:"/" },
          { title: 'Hotel Policies', icon: 'assignment_turned_in', to:"/hotelpolicies" },
          { title: 'Contact', icon: 'perm_contact_calendar', to:"/contact" }
        ]
      }
    }   
  }
</script>