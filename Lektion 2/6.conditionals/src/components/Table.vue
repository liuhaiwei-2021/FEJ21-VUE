<template>
    <table class="table" v-if="data.length > 0">
        <thead>
        <tr>
            <th scope="col">#</th>
            <th scope="col">Firstname</th>
            <th scope="col">Lastname</th>
            <th scope="col">Email address</th>
        </tr>
        </thead>
        <tbody>
            <TableRow v-for="user in data" :key="user.id" id="1" firstName="Hans" lastName="Mattin-Lassei" email="hans@mattin-lassei.com" />
        </tbody>
    </table>
    <div v-else>
        Ingen data finns.
    </div>

</template>

<script>
import TableRow from './TableRow'

export default {
    components: {
        TableRow
    },
    data() {
        return {
            data: [
                { id: 1, firstName: 'Hans', lastName: 'Mattin-Lassei', email: 'hans@domain.com' },
                { id: 1, firstName: 'Tommy', lastName: 'Mattin-Lassei', email: 'tommy@domain.com' },
                { id: 1, firstName: 'Joakim', lastName: 'Wahlström', email: 'joakim@domain.com' },
            ]
        }
    }
};
</script>

<style>
</style>