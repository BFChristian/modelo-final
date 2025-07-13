<template>
    <h1>Conversor de temperatura</h1>
    <label for="celcius">Ingrese Temperatura: °C </label>
    <input id="celcius" type="text" v-model.number="celcius" />
    <p :class="selectorDeColor(fahrenheit)">Conv Temperatura °F: {{ fahrenheit }}</p>
    <p :class="selectorDeColor(kelvin)">Conv Temperatura °K: {{ kelvin }}</p>
</template>

<script>

export default {
    name: 'Conversor',
    data() {
        return {
            celcius: 0,
        };
    },
    methods: {
        // Aquí puedes agregar métodos para manejar la lógica de conversión
        convertirCelciusAFahrenheit() {
            if (this.celcius !== 0) {
                return (this.celcius * 9 / 5) + 32;
            } else {
                return 0;
            }
        },
        convertirCelciusAKelvin() {
            if (this.celcius !== 0) {
                return parseFloat(this.celcius) + 273.15;
            } else {
                return 0;
            }
        },
        selectorDeColor(grados) {
            if (grados <= 0) return 'azul';
            if (grados < 15) return 'magenta';
            return 'rojo';
        }
    },
    computed: {
        // Aquí puedes agregar propiedades computadas si es necesario
        kelvin() {
            return this.convertirCelciusAKelvin();
        },
        fahrenheit() {
            return this.convertirCelciusAFahrenheit();
        }
    },
    mounted() {
        // Aquí puedes inicializar cualquier dato o realizar acciones al montar el componente
    }
}

</script>

<style scoped>
.azul {
    color: blue;
}

.magenta {
    color: magenta;
}

.rojo {
    color: red;
}
</style>
