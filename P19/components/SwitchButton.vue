<script>
export default {

    emits: ['off', 'on'],

    data() {
        return {
            onIsDisabled: false,
        }
    },

    methods: {
        manage() {
            if(!this.onIsDisabled) {
                this.$emit('off')
                this.onIsDisabled = true
            }
            else {
                this.$emit('on')
                this.onIsDisabled = false
            }
        }
    }

}
</script>

<template>
    <div style="border:solid;display:inline-block">
        <button @click="manage" :disabled="!onIsDisabled">ON</button>
        <button @click="manage" :disabled="onIsDisabled">OFF</button>
    </div>

</template>


<style></style>