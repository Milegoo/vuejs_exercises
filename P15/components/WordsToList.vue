<script>
export default {

    props: ['words'],

    data() {
        return {
            wordList: [],
        }
    },

    mounted() {
        this.wordList = this.words.trim().split(' ')
    }

}
</script>
<template>
    <ul >
        <li v-for="item in wordList">{{item}}</li>
    </ul>

</template>
<style></style>