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
                    <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
                        <th scope="row" class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap dark:text-white">
                            Kuka 5 Axis Robotic Arm
                        </th>
                        <td class="py-4 px-6">
                            Machines
                        </td>
                        <td class="py-4 px-6">
                            22 Aug, 2022
                        </td>
                        <td class="py-4 px-6" align="right">
                            <button type="button"
                                class="py-2 px-3 text-xs font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Check
                                Status</button>
                        </td>
                    </tr>
                    <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
                        <th scope="row" class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap dark:text-white">
                            Audi A6 Left Steering Dashboard
                        </th>
                        <td class="py-4 px-6">
                            Machines
                        </td>
                        <td class="py-4 px-6">
                            18 Aug, 2022
                        </td>
                        <td class="py-4 px-6" align="right">
                            <button type="button"
                                class="py-2 px-3 text-xs font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Check
                                Status</button>
                        </td>
                    </tr>
                    <tr class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
                        <th scope="row" class="py-4 px-6 font-medium text-gray-900 whitespace-nowrap dark:text-white">
                            BMW Auto-Transmission Gear Kit
                        </th>
                        <td class="py-4 px-6">
                            Machines
                        </td>
                        <td class="py-4 px-6">
                            15 Aug, 2022
                        </td>
                        <td class="py-4 px-6" align="right">
                            <button type="button"
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
    name: "OrdersTable"
}
</script>

<style>
</style>