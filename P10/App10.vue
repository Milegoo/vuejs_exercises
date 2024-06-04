<script>
export default{

    data() {
        return {
            a: false,
        }
    },

    computed: {
        b() {
            return this.a
        },

        c() {
            return this.b
        },

        d() {
            return this.c
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