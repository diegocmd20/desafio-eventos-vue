<template>
    <div class="border border-secondary rounded border-1 py-1">
        <div class="d-flex align-items-center justify-content-center">
            
                <div class="d-flex flex-column my-1 mx-2">
                    <label for="paciente" class="form-label fst-semibold">Paciente</label>
                    <input name="paciente" type="text" class="form-control">
                </div>
                <div class="d-flex flex-column my-1 mx-2">
                    <label for="fecha" class="form-label fst-semibold">Fecha</label>
                    <input type="date" name="fecha">
                </div>
                <div class="d-flex flex-column my-1 mx-2">
                    <label for="hora" class="form-label fst-semibold">Hora</label>
                    <input type="time" name="hora">
                </div>
                <div class="d-flex flex-column my-1 mx-2">
                    <label for="gravedad" class="form-label">Gravedad</label>
                    <select name="gravedad">
                        <option value="" selected>Elige la gravedad</option>
                        <option value="bg-success">Baja</option>
                        <option value="bg-warning">Media</option>
                        <option value="bg-danger">Grave</option>
                    </select>
                </div>
                <div class="d-flex flex-column my-1 mx-2">
                    <label for="motivo">Motivo</label>
                    <input name="motivo" type="text" class="form-control">
                </div>

        </div>
        <button type="submit">Agregar</button>
    </div>
</template>

<script>
export default {
    name: 'Cita',
    data() {
        return {

        };
    },
    computed:{

    }
};
</script>

<style scoped></style>