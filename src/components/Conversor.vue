<template>
    <h1>Conversor de temperatura</h1>
    <label for="celcius">Ingrese Temperatura: °C </label>
    <input id="celcius" type="text" v-model="celcius" />
    <p for="">Conv Temperatura °F: </p>
    <p for="">Conv Temperatura °K: </p>
</template>

<script>

export default {
    name: 'Conversor',
    data() {
        return {
            celcius: '',
            fahrenheit: '',
            kelvin: ''
        };
    },
    methods: {
        // Aquí puedes agregar métodos para manejar la lógica de conversión

    },
    computed: {
        // Aquí puedes agregar propiedades computadas si es necesario
    },
    mounted() {
        // Aquí puedes inicializar cualquier dato o realizar acciones al montar el componente
    }
}

</script>

<style scoped></style>
