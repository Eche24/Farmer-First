<template>
    <v-container fluid >
          <v-layout wrap align-center justify-center row fill-height class="my-0 py-0">
        <v-flex xs12 md10 sm10 lg10 class="py-0 my-0">
          <p class="google-font" style="font-size:130%; color:#868e96;" > Follow Us:
            <span v-for="(item,i) in ChapterDetails.socialLinks" :key="i">
              <v-tooltip top>
                  <v-btn flat icon :href="item.link" target="_blank" slot="activator" class="btn">
                    <v-icon>{{item.icon}}</v-icon>
                  </v-btn>
                  <span>{{item.name}}</span>
              </v-tooltip>
            </span>
          </p>
          <v-divider></v-divider>
        </v-flex>
      </v-layout>
    </v-container>
</template>
<script>
  import ChapterDetails from '@/assets/data/chapterDetails.json'
  export default {
    data() {
      return {
        ChapterDetails:ChapterDetails,
      }
    },
  }
</script>
<style>
.btn:hover {
  background-color:green;
}
</style>
