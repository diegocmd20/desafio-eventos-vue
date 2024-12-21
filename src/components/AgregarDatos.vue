<template>
    <div :class="['card', 'm-1', cambiarColor]" style="width: 12em;">
        <h6>Paciente</h6>
        <p>{{ paciente }}</p>
        <h6>Fecha</h6>
        <p>{{ fecha }}</p>
        <h6>Hora</h6>
        <p>{{ hora }}</p>
        <h6>Gravedad</h6>
        <p>{{ gravedad }}</p>
        <h6>Motivo</h6>
        <p>{{ motivo }}</p>
        <button @click="eliminarTarjeta" type="submit">Eliminar</button>
    </div>
</template>

<script>
export default {
    name: 'AgregarDatos',
    props: {
        paciente: String,
        fecha: [String, Date],
        hora: [String, Date],
        gravedad: String,
        motivo: String,
    },
    computed: {
        cambiarColor() {
            if (this.gravedad === 'Baja') {
                return 'bg-success';
            } else if (this.gravedad === 'Media') {
                return 'bg-warning';
            } else if (this.gravedad === 'Grave') {
                return 'bg-danger';
            } else {
                return 'bg-dark';
            }
        },
        eliminarTarjeta(){
            this.$emit('eliminar');
        }
    }
};
</script>

<style scoped>

</style>