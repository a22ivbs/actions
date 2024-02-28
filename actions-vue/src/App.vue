<script setup>
const numbers = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

const handleClick = (number) => {
  alert(`Has clicado el número: ${number}`)
}
</script>

<template>
  <div class="grid">
    <div v-for="(row, i) in numbers" :key="i" class="row">
      <button
        v-for="(number, j) in row"
        :key="j"
        @click="handleClick(number)"
        class="cell"
      >
        {{ number }}
      </button>
    </div>
  </div>
</template>

<style scoped>
.grid {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.row {
  display: flex;
}

.cell {
  width: 50px;
  height: 50px;
  margin: 5px;
  font-size: 20px;
}
</style>