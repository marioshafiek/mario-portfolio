<template>
  <!--Container-->
  <div class="container">
    <!--Header-->
    <div class="sideHeader">
      <side-header />
    </div>
    <!--Links-->
    <div class="links">
      <side-links :selected="selected" @changedSelected="changeSelected" />
    </div>
    <div class="backlight"></div>
    <div class="resourceSeperator">
      <!--Resources-->
      <div class="links">
        <side-resources :selected="selected" @changedSelected="changeSelected" />
      </div>
      <!--Seprator-->
      <div>
        <div>
          <hr class="dotted-separator" />
        </div>
      </div>
      <!--Footer-->
      <div>
        <side-footer />
      </div>
    </div>
  </div>
</template>

<script>
import sideHeader from './components/sideHeader.vue'
import sideLinks from './components/sideLinks.vue'
import sideResources from './components/sideResources.vue'
import sideFooter from './components/sideFooter.vue'
export default {
  name: 'SideBar',
  data() {
    return {
      selected: 1,
    }
  },
  components: {
    sideHeader,
    sideLinks,
    sideResources,
    sideFooter,
  },
  methods: {
    changeSelected(id) {
      this.selected = id
      console.log('HERE', id)
    },
  },
}
</script>

<style scoped>
.container {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 15px;
  color: #9d9d9e;
}
.sideHeader {
  padding: 25px;
}
.resourceSeperator {
  display: flex;
  flex-direction: column;
  gap: 20px;
}
.links {
  padding: 15px;
  display: flex;
  flex-direction: column;
  gap: 2px;
}
.dotted-separator {
  margin: 0px;
  border: none;
  border-top: 1px dashed #363333; /* Adjust color and thickness as needed */
  filter: blur(0.5px);
  transform: translateY(-100%);
}
/* Backlight effect in the middle of the sidebar */
.backlight {
  position: absolute;
  top: 70%; /* Adjust vertical position as needed */
  left: 0;
  width: 100%;
  height: 400px; /* Height of the glow area; adjust as needed */
  transform: translateY(-100%);
  background-color: #ff0000; /* Change to your desired glow color */
  filter: blur(900px); /* Adjust the blur to control glow softness */
  opacity: 0.1; /* Adjust opacity for a subtle effect */
  z-index: -1;
}
</style>
