<template>
    <div class="w-full shadow p-6">
        <div class="overflow-x-auto relative">
            <table class="w-full text-sm text-left text-gray-500 dark:text-gray-400">
                <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
                    <tr>
                        <th scope="col" class="py-3 px-6">
                            Order
                        </th>
                        <th scope="col" class="py-3 px-6">
                            Category
                        </th>
                        <th scope="col" class="py-3 px-6">
                            Order date
                        </th>
                        <th scope="col" class="py-3 px-6" align="right">
                            Actions
                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="order in orders" :key="order.id"
                        class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
                        <th scope="row" class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap dark:text-white">
                            {{ order.name }}
                        </th>
                        <td class="py-4 px-6">
                            {{ order.category }}
                        </td>
                        <td class="py-4 px-6">
                            {{ order.orderDate }}
                        </td>
                        <td class="py-4 px-6" align="right">
                            <button type="button" @click="checkStatus(order)"
                                class="py-2 px-3 text-xs font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Check
                                Status</button>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>

<script>
export default {
    name: "OrdersTable",
    props: {
        orders: {
            type: Array,
            required: true
        }
    },
    emits: ["check-status"],
    methods: {
        checkStatus(order) {
            // emit an event to check the status of the order
            this.$emit("check-status", order);
        }
    }
}
</script>

<style>
</style>