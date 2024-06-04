<script>
export default{
    data() {
        return {
            clase: 'released'
        }
    },

}
</script>
<template>
    <div>
        <input @keydown="clase='pressed'" @keyup="clase='released'" type="text" :class="clase"/>
    </div>
</template>

<style>
input.pressed {
    background-color: red;
}

input.released {
    background-color: aqua;
}
</style>