<template>
    <h1>Full Name : {{fullName}}</h1>
    <button type="button" @click="changeName()">변경</button>
</template>
<script>
export default {
    data() {
        return {
            firstName : "이름",
            lastName : "성",
            fullName : "",
        };
    },
    computed : {
        fullName() {
            this.firstName = tnis.lastName + " " + this.firstName;

        }
    },

    watch : {
        firstName() {
            this.firstName = tnis.lastName + " " + this.firstName;
        },
        lastName() {
            this.firstName = tnis.lastName + " " + this.firstName;
        }
    },
    methods : {
        changeName() {
            this.firstName = "(변경) 이름";
        }
    }
}
</script>