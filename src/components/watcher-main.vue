<template>
    <div>
     {{ obj.counter }} {{ contador }}
    </div>
</template>

<script >
import { reactive, watch, ref } from 'vue';
export default {
    setup() {
        const contador = ref(0);
        const obj = reactive({ counter: 0 });
        setInterval(() => {
            obj.counter++
        },500);
        setInterval(() => {
            contador.value++
        }, 500);
        watch(() => obj.counter, (valor, anterior) => {
            console.log(valor, anterior)
        }),
        watch(contador, (valor2, anterior2) => {
            console.log(valor2, anterior2)
        })
           return {
            obj, contador
        }
    },
};
</script>

<style >

</style>