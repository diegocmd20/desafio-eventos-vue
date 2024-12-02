<template>
    <div class="container my-1">
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
        <button type="submit">Eliminar</button>
    </div>
</template>

<script>
export default {
    name: 'AgregarDatos',
    props: {
        paciente: String,
        fecha: Date,
        hora: Date,
        gravedad: String,
        motivo: String,
    }
};
</script>

<style scoped></style>