<template>
<div>
  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames">{{name}}
</div>
</template>

<script>
export default {
  name: "item",
  components: {
    /* "Declare" the component in the js of the parent*/
  },
  data() {
    return {
      name: ".",
    }

  }
};
</script>

<style>

</style>