<template>
  <form @submit="event => onAddNewTask(event, inputValue)">
    <input v-model="inputValue" type="text" class="task-input" />
    <Button text="ADD TASK" />
  </form>
</template>

<script>
import Button from './Button.vue';

export default {
  name: 'AddTask',
  components: {
    Button
  },
  props: {
    tasks: { type: Array },
    onAddNewTask: { type: Function }
  }
};
</script>

<style scoped>
form {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.task-input {
  width: 75%;
  padding: 5px 10px;
  border: 0;
  border-bottom: 1px solid #ccc;
}

.task-input:focus {
  outline: 0;
}
</style>
