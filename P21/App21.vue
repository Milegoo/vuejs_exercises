<script>
import ColorSelector1 from './components/ColorSelector1.vue'
export default {
    components: {
        ColorSelector1
    },

    data() {
        return {
            color: `rgb(0,0,0)`
        }
    }



}
</script>
<template>
    <div style="border:solid red; display:flex;">
        <ColorSelector1 v-model:color="color"/>
        <div :style="`color:${color}`">TEXT</div>
        <!-- Make sure the TEXT changes the color to the selected one-->
    </div>
</template>
<style></style>