<script>
export default{

    props: ['buffer', 'reversedBuffer'],
    emits: ['update:buffer', 'update:reversedBuffer'],

    data() {
        return {
            changedText: '',
        }
    },

    watch: {

        buffer: function() {
            this.changedText = this.buffer.replace(/./g,x => x.toUpperCase() == x ? x.toLowerCase() : x.toUpperCase())
        },

        reversedBuffer: function() {
            this.changedText = this.reversedBuffer
        },

        changedText: function(newValue) {
            this.$emit('update:reversedBuffer', newValue)
            let newBuffer = this.changedText.replace(/./g,x => x.toUpperCase() == x ? x.toLowerCase() : x.toUpperCase())
            this.$emit('update:buffer', newBuffer)
        }

    }


}
</script>
<template>
    <input type="text" v-model="changedText"/>
</template>
<style>
</style>