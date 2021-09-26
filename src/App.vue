<template>
  <main class="container">
    <AddTask :tasks="tasks" :onAddNewTask="addTaskHandler" />
    <Tasks :tasks="tasks" />
  </main>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
</template>

<script>
import AddTask from './components/AddTask.vue';
import Tasks from './components/Tasks.vue';

export default {
  name: 'App',
  components: {
    AddTask,
    Tasks
  },
  data() {
    return {
      tasks: []
    };
  },
  methods: {
    formIsValid: taskText => taskText?.length > 0,
    addTaskHandler(event, inputValue) {
      event.preventDefault();

      if (this.formIsValid(inputValue)) {
        this.tasks.push({
          text: inputValue,
          date: new Date().toISOString(),
          done: false,
          id: Date.now()
        });
      }
    }
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid rgb(38, 38, 38);
  padding: 30px;
  border-radius: 5px;
}
</style>
