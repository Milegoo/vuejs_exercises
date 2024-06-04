<script>
export default{
    data() {
        return {
            a: 0,
            b: 0,
        }
    },


}
</script>
<template>
    <div>
        <input type="number" v-model="a"/><input type="number" v-model="b"/> <span>{{ a+b }}</span>
        <!--Important type=number or it will be detected as string and 9+8 = 98 !!-->
    </div>
</template>
<style>
</style>