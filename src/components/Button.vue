<template>
  <button @click="onClick" :style="{ background: color }" class="btn">
    {{ text }}
  </button>
</template>

<script>
export default {
  props: ['text', 'color'],
  methods: {
    onClick() {
      console.log('clicked');
    }
  }
};
</script>
