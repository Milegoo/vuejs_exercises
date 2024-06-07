<script>
export default {

    props: ['parentCheckboxIsClicked', 'bothAreClicked', 'bothAreUnclicked'],
    emits: ['update:parentCheckboxIsClicked', 'update:bothAreClicked', 'update:bothAreUnclicked' ],

    data() {

        return {
            checkboxs: [false]
        }


    },


    methods: {
        manageClick(checkboxId) {

            if (this.bothAreClicked) {
                console.log("aaa");
                this.checkboxs[checkboxId] = false
                this.$emit('update:bothAreClicked', false)
                this.$emit('update:parentCheckboxIsClicked', false)
            }
            else {
                if (this.checkboxs[checkboxId]) {
                    this.checkboxs[checkboxId] = false
                    this.$emit('update:bothAreUnclicked', true)
                }
                else {
                    if (this.checkboxs[(checkboxId + 1) % 2]) {
                        this.checkboxs[checkboxId] = true
                        this.$emit('update:bothAreClicked', true)
                        this.$emit('update:parentCheckboxIsClicked', true)
                        this.$emit('update:bothAreUnclicked', false)
                    }
                    else {
                        this.checkboxs[checkboxId] = true
                        this.$emit('update:bothAreUnclicked', false)

                    }

                }


            }
        }
    },

    watch: {
        bothAreClicked: function (newValue) {
            if (newValue) {
                this.checkboxs[0] = true
                this.checkboxs[1] = true
            }
        },

        parentCheckboxIsClicked: function (newValue) {
            if (newValue) {
                this.checkboxs[0] = true
                this.checkboxs[1] = true
            }

        },

        bothAreUnclicked: function(newValue) {
            if(newValue) {
                this.checkboxs[0] = false
                this.checkboxs[1] = false
            }
         

        }
    }


}
</script>
<template>
    <div>
        <input type="checkbox" @click="manageClick(0)" :checked="checkboxs[0]">
        <input type="checkbox" @click="manageClick(1)" :checked="checkboxs[1]">
    </div>

</template>
<style scoped>
div {
    display: inline-block;
    border: solid black;
}

div input {
    padding-left: 4px;
}
</style>