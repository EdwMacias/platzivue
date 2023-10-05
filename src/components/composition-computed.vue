<template>
    <div>
    Nombre completo: {{ fullName }}
    </div>
</template>

<script>
import { ref, computed} from 'vue';
export default {
    setup() {
        const firstName = ref('Edwar');
        const lastName = ref('Macias');

        const fullName = computed(() => {
            return `${firstName.value} ${lastName.value}`;
        });


        return {
            fullName
        }
    }
}
</script>

<style scoped>

</style>
