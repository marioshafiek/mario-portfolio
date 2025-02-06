<template>
  <!--Container-->
  <div class="container">
    <!--Header-->
    <div>
      <side-header />
    </div>
    <!--Links-->
    <div>Links</div>

    <div class="resourceSeperator">
      <!--Resources-->
      <div>Resources</div>
      <!--Seprator-->
      <div>Seperator</div>
    </div>
    <!--Footer-->
    <div class="footer">
      <div>Date</div>
      <div>Download CV</div>
    </div>
  </div>
</template>

<script>
import sideHeader from './components/sideHeader.vue'
export default {
  name: 'SideBar',
  components: {
    sideHeader,
  },
}
</script>

<style scoped>
.container {
  padding: 25px;
  display: flex;
  flex-direction: column;
  gap: 36px;
}
.resourceSeperator {
  display: flex;
  flex-direction: column;
  gap: 242px;
}
.footer {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
</style>
