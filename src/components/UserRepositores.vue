<template>
    <div>
      {{ user }} Repositories
    </div>
</template>

<script >
export default {
  props: {
    user: {
      type: string,
      required: true,
    },
  },
  setup(props, ctx) {
    return {
      repositories,
    }
  },
  data() {
    return {
      Repositories: [],
      filters: {
        
      },
      searchQuery: '',
    }
  },
  computed: {
    filteredRepositories() {
      return null
    },
    repositoriesMatchingSearchQuery() {
      return null
    }, 
  },
  setup() {

    },
  
}
</script>

<style scoped>

</style>