<template>
  <button :class="mode">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: ['mode'],
};
</script>

<style scoped>
button {
  padding: 0.75rem 1.5rem;
  font-family: 'Open Sans', sans-serif;
  font-weight: 600;
  background-color: #5d0399;
  border: 1px solid #3a0061;
  border-radius: 2rem;
  color: white;
  cursor: pointer;
}

button:hover,
button:active {
  background-color: #3a0061;
  border-color: #270041;
}

.flat {
  background-color: transparent;
  color: #3a0061;
  border: none;
  text-decoration: underline;
}

.flat:hover,
.flat:active {
  background-color: #edd2ff;
}
</style>
