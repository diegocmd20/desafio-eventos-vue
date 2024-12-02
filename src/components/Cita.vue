<template>
    <div class="border border-secondary rounded border-1 py-1">
        <div class="d-flex align-items-center justify-content-center">

            <div class="d-flex flex-column my-1 mx-2">
                <label for="paciente" class="form-label fst-semibold">Paciente</label>
                <input v-model="paciente" name="paciente" type="text" class="form-control" placeholder="Nombre del Paciente">
            </div>
            <div class="d-flex flex-column my-1 mx-2">
                <label for="fecha" class="form-label fst-semibold">Fecha</label>
                <input v-model="fecha" type="date" name="fecha">
            </div>
            <div class="d-flex flex-column my-1 mx-2">
                <label for="hora" class="form-label fst-semibold">Hora</label>
                <input v-model="hora" type="time" name="hora">
            </div>
            <div class="d-flex flex-column my-1 mx-2">
                <label for="gravedad" class="form-label">Gravedad</label>
                <select v-model="gravedad" name="gravedad">
                    <option value="" selected>Elige la gravedad</option>
                    <option value="bg-success">Baja</option>
                    <option value="bg-warning">Media</option>
                    <option value="bg-danger">Grave</option>
                </select>
            </div>
            <div class="d-flex flex-column my-1 mx-2">
                <label for="motivo">Motivo</label>
                <input v-model="motivo" name="motivo" type="text" class="form-control">
            </div>

        </div>
        <button type="submit">Agregar</button>
        <div>
            <AgregarDatos :paciente="paciente" :fecha="fecha" :hora="hora" :gravedad="gravedad" :motivo="motivo"/>
        </div>
    </div>
</template>

<script>
import AgregarDatos from './AgregarDatos.vue';
export default {
    name: 'Cita',
    data() {
        return {
            paciente: '',
            fecha: '',
            hora: '',
            gravedad: '',
            motivo:'',
        };
    },
    components: {
        AgregarDatos,
    },
    methods: {

    }
};
</script>

<style scoped></style>