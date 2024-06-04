<script>
import ColorSelector from './components/ColorSelector.vue'
export default {
    components: {
        ColorSelector
    },

    data() {
        return {
            color: `rgb(0,0,0)`
        }
    },

    methods: {
        handleColor(event) {
            this.color = event
        }
    }



}
</script>
<template>
    <div style="border:solid red; display:flex;">
        <ColorSelector @color="handleColor"/>
        <div :style="`color:${color}`">TEXT</div>
        <!-- Make sure the TEXT changes the color to the selected one-->
    </div>
</template>
<style></style>