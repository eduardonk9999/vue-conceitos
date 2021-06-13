<template>
  <div>
    <h1>Lista de tarefas!</h1>

    <button @click="() => (showList = !showList)">Ver a lista</button>

    <br />

    <ul v-if="showList">
      <li v-for="(task, index) in tasks" 
        :key="index"
        @dblclick="complete(task)"
      >
        {{ tasks[0].name }}
        <button
          @click="remove(task)">&times;</button>
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
  methods: {
    complete (task) {
      this.tasks = this.task.map(t => {
        if (t.name === task.name) {
          return {...t, isDone: t.isDone}
        }
        return { ...t}
      })
    },
    remove(task){
      this.tasks = this.tasks.filter(t => t.name !== task.name)
      console.log('task', task)
    }
  },
};
</script>