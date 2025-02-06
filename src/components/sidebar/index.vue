<template>
  <!--Container-->
  <div class="container">
    <!--Header-->
    <div>Header</div>
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
export default {
  name: 'SideBar',
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
