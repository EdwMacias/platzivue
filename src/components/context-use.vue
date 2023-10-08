<template>
    <div>
    {{ fullName }}
    </div>
</template>

<script>
import { toRefs, computed} from 'vue';

export default {
    props: {
        firstName: String,
        lastName: String,
    },
    setup(props, context) {
        console.log(context);
        const { firstName, lastName} = toRefs(props);

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
