<template>
  <section fill-height text-center>
    <cabecalho :valor="titulo" />
    <div class="container">
      <adicionar-tarefa v-on:adicionarTarefa="adicionarTarefa" />
      <listar-tarefas :tarefas="tarefas" />
      <footer>
        <em> Altere sua lista de tarefas </em>
        <entrada-dados type="text" v-model="titulo" />
      </footer>
    </div>
    <rodape />
  </section>
</template>

<script>
import Cabecalho from "@/components/Cabecalho";
import Rodape from "@/components/Rodape";
import ListarTarefas from "@/components/ListarTarefas.vue";
import AdicionarTarefa from "@/components/AdicionarTarefa.vue";
import EntradaDados from "@/components/templates/EntradaDados";

export default {
  name: "App",
  components: {
    Cabecalho,
    Rodape,
    ListarTarefas,
    AdicionarTarefa,
    EntradaDados,
  },
  data() {
    return {
      titulo: "Minha Lista de Tarefas",
      tarefas: [
        { titulo: "Estudar", checked: false },
        { titulo: "Programar", checked: true },
      ],
    };
  },
  methods: {
    adicionarTarefa(novaTarefa) {
      this.tarefas.push({
        titulo: novaTarefa,
        checked: false,
      });
    },
  },
};
</script>

<style>
.container {
  width: 40%;
  margin: 20px auto 0px auto;
  margin: 50px;
  margin-left: auto;
  margin-right: 300px;
}

ul li {
  list-style: none;
}

.removed {
  color: purple;
}

.removed label {
  text-decoration: line-through;
}
</style>