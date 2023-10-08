<script>
import TemplateRef from './components/template-ref.vue';
import { provide } from 'vue';

export default {
  name: 'App', 
  components: {
    TemplateRef
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
<TemplateRef firstName="Edwar" lastName="Macias"/>

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
