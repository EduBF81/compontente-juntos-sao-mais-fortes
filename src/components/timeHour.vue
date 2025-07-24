<template>
    <div class="time-component">
        <span class="hour">{{ hours }}</span>:
        <span class="minute">{{ minutes }}</span>:
        <span class="second">{{ seconds }}</span>
    </div>
</template>

<script>
export default {
    name: 'TimeHour',
    data() {
        return {
            hours: '00',
            minutes: '00',
            seconds: '00'
        }
    },
    mounted() {
        this.updateTime()
        setInterval(this.updateTime, 1000)
    },
    methods: {
        updateTime() {
            const now = new Date()
            this.hours = String(now.getHours()).padStart(2, '0')
            this.minutes = String(now.getMinutes()).padStart(2, '0')
            this.seconds = String(now.getSeconds()).padStart(2, '0')
        }
    }
}
</script>

<style scoped>
.time-component {
    font-size: 1.5em;
    font-family: monospace;
}

.hour, .minute, .second {
    font-weight: bold;
}
</style>