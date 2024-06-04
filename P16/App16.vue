<script>
import WordsToList from './components/WordsToList.vue'

export default{

    data() {
        return {
            words: '',
        }
    },

    components: {
        WordsToList
    },

}
</script>
<template>
    <input type="text" v-model="words">
    <WordsToList v-if="words != ''" :words="words" />
</template>
<style>
</style>