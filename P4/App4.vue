<script>
export default{
    data() {
        return {
            disable: false
        }
    }

}
</script>
<template>
    <div>
        <button @click="disable = true" :disabled="disable">click me!</button>
    </div>

</template>
<style>
</style>