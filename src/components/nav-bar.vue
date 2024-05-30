
<template>
  <nav class="vue-nav" :style="{backgroundColor:navBg}">
    <div class="nav-body" :class="items.container ? 'container-fluid' : 'container'">
      <div class="vue-nav-brand">Logo</div>


      <ul class="vue-nav-list" v-for="item in items" :key="item.routes">
        <li v-for="each in item.routes" :key="each.name">
          <router-link :to="{name: each.routeName}" class="">
            {{ each.name }}
          </router-link>
        </li>
      </ul>

    </div>

  </nav>
</template>

<script>
export default {
  name: 'Nav-bar',
  props: {
    items: [],
    navBg:{
      type:String,
      default:'#fff',
    }

  },

  mounted() {
    this.items.forEach((v) =>{
      console.log(v.routes)
    })
  }
}

</script>
