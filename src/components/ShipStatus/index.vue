<template>
    <div class="w-full p-6 relative flex flex-col justify-center items-center">
        <h4 class="font-normal w-full text-left mb-4">Order status:
            <span class="font-semibold">
                {{ order.name }}
            </span>
        </h4>
        <h4 class="font-normal w-full text-left mb-4">Expected Delivery:
            <span class="font-semibold">
                {{ order.expectedDeliveryDate }}
            </span>
        </h4>
        <div class="w-full flex justify-center items-center">
            <h3 class="font-sm font-normal">{{
                    order.shipFrom
            }}</h3>
            <div class="w-full mx-3 relative flex items-center">
                <hr class="w-full border-solid border-2 border-indigo-800 rounded-xl" />
                <div id="dot"
                    class="absolute mb-4 w-16 h-16 rounded-full flex justify-center items-center right-0 drop-shadow-md"
                    :style="{
                        right: orderStatus + '%'
                    }">
                    <div id="pulse-effect"></div>
                    <img src="../../assets/images/cargo-ship.svg" alt="">
                </div>
            </div>
            <h3 class="font-sm font-normal">{{ order.shipTo }}</h3>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ShipStatus',
    props: {
        'order': {
            type: Object,
        }
    },
    computed: {
        orderStatus: function () {
            // Calculate difference between orderDate and expectedDeliveryDate
            var orderDate = new Date(this.order.orderDate);
            var expectedDeliveryDate = new Date(this.order.expectedDeliveryDate);
            var difference = expectedDeliveryDate.getTime() - orderDate.getTime();
            var days = Math.floor(difference / (1000 * 3600 * 24));

            // Days left from today to expectedDeliveryDate
            var daysLeft = expectedDeliveryDate.getDate() - new Date().getDate();
            // If this days left, means this percentage is completed
            const percentageCompleted = ((days - daysLeft) / days) * 100;
            console.log(days, daysLeft, percentageCompleted);

            // return max 99%
            return Math.min(percentageCompleted, 96);
        }
    }
}
</script>

<style lang="scss">
#dot {
    transform: translateX(50%);
    border-radius: 50%;
    transition: right 1s ease-in-out;

    #pulse-effect {
        width: 10px;
        height: 10px;
        top: 44%;
        transform: scale(1);
        animation: pulse 2s infinite;
        position: absolute;
        left: 50%;
        transform: translate(-50%, -50%);
        border-radius: 50%;
    }
}

@keyframes pulse {
    0% {
        transform: scale(0.95);
        box-shadow: 0 0 0 0 rgb(51 217 178 / 70%);
    }

    70% {
        transform: scale(1);
        box-shadow: 0 0 0 20px rgb(51 217 178 / 0%);
    }

    100% {
        transform: scale(0.95);
        box-shadow: 0 0 0 0 rgb(51 217 178 / 0%);
    }
}
</style>