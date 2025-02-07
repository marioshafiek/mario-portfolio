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
      <div class="backgroundPattern">
        <router-view />
      </div>
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
  border-right: 2px dashed #282729;
}
.q-drawer--left.q-drawer--bordered {
  border: none;
}
.backgroundPattern {
  background-color: #161617;
  opacity: 0.1;
  background-image: radial-gradient(white 0.1px, #161617 0.8px);
  background-size: 10px 10px;
}
.drawer-toggle {
  position: relative;
  top: 20px;
  left: 20px;
  z-index: 1000;
}
.btnDrawer {
  padding-left: 10px;
  padding-top: 10px;
}
</style>
