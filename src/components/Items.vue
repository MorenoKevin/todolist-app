<template>
  <div>
    <ul>
      <Item>

      </Item>
    </ul>
  </div>
</template>

<script>
import Item from "./Item.vue";

export default {
  name: "items",
  components: {
    /* "Declare" the component in the js of the parent*/
    Item,
  }
}
</script>

<style scoped>

</style>