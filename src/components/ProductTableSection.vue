<template> 
    <div v-if="product.table" class="container"> 
        <h5 class="mb-4">Physico-chemical properties:</h5>
        <table class="table table-striped mb-5">
            <thead class="table-secondary">
                <tr>
                    <th v-for="(head, index) in product.table.tableHead" :key="index">{{ head }}</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(flight, index) in product.table.tableData" :key="index">
                    <td>{{ index + 1 }}</td>
                    <td>{{ flight.head }}</td>
                    <td>{{ flight.body }}</td>
                </tr>
            </tbody>
        </table>

    </div>
    <div v-else class="text-center">
        No reports at this moment.
    </div>
</template>

<script>
export default {
    props: {
        product: {
            type: Object,
            required: true,
        }
    },
};
</script>