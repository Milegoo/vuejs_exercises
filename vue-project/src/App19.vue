<script>
import SwitchButton from './components/SwitchButton.vue'
export default{
    components: {
        SwitchButton
    },

    data() {
        return {
            state: '',
        }
    }

}
</script>
<template>
    <SwitchButton @on="state = 'just turned on'" @off="state = 'just turned off'"/> {{ state }}
</template>
<style>
</style>