<template>
    {{ count }}
    <button type="button" @click="increment">
        증가
    </button>
</template>

<script>
export default {
computed : {
    count(){
        return this.$store.state.count;
    }
},
method
</script>
