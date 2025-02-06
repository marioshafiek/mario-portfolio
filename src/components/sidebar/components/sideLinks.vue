<template>
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
  >
  </q-btn>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { id: 1, name: 'Home', icon: 'img:icons/Home.svg' },
        { id: 2, name: 'Projects', icon: 'img:icons/projects.svg' },
        { id: 3, name: 'Services', icon: 'img:icons/services.svg' },
        { id: 4, name: 'Contact', icon: 'img:icons/mail.svg' },
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
</style>
