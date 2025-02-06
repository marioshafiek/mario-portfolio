<template>
  <div class="resourcesContainer">
    <div class="title">Resources</div>
    <div class="links">
      <q-btn
        v-for="link in links"
        :key="link.name"
        color="#9d9d9e"
        text-color="#9d9d9e"
        :icon="link.icon"
        flat
        size="11px"
        :label="link.name"
        class="btnLink"
        :class="link.id == selected ? 'btnLinkSelected' : ''"
        @click="changedSelected(link.id)"
      ></q-btn>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { id: 5, name: 'Bookmarks', icon: 'img:icons/bookmark.svg' },
        { id: 6, name: 'Stack', icon: 'img:icons/stack.svg' },
        { id: 7, name: 'Linkedin', icon: 'img:icons/linkedin.svg' },
      ],
    }
  },
  props: {
    selected: Number,
  },
  methods: {
    changedSelected(id) {
      console.log('Emitting event with id:', id)
      this.$emit('changed-selected', id)
    },
  },
}
</script>

<style>
.btnLink {
  width: 250px;
  height: 50px;
  align-items: start;
  background-color: none;
  border-radius: 16px;
}
.btnLinkSelected {
  background-color: #1c1c1f;
  border: 1px solid #252526;
}
.resourcesContainer {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
.title {
  padding-left: 10px;
  font-size: 16px;
}
.links {
  display: flex;
  flex-direction: column;
  gap: 2px;
}
</style>
