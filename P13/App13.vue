<script>
export default {

    data() {
        return {
            state: 0, //0-> green, 1-> yellow, 2-> red
        }
    },

    computed: {
        green() {
            if(this.state == 0) {
                return `light greenOn`
            }
            else {
                return `light greenOff`
            }
        },

        red() {
            if(this.state == 2) {
                return `light redOn`
            }
            else {
                return `light redOff`
            }
        },

        yellow() {
            if(this.state == 1) {
                return `light yellowOn`
            }
            else {
                return `light yellowOff`
            }
        },

    },

    methods: {
        toggleLight() {
            if (this.state == 0) {
                this.state = 1
            }
            else if (this.state == 1) {
                this.state = 2
            }
            else if (this.state == 2) {
                this.state = 0
            }
        }
    }
}
</script>
<template>
    <div class="trafficlight">
        <div :class="red"></div>
        <div :class="yellow"></div>
        <div :class="green"></div>
        <button @click="toggleLight">Switch</button>
    </div>

</template>
<style>

div.trafficlight {
    display: inline-block;
    width: 30px;
}

div.light {
    height: 30px;
}

div.redOn {
    background-color: red
}

div.redOff {
    background-color: indianred
}

div.yellowOn {
    background-color: yellow;
}

div.yellowOff {
    background-color: khaki;
}

div.greenOn {
    background-color: lime;
}

div.greenOff {
    background-color: seagreen;
}
</style>
