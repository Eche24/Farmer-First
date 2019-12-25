<template>
  <v-app>
    <nav>
      <v-app-bar
        height="75px"
        scroll-off-screen
        app
        
      >
        <v-app-bar-nav-icon
          class="hidden-sm-and-up"
          @click.stop="drawer = !drawer"
        />
        
        <v-toolbar-title
          class="ml-2 pl-2"
          :to="$url('/')"
          title="Home"
        >
          <g-image src="@/assets/img/logo/logo3.png"  width="150vh" alt='farmer first logo' style="margin: 10px 0 0 0"/>
        </v-toolbar-title>
        <v-spacer />
        <v-toolbar-items
          class="hidden-xs-only"
          v-for="(item, i) in items"
          :key="i"
        >
         <v-btn-toggle
         class="pt-4"
          tile
          color="yellow accent-3"
          group
         
        >
          <v-btn
          
            text
            :to='item.link'
            style="text-transform: capitalize;"
            flat
            class="link"
            color=""
          >
            {{item.text}}
          </v-btn>
         </v-btn-toggle>
        </v-toolbar-items>
      </v-app-bar>
    
      <v-navigation-drawer
        v-model="drawer"
        temporary
        app
      >
        <v-list-item>
          <v-list-item-content>
            <v-list-item-title class="">
             <g-image src="@/assets/img/logo/logo3.png" width="100vh alt='farmer first logo' "/>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
          <v-list dense app >
      <v-list-item-group v-model="item" color="yellow accent-3">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to='item.link'
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"  class="link"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
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
      items:[
          { text: 'Home', icon: 'mdi-home',link:'/'},
          { text: 'About', icon: 'mdi-view-dashboard',link:'/about'},
            { text: 'Farms', icon: 'mdi-account',link:'/farms'},
            { text: 'Contact', icon: 'mdi-dialpad',link:'/contact'},
              
      ]
    }),
  }
</script>
<style scoped>
.link {
  color: green;
}
</style>