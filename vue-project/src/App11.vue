<script>
export default{

    data() {
        return {
            phonebook: [
                { name: 'Jaime Sommers', phone: '311-555-2368' },
                { name: 'Ghostbusters', phone: '555-2368' },
                { name: 'Mr. Plow', phone: '636-555-3226' },
                { name: 'Gene Parmesan: Private Eye', phone: '555-0113' },
                { name: 'The A-Team', phone: '555-6162' },
            ]
        }
    }

}
</script>
<template>
    <table>
        <tr>
            <th>Name</th>
            <th>Phone number</th>
        </tr>
        <tr v-for="item in phonebook">
            <td>{{ item.name }}</td>
            <td>{{ item.phone }}</td>
        </tr>
    </table>

</template>
<style>
table {
    border-collapse: collapse;
}

table th,
td {
    border: 1px solid black;
}
</style>