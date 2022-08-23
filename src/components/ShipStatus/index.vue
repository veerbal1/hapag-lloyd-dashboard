<template>
    <div class="relative mt-8 flex flex-col justify-center items-center w-full">
        <h4 class="font-normal w-full text-left mb-4">Order status:
            <span class="font-semibold">
                Crankshaft CNC
            </span>
        </h4>
        <div class="w-full flex justify-center items-center">
            <h3 class="font-sm font-normal">Germany</h3>
            <div class="w-full mx-3 relative flex items-center">
                <hr class="w-full border-solid border-2 border-indigo-800 rounded-xl" />
                <div id="dot" class="absolute w-6 h-6 rounded-full right-0 transition-all"></div>
            </div>
            <h3 class="font-sm font-normal">India</h3>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ShipStatus'
}
</script>

<style>
#dot {
    transform: translateX(50%);
    background-color: rgb(163, 230, 53);
    box-shadow: 0 0 0 0 rgb(51 217 178);
    animation: pulse 2s infinite;
    transform: scale(1);
}

@keyframes pulse {
    0% {
        transform: scale(0.95);
        box-shadow: 0 0 0 0 rgb(51 217 178 / 70%);
    }

    70% {
        transform: scale(1);
        box-shadow: 0 0 0 10px rgb(51 217 178 / 0%);
    }

    100% {
        transform: scale(0.95);
        box-shadow: 0 0 0 0 rgb(51 217 178 / 0%);
    }
}
</style>