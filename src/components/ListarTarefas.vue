<template>
  <ul>
    <li
      v-for="(tarefa, index) in tarefas"
      :key="index"
      :class="{ removed: tarefa.checked }"
    >
     <input v-model="tarefa.checked" type="checkbox" />
     <label> {{ tarefa.titulo }} </label>
    </li>
 </ul>
</template>

<script>
export default {
    props: {
        tarefas: {
            type: Array,
            default: () => [{ titulo: "Atividade padrão", checked: false }],
        }
    }
};
</script>

<style>

</style>