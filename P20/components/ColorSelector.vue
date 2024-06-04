<script>
export default {

    emits: ['color'],

    data() {
        return {
            redColor: 0,
            greenColor: 0,
            blueColor: 0,
        }
    },

    computed: {
        rgbColor() {
            return `rgb(${this.redColor},${this.greenColor},${this.blueColor})`

        }
    },

    watch: {
        redColor(newValue) {
            this.$emit('color', this.rgbColor)
        },
        greenColor(newValue) {
            this.$emit('color', this.rgbColor)
        },
        blueColor(newValue) {
            this.$emit('color', this.rgbColor)
        },
    }

}
</script>
<template>
    <div style="border:solid; display:flex;">
        <div :style="`background-color: ${rgbColor}; width:110px; height:110px;`"></div>
        <div style="display:flex; flex-direction:column; padding:10px;">
            <div>R: <input type="range" min=0 max=255 v-model="redColor"> red value</div>
            <div>G: <input type="range" min=0 max=255 v-model="greenColor"> green value</div>
            <div>B: <input type="range" min=0 max=255 v-model="blueColor"> blue value</div>
        </div>
    </div>
</template>
<style></style>