<script>
import Card from './components/Card.vue'
export default {
    components: {
        Card
    },
    data() {
        return {
            person: {
                name: 'My Name',
                picture: `data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAY
                        AAAAfFcSJAAAADUlEQVR42mM82Mz1HwAFqgJP3gasfwAAAABJRU5ErkJggg==`,
                email: 'me@somerandomdomain.com',
                phone: '+00 00 000 0000',
            }
        }
    },
}
</script>
<template>
    <div style="display:flex;">
        <Card :person="person"/>
    </div>


</template>
<style></style>