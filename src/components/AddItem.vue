<template>
<div class="input-group mb-3">
  <input type="text" class="form-control" id="listItem" v-model="item" placeholder="add list item"/>
  <div class="input-group-append">
    <button class="btn btn-outline-secondary" type="button" @click="clickBtn">Add!</button>
  </div>
</div>
</template>

<script>

export default {
  name: "AddItem",
  props: ['item'],
  methods: {
    clickBtn() {
      this.$emit('clickBtn', this.item);
      this.item = "";
    }
  }
}
</script>

<style scoped>

</style>