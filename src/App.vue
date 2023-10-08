<script>
import ProvideInject from './components/provide-inject.vue';
import { provide } from 'vue';

export default {
  name: 'App', 
  components: {
    ProvideInject
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
<ProvideInject firstName="Edwar" lastName="Macias"/>

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
