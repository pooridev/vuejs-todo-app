<template>
  <button class="btn">
    {{ text }}
  </button>
</template>

<script>
export default {
  props: ['text', 'color']
};
</script>

<style scoped>
.btn {
  display: inline-block;
  background: rgb(38, 38, 38);
  color: #fff;
  border: none;
  padding: 5px 10px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
  width: 25%;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}
</style>
