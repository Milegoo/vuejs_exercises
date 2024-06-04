<script>
export default{

    data() {
        return {
            a: false,
            b: false,
            c: false,
            d: false,
        }
    },

    watch: {
        a() {
            this.b = this.a
        },

        b() {
            this.c = this.b
        },

        c() {
            this.d = this.c
        }
    }

}
</script>
<template>
    <div>
        <input type="checkbox" v-model="a">{{ a }} {{ b }} {{ c }} {{ d }}
    </div>
</template>
<style>
</style>