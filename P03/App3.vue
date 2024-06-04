<script>
export default{
    data() {
        return {
            visible: true
        }
    }

}
</script>
<template>
    <div>
        <button @click="visible = false" v-if="visible">click me!</button>
    </div>

</template>
<style>
</style>