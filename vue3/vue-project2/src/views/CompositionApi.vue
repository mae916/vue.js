<template>
    <input type="number" v-model="state.num1" @keyup="calcu" /> +
    <input type="number" v-model="state.num2" @keyup="calcu" /> =
    {{state.result}}
</template>
<script>
import {reactive, computed, toRefs} from 'vue';
export default {
    setup() {
         let state = reactive({
             num1 : 0,
             num2 : 0,
             result : computed(() => {
                 return state.num1 + state.num2;
             }),
         });

function calcu() {
    state.result = state.num1 + state.num2;
}
         return {
             state,
             calcu,
         };  
    }
}
</script>
