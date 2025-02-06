<template>
  <div class="footer">
    <div class="date dateText">
      <div>6/2/2025</div>
      <div>Cairo, Egypt</div>
    </div>
    <div class="backlight"></div>
    <div>
      <q-btn class="download"> Download CV </q-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: 'sideFooter',
}
</script>

<style>
.footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 30px;
}
.date {
  display: flex;
  flex-direction: column;
  gap: 5px;
  border: 1px dashed #363232;
  border-radius: 10px;
  padding: 10px 30px;
  width: 200px;
  filter: blur(0.3px);
}
.dateText {
  font-size: 20px;
}
/* Backlight effect in the middle of the sidebar */
.backlight {
  position: absolute;
  top: 90%;
  left: 0;
  width: 100%;
  height: 100px;
  transform: translateY(-50%);
  background-color: #ff0000;
  filter: blur(800px); /* Adjust the blur to control glow softness */
  opacity: 0.3; /* Adjust opacity for a subtle effect */
  z-index: 0; /* Ensure the glow is behind other content */
}
.download {
  border: 1px dashed #363232;
  border-radius: 12px;
  padding: 10px 50px;
}
</style>
