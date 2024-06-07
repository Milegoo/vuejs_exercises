<script>
import MagicInput from './components/MagicInput.vue'
export default {
    components: {
        MagicInput
    },

    data() {
        return {
            buffer: '',
            reversedBuffer: '',
        }
    },

    watch: {

        buffer: function () {
            this.reversedBuffer = this.buffer.replace(/./g, x => x.toUpperCase() == x ? x.toLowerCase() : x.toUpperCase())
        }

    }



}
</script>
<template>
    <MagicInput v-model:buffer="buffer" v-model:reversedBuffer="reversedBuffer"/>
    <input type="text" v-model="buffer" /><span>{{ buffer }}</span>

</template>
<style></style>