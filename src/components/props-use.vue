<template>
    <div>
    Nombre completo: {{ fullName }}
    </div>
</template>

<script>
import { toRefs, computed} from 'vue';
export default {
    props: {
        firstName: String,
        lastName: String
    },
    setup(props) {
        const { firstName, lastName} = toRefs(props);
        // const firstName = ref('Edwar');
        // const lastName = ref('Macias');

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
