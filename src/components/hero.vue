<template>
  <v-carousel hide-delimiters cycle :show-arrows="false">
    <v-carousel-item v-for="(item,i) in items" :key="i" :src="item.src">
      <v-row class="fill-height overlay hidden-xs-only" align="center" justify="center">
        <v-col class="text-center white--text pt-5" cols="12" style="margin-top:10%;">
          <h4
            class="textover"
            style=" font-family: 'Roboto', sans-serif; font-size:150%; font-weight: 900; font-style:italic"
          >...building communities through smallholder farmers</h4>
          <h1
            class="text-capitalize textover"
            style="font-size:190%; font-family: 'roboto', sans-serif;"
          >lets walk you through a value-based agric-investment experience</h1>
        </v-col>
      </v-row>
    </v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          src:
            "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597610375/farmer%20first/farmer-first-1_ispubh.jpg",
        },
        {
          src:
            "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597610701/farmer%20first/DSCN9688_pmemvq.jpg",
        },

        {
          src:
            "https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597609965/farmer%20first/farmerfirst-soyabean_n02x5q.jpg",
        },
      ],
      cycle: true,
    };
  },
};
</script>
<style scoped>
.overlay {
  /* opacity: 1;
      background: rgba(129, 199, 132, 0.47); */
}
.textover {
  line-height: 1.5em;
  text-shadow: 2px 2px 2px #000;
}
</style>