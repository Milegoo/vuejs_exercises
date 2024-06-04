<script>
import WordsToList from './components/WordsToList.vue'

export default{

    data() {
        return {
            words: '',
            isClicked: false,
        }
    },

    components: {
        WordsToList
    },

    methods: {
        manageClick() {
            if(!this.isClicked) {
                this.isClicked = true
            }

        }
    }

}
</script>
<template>
    <input type="text" v-model="words">
    <button @click="manageClick">Make list!</button>
    <WordsToList v-if="words != '' && isClicked" :words="words" />
</template>
<style>
</style>