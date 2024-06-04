<script>
export default{

    data() {
        return {
            state: 0 // 0 - green, 1 - yellow, 2 - red
        }
    },

    methods: {
        changeState() {
            this.state = ++this.state % 3
        }
    },

    computed: {
        greenClass() {
            return {greenOn: this.state == 0, greenOff: this.state != 0}
        }
    }


}
</script>

<template>

    <div class="trafficlight">
        <div class="light" :class="{redOn: state == 2, redOff: state != 2}"></div> <!--There can't be 2 attributes class, but v-bind allows us to do it.-->
        <div class="light" :class="{yellowOn: state == 1, yellowOff: state != 1}"></div>
        <div class="light" :class="greenClass"></div>
        <button @click="changeState">Switch</button>
    </div>

</template>



<style>

div.trafficlight{display: inline-block; width:30px;}
div.light{height: 30px;}
div.redOn{ background-color: red}
div.redOff{background-color: indianred}
div.yellowOn{background-color: yellow;}
div.yellowOff{background-color: khaki;}
div.greenOn{background-color: lime;}
div.greenOff{background-color: seagreen;}

</style>