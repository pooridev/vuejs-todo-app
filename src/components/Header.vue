<template>
  <header @click="logProp">
    <h1>
      {{ title }}
    </h1>
    <Button text="ADD TASK" color="green" />
  </header>
</template>

<script>
import Button from './Button.vue';

export default {
  name: 'Header',
  components: {
    Button
  },
  props: ['title'],
  methods: {}
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
