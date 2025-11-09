<template>
    <vue-countdown 
    :time="time" 
    :interval="1000" 
    v-slot="{ days, hours, minutes, seconds }"
    >
    <div class="flex flex-row justify-center space-x-2 text-[12px] font-base-wedding font-bold">
        <div class="day">
            <h1 class="text-[20px]">{{ days }}</h1>
            <span>HARI</span>
        </div>
        <div class="hours">
            <h1 class="text-[20px]">{{ hours }}</h1>
            <span>JAM</span>
        </div>
        <div class="minutes">
            <h1 class="text-[20px]">{{ minutes }}</h1>
            <span>MENIT</span>
        </div>
        <div class="seconds">
            <h1 class="text-[20px]">{{ seconds }}</h1>
            <span>DETIK</span>
        </div>
    </div>
    </vue-countdown>
</template>

<script>
export default {
    name: 'Countdown',

    data() {
        const now = new Date();
        const newYear = new Date(now.getFullYear(), 11, 1);

        return {
            time: newYear - now,
        }
    }
}
</script>