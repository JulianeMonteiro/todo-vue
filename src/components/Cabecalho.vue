<script setup>
const props = defineProps(["tarefasPendentes"]);
</script>
<template>
  <header v-el class="p-5 mb-4 mt-4 bg-light rounded-3">
    <h1>Minhas tarefas</h1>
    <p v-if="props.tarefasPendentes == 1">
      Você possui {{ props.tarefasPendentes }} tarefa pendente
    </p>

    <p v-else-if="props.tarefasPendentes > 1">
      Você possui {{ props.tarefasPendentes }} tarefas pendentes
    </p>

    <p v-else>Parabéns! Você não possui tarefas pendentes!</p>
  </header>
</template>
