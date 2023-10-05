<script>
import WatcherMain from './components/watcher-main.vue';
export default {
  name: 'App', 
  components: {
    WatcherMain,
  },
  data() {
    return {
      
    }
  },

}
</script>

<template>
<div>
<WatcherMain/>
</div>
</template>

<style scoped>

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
