<script>
import ScriptSetup from './components/script-setup.vue';
import { provide } from 'vue';

export default {
  name: 'App', 
  components: {
    ScriptSetup
},
setup() {
  provide("username", "EdwMacias");
},

  data() {
    return {
      
    }
  },

}
</script>

<template>
<div>
<ScriptSetup />

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
