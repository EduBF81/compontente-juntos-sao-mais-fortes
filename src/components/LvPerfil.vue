<template>
    <div>
        <h3>Time</h3>
        <p>Time: {{ nome }}</p>
        <p>Estadio: {{ estadio }}</p>
    </div>
</template>
<script>

export default {
    name: 'lv-perfil',
    data() {
        return {
            nome: 'Cruzeiro',
            estadio: 'Mineirão',

        }
    }
}

</script>


<style scoped>
.time-component {
    font-size: 1.5em;
    font-family: monospace;
}

.hour,
.minute,
.second {
    font-weight: bold;
}
</style>