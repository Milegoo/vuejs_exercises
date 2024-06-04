<script>
export default{
    data() {
        return {
            bgColor: 'white',
        }
    },

    methods: {
        toggleColor() {
            (this.bgColor == 'white') ? this.bgColor = 'red' : this.bgColor = 'white'
        }
    },

    computed: {
        inputStyle() {
            return `background-color: ${this.bgColor}`
        }
    }

}
</script>
<template>
    <div>
        <input @keydown="toggleColor" @keyup="toggleColor" type="text" :style="inputStyle"/>
    </div>
</template>
<style>
</style>