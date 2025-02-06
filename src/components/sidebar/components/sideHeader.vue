<template>
  <div class="headerContainer">
    <div>
      <q-avatar rounded>
        <img src="https://cdn.quasar.dev/img/avatar.png" />
      </q-avatar>
    </div>
    <!--Info-->
    <div class="info">
      <div>Mario Shafiek</div>
      <div>Software/Motion</div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.headerContainer {
  display: flex;
  gap: 20px;
  align-items: center;
}
.info {
  display: flex;
  flex-direction: column;
}
</style>
