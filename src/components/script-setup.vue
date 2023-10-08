<template>
    <div>
    {{ fullName }}
    <div>Username:  {{ username }}</div>
    <button ref="btn">click!</button>
    </div>
    <p>Se explicaron las API de composition y de options, donde se enfoca en ver las diferencias
        pero no se entregan como tal una diferencia para el lado negativo, son maneras de trabajar,
        Por ejemplo cuando se quiere trabajar con muchas funciones pues el composition API es mucho mas
        facil de trabajar, pero el option API es mas para funciones basicas, de igual manera el acceso 
        a los datos para que se mantengan reactivos es importante, así que mejor verificar
        eso siempre.
    </p>
</template>
<script setup>
import {  toRefs, ref, computed, inject, watch } from 'vue';
const props = defineProps( {
        firstName: String,
        lastName: String,
    });

const { firstName, lastName} = toRefs(props);
const fullName = computed(() => {
    return `${firstName.value} ${lastName.value}`;
});
const username = inject("username");
defineExpose({ 
    fullName
});
const btn = ref(null);
console.log(btn.value);
watch(() => btn.value, (valor) => {
    console.log(valor);
});
</script>