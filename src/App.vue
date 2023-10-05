<script>
import WatcherMain from './components/watcher-main.vue';
import CompositionComputed from './components/composition-computed.vue';
import propsUse from './components/props-use.vue';
export default {
  name: 'App', 
  components: {
    WatcherMain, CompositionComputed, propsUse
},
  data() {
    return {
      
    }
  },

}
</script>

<template>
<div>

<!-- <WatcherMain/> -->
<CompositionComputed/>
<propsUse firstName="david" lastName="lopez"/>
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
