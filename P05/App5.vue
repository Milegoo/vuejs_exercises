<script>
export default{
    data() {
        return {
            text: '',
        }
    },

    methods: {
        clearText() {
            if (this.text.length >= 5) {
                this.text = ''
            }
        }
    },

    watch: {
        text() {
            this.clearText()
        }

    }
}
</script>
<template>
    <div>
        <input type="text" v-model="text"/>
    </div>

</template>
<style>
</style>