<template>
  <v-app>
    <nav>
      <v-app-bar
        height="55px"
        scroll-off-screen
        app
        dense
      >
        <v-app-bar-nav-icon
          class="hidden-sm-and-up"
          @click.stop="drawer = !drawer"
        />
        <!-- </v-btn> -->
        <v-toolbar-title
          class="ml-2 pl-2"
          :to="$url('/')"
          title="Home"
        >
          <!-- <v-img 
            :src="require('@/assets/img/logo/logo4.png')"
              :lazy-src="require('@/assets/img/logo/logo4.png')"
              width="10vh"
              height="50px"
              >
               
              </v-img>
          -->
          <g-image src="@/assets/img/logo/logo.png" width="100vh" alt='farmer first logo'/>
        </v-toolbar-title>
        <v-spacer />
        <v-toolbar-items
          class="hidden-xs-only"
        >
          <v-btn
            text
            :to="$url('/')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
          >
            Home
          </v-btn>
          <v-btn
            text
            :to="$url('/about')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
          >
            About
          </v-btn>
          <!-- <v-btn
            text
            :to="$url('/team')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
          >
            Our team
          </v-btn> -->
          <v-btn
            text
            :to="$url('/Farms')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
          >
            Farms
          </v-btn>
          <v-btn
            text
            :to="$url('/contact')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
          >
            Contact
          </v-btn>
        </v-toolbar-items>
      </v-app-bar>
    
      <v-navigation-drawer
        v-model="drawer"
        temporary
        app
      >
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="title blue--text pl-5">
             <g-image src="@/assets/img/logo/logo.png" width="100vh alt='farmer first logo' "/>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
        <v-list dense nav>
        <v-list-item 
        >
         
          <v-list-item-content>
            <v-list-item-title
            
            >
            <v-btn
            text
            :to="$url('/')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
          >
          <v-icon class="mr-1">home</v-icon>
            Home
          </v-btn>
            
            </v-list-item-title>
              <v-list-item-title
            >
            <v-btn
            text
            :to="$url('/about')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
          >
           <v-icon class="mr-1">mdi-view-dashboard</v-icon>
            About
          </v-btn>
            
            </v-list-item-title>
              <v-list-item-title >
            <v-btn
            text
            :to="$url('/services')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
          >
             <v-icon class="mr-1">info</v-icon>
            Services
          </v-btn>
            
            </v-list-item-title>
              <v-list-item-title 
            >
         
             <v-btn
            text
            :to="$url('/contact')"
            style="text-transform: capitalize;"
            flat
            class="ml-0"
          >
          <v-icon class="mr-1">mdi-dialpad</v-icon>
            Contact
          </v-btn>
            
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      </v-navigation-drawer>
    </nav>
    <v-content class="" style="background-color:white" >
        <slot />
    </v-content>

   
      <Footer />
  
  </v-app>
</template>

<static-query>
  query {
    metadata {
      siteName
    }
  }
</static-query>
<script>
  import Footer from '~/components/footer.vue'
  export default {
    components: {
      Footer,
    },
    data: () => ({
      drawer: false,
    }),
  }
</script>
