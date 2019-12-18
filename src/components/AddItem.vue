<template>
<div>
  <input id="listItem" v-model="item" v-on: @keyup.enter="Validate" placeholder="add list item"/>
  <button @click="Validate" v-on:click="count++">Vous avez cliqué {{ count }} fois.</button>
</div>
</template>

<script>
export default {
  name: "AddItem",
  props: ['item'],
  data() {
    return {
      count: 0,
    }
  },
  methods: {

    Validate() {
      this.$emit('enter-btn', this.item);
      this.item = "";
    }
  }
}
</script>

<style scoped>

</style>