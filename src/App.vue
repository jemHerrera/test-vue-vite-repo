<script setup>
  import { ref, computed } from 'vue'
  import Home from './components/views/Home.vue'
  import NewPost from './components/views/NewPost.vue'

  const routes = {
    '/': Home,
    '/new-post': NewPost
  }

  const currentPath = ref(window.location.hash);

  window.addEventListener('hashchange', () => {
    currentPath.value = window.location.hash;
  })

  const currentView = computed(() => {
    return routes[currentPath.value.slice(1) || '/']
  })
</script>

<template>
  <component :is="currerntView"></component>
</template>

<style lang="scss">
@use './styles/abstracts' as *;
@use './styles/resets.scss';


</style>
