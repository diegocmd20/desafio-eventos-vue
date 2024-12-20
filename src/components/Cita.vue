<template>
    <div class="border border-secondary rounded border-1 py-1">
        <div class="d-flex align-items-center justify-content-center">

            <div class="d-flex flex-column my-1 mx-2">
                <label for="paciente" class="form-label fst-semibold">Paciente</label>
                <input v-model="paciente" name="paciente" type="text" placeholder="Nombre del Paciente">
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
                    <option value="Baja">Baja</option>
                    <option value="Media">Media</option>
                    <option value="Grave">Grave</option>
                </select>
            </div>
            <div class="d-flex flex-column my-1 mx-2">
                <label for="motivo">Motivo</label>
                <input v-model="motivo" name="motivo" type="text" class="form-control">
            </div>

        </div>
        <button @click="agregarTarjeta" type="button">Agregar</button>
    </div>
    <div class="row">
        <div v-for="(tarjeta, index) in tarjetas" :key="index" class="col-12 col-md-3">
            <AgregarDatos :paciente="tarjeta.paciente" :fecha="tarjeta.fecha" :hora="tarjeta.hora"
                :gravedad="tarjeta.gravedad" :motivo="tarjeta.motivo" />
        </div>
    </div>

</template>

<script>
import AgregarDatos from './AgregarDatos.vue';
export default {
    name: 'Cita',
    data() {
        return {
            tarjetas: [],
            paciente: '',
            fecha: '',
            hora: '',
            gravedad: '',
            motivo: '',
        };
    },
    components: {
        AgregarDatos,
    },
    methods: {
        agregarTarjeta() {
            const nuevaTarjeta = {
                paciente: this.paciente,
                fecha: this.fecha,
                hora: this.hora,
                gravedad: this.gravedad,
                motivo: this.motivo,
            };

            this.tarjetas.push(nuevaTarjeta);

            this.paciente = '';
            this.fecha = '';
            this.hora = '';
            this.gravedad = '';
            this.motivo = '';
        },
    }
};
</script>

<style scoped></style>