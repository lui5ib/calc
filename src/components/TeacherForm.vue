<template>
    <h3> {{ inputText }}</h3>
    <section>
        <h3>Añadir Profesor</h3>
        <div><label for="">Nombre:</label><input type="text" v-model="teacher.teacherName"></div>
        <div><label for="">Apellido:</label><input type="text" v-model="teacher.surname"></div>
        <div><label for="">DNI:</label><input type="text" v-model="teacher.dni"></div>
        <div><label for="">Materias:</label><input type="text" v-model="subject"><button @click="handleSubject()">Agregar</button></div>
        <input type="checkbox" v-model="teacher.doc">Documentaciòn entregada.<button type="">Agregar</button>
        <br>
        <div>
            <ul>
                <li v-for="{materia, index} in teacher.subjects" :key="index" >{{ materia }}</li>
            </ul>
        </div>
    </section>

    <section>
        <h2>Listado de profesores</h2>
        
    </section>
</template>

<script setup>
    import { ref } from 'vue';
    let inputText = ref('Hello Mundo');

    let teacher = ref({
        teacherName: '',
        surname: '',
        dni: '',
        subjects: [],
        doc: false

    })
    
    let teachers = ref([])

    let subject = ref('')

    const handleSubject = () => {
        teacher.value.subjects.push(subject.value);
    }

</script>

<style scoped>

</style>