<template>
  <q-layout view="lHh lpR lFf">
    <q-drawer
      v-model="leftDrawerOpen"
      side="left"
      overlay
      behavior="desktop"
      bordered
      class="drawer"
    >
      <side-bar />
    </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import SideBar from '../components/sidebar/index.vue'
export default {
  data() {
    return {
      leftDrawerOpen: true,
    }
  },
  components: {
    SideBar,
  },
  methods: {
    toggleLeftDrawer() {
      this.leftDrawerOpen = !this.leftDrawerOpen
    },
  },
}
</script>

<style>
.drawer {
  background-color: #161617;
  border-right: 2px solid #282729;
}
.q-drawer--left.q-drawer--bordered {
  border: none;
}
</style>
