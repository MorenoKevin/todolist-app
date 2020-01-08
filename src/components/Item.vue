<template>
  <div>
    <ul>
  <input type="checkbox" id=1 value=1 v-model="checkedNames">
  <label for=1>Apprendre le JS</label><br>
  <input type="checkbox" id=2 value=2 v-model="checkedNames">
  <label for=2>Apprendre le Bash</label><br>
  <input type="checkbox" id=3 value=3 v-model="checkedNames">
  <label for=3>Apprendre à lire</label>
  </ul>
  <br>
  <span>Noms cochés : {{ checkedNames }}</span>
  </div>
</template>

<script>
export default {
  name: "Item",
    data() {
      return {
      checkedNames: [],
      }
    }
}
</script>

<style scoped>

</style>