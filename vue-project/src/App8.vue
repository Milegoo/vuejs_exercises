<script>
export default{

    data() {
        return {
            redness: 0,
        }
    },

    computed: {
        inputStyle() {
            return `color: hsl(0,${this.redness}%,50%)`
        }
    }

}
</script>
<template>
    <div>
        <div :style="inputStyle">AM I RED?</div>
        <input type="range" min="0" max="100" v-model="redness">
        <div v-if="redness >= 70">YES!</div>
    </div>
</template>
<style>
</style>