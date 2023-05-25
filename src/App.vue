<template>
  <section>
    <h3>Add teacher</h3>
    <form action="">
      <div><label for="">Nombre:</label><input type="text"></div>
      <div><label for="">Apellido</label><input type="text"></div>
      <div><label for="">DNI</label><input type="text"></div>
      <div><label for="">Materias</label><input type="text"><button>Add materias</button></div>
      <div><label for="">Docs </label><input type="checkbox"></div>
      <button mat-button>Add teacher</button>

    </form>

  </section>

  <section>
<h3>teacher list</h3>
  </section>
</template>

<script lang="ts" setup>
import { Ref, ref  } from "vue";

interface ITeacher{
  teacherName: string,
  surname: string,
  dni: string,
  subjects: Array<string>,
  doc: boolean

}

let teacher:Ref<ITeacher> = ref({
  teacherName: '',
  surname: '',
  dni: '',
  subjects: [],
  doc: false
})

let teachers:Ref<Array<ITeacher>> = ref([])

let subject:Ref<string> = ref('')
</script>

<!-- ESTRUCTURA EN JS
<script lang="ts" setup>
import { ref  } from "vue";

let teacher = ref({
  teacherName: '',
  surname: '',
  dni: '',
  subjects: [],
  docs: false
})
</script> -->

<style>

</style>
