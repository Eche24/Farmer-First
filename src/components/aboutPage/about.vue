<template>
  <v-container fluid class="mt-2 mb-0">
      <v-layout wrap align-center justify-center row fill-height class="my-0">
        <v-flex xs12 md10 class="mb-0">
            <p class="text-uppercase text-center mb-0 mt-2" style="font-size:190%; color:#616161;">Farmer First</p>   
        </v-flex>
      </v-layout>
      <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10 class="">
          <Mission/>
        </v-flex>
      </v-layout>
       <v-layout wrap align-center justify-center row fill-height>
        <v-flex xs12 md10 class="">
          <Team/>
        </v-flex>
      </v-layout>
    </v-container>
  
</template>
<script>
import Mission from '~/components/aboutPage/mission.vue'
import Team from '~/components/aboutPage/team.vue'
export default {
      components :{
         Mission,
         Team
    },
}
</script>