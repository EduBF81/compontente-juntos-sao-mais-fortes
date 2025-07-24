<template>
    <div>
        <h3>Buscando Rivais</h3>
        <label>Time:</label>
        <input type="text" v-model="busca" placeholder="Digite o nome do time" />
        <p>Rival: {{ rival(busca) }}</p>

        <h3>Time</h3>
        <p>Time: {{ nome }}</p>
        <p>Estadio: {{ estadio }}</p>
    </div>
</template>
<script>

export default {
    name: 'LvTime',
    data() {
        return {
            nome: 'Cruzeiro',
            estadio: 'Mineirão',
            busca: '',

        }
    },
    methods: {
        rival(time) {
            // Aqui você pode implementar a lógica de busca
            // Por exemplo, usando um switch case para retornar o rival do time
            switch (time.toLowerCase()) {
                case 'corinthians':
                    return 'palmeiras'
                case 'santos':
                    return 'são Paulo'
                case 'flamengo':
                    return 'vasco'
                case 'cruzeiro':
                    return 'atlético mineiro'
                default:
                    return;
            }
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