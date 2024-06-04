<script>
export default{

    data() {
        return {
            counter: 0,
            interval: 0,
        }
    },

    mounted() {
        this.interval = setInterval(() => this.counter++, 100);
    },

    unmounted() {
        clearInterval(this.interval)
    }

}
</script>
<template>
    <span>{{ counter }}</span>
</template>
<style>
span {
        font-size: 230px;
        color: black;
}
</style>