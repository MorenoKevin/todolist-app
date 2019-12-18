<template>
  <div>
    <ul>
  <li><input type="checkbox" id=1 v-model="checkedNames">
  <label for="jack">Apprendre le JS</label></li>
  <li><input type="checkbox" id=2 v-model="checkedNames">
  <label for="john">Apprendre le Bash</label></li>
  <li><input type="checkbox" id=3 v-model="checkedNames">
  <label for="mike">Apprendre à lire</label></li>
  </ul>
  </div>
</template>

<script>
export default {
  name: "Item"
}
</script>

<style scoped>

</style>