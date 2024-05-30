<template>
  <NavBar :items="items"/>
</template>

<script>
import NavBar from "@/components/nav-bar.vue";

export default {
  name: 'App',
  components: {
    NavBar,
  },

  data() {
    return {
      items: [
        {
          container:false,
          navBg: {
            default:'#fff'
          },

          routes: [
            {name: 'Home', routeName: 'Home',},
            {name: 'About', routeName: 'About',},
            {name: 'Contact', routeName: 'Contact',},
          ]
        }
      ],

    }
  }
}
</script>

<style>
@import "styles/style.scss";
</style>
