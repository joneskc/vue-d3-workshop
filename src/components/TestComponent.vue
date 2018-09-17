// example of reactivity

<template>

</template>

<script>
export default {
    data() {
        return {
            a: 1,
            b: 2,
            c: a + b
        }
    },
    computed: {
        c() {
            return this.a +this.b
        }
    }
}
</script>

<style>

</style>
