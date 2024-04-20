<template>
<section class="form">
    <h3>Añadir profesores</h3>
    <div><label>Nombre:</label><input type="text"/></div>
    <div><label>Apellidos:</label><input type="text"/></div>
    <div><label>DNI / NIF:</label><input type="text"/></div>
    <div><label>Materias:</label><input type="text"/> <button>Agregar</button></div>
    <div><input type="checkbox"/> Dcumentacion entregada</div>
    <button>Agregar</button>
</section>
<section>Listado de  Profesores</section>
</template>

<script lang="ts" setup>
import {Ref, ref} from 'vue';

interface ITeacher {
    teacherName: string,
    surname: string,
    dni: string,
    subjects: Array<string>,
    doc:boolean
}

let teacher:Ref<ITeacher> = ref({
    teacherName: '',
    surname: '',
    dni: '',
    subjects: [],
    doc: false
})

let teachers:Ref<Array<ITeacher>> = ref([])
</script>

<style scoped>
.form input{
    margin-top: 10px;
    margin-left:5px;
    margin-bottom: 4px;

}
</style>
