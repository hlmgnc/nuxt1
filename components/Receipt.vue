<script>
export default {
  name: 'Receipt',
  props: ['receipt', 'idMeal'],
}
</script>
<template>
  <div class="receipt">
    <p>{{ receipt }}</p>
  </div>
</template>

<style scoped>
.receipt {
  padding: 2rem;
  border: 1px dotted #ccc;
  margin: 1rem 0;
}
</style>
