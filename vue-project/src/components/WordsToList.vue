<script>
export default {

    props: ['words'],

    data() {
        return {
            wordList: [],
        }
    },

    computed: {
        wordList() {
            return this.words.trim().split(' ')
        }
    }
}

</script>
<template>
    <ul>
        <li v-for="item in wordList">{{item}}</li>
    </ul>

</template>
<style></style>