<template>
<div>
  <AddItem></AddItem>
  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
    <label for="mike">yolo</label>
</div>
</template>

<script>
export default {
  name: "item",
  components: {
    /* "Declare" the component in the js of the parent*/
    //AddItem,
  },
};
</script>

<style>

</style>