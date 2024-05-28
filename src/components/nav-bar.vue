
<template>
  <nav class="vue-nav" :style="{ background: items.navBg }">
    <div class="nav-body" :class="items.container ? 'container-fluid' : 'container'">
      <div class="vue-nav-brand">Logo</div>
      <div v-for="item in items" :key="item.routes">
        <ul class="vue-nav-list">
          <li v-for="each in item.routes" :key="each.name">
            <router-link :to="{name: each.routeName}" class="">
              {{ each.name }}
            </router-link>
          </li>
        </ul>
      </div>

    </div>

  </nav>
</template>

<script>
export default {
  name: 'Nav-bar',
  props: {
    items: [],

  },

  mounted() {
    this.items.forEach((v) =>{
      console.log(v.routes)
    })
  }
}

</script>
