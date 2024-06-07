<script>
import DoubleCheckbox from './components/DoubleCheckbox.vue'
export default {

    components: {
        DoubleCheckbox
    },

    data() {
        return {
            parentCheckboxIsClicked: false,
            bothAreClicked: false,
            bothAreUnclicked: false,
        }
    },

    methods: {
        handleParentClick() {
            this.parentCheckboxIsClicked = !this.parentCheckboxIsClicked
            if(this.parentCheckboxIsClicked) {
                this.bothAreClicked = true
                this.bothAreUnclicked = false
            }
            else {
                this.bothAreClicked = false
                this.bothAreUnclicked = true
            }
        }
    }

}
</script>
<template> 
    <div>
        <input type="checkbox" @click="handleParentClick()" :checked="parentCheckboxIsClicked">
    </div>
    <DoubleCheckbox v-model:parentCheckboxIsClicked="parentCheckboxIsClicked"
                    v-model:bothAreClicked="bothAreClicked"
                    v-model:bothAreUnclicked="bothAreUnclicked"/>

</template>
<style></style>