<template>
  <div>
    <h1>Lista de tarefas!</h1>

    <button @click="() => (showList = !showList)">Ver a lista</button>

    <br />

    <ul v-if="showList">
      <li v-for="(task, index) in tasks" :key="index">
        {{ tasks[0].name }}

        <button>&times;</button>
      </li>
    </ul>
  </div>
</template>


<script>
export default {
  data: () => ({
    showList: false,
    tasks: [{ name: "Fazer o curso", isDone: false }],
  }),
};
</script>