<script>
export default {

    props: ['person'],

}
</script>

<template>
    <div class="card">
        <div>
            <img :src="person.picture">
        </div>
        <div>
            <h1>{{person.name}}</h1>
        </div>
        <div>{{person.email}}</div>
        <div>{{ person.phone }}</div>
    </div>

</template>
<style>
.card {
    font-family: Roboto;
    text-align: center;
    background: #ffbcbc;
    box-shadow: 6px 6px 8px #888;
    margin: 15px;
}

.card div {
    padding: 10px;
}

.card img {
    width: 100px;
}
</style>