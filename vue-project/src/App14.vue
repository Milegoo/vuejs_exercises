<script>
export default {

    data() {
        return {
            state: 0, //0-> green, 1-> yellow, 2-> red
        }
    },

    computed: {
        red() {
            return `height: 30px; background-color: ${(this.state == 2) ? 'red': 'indianRed'}`
        },

        green() {
            return `height: 30px; background-color: ${(this.state == 0) ? 'green': 'seagreen'}`
        },

        yellow() {
            return `height: 30px; background-color: ${(this.state == 1) ? 'yellow': 'khaki'}`
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

    <div style="display: inline-block; width:30px;">
        <div :style="red"></div>
        <div :style="yellow"></div>
        <div :style="green"></div>
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
