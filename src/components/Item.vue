<template>
<div>
  <label v-bind:class="{'striked' : singleItem.isChecked}"><input type="checkbox" v-model="singleItem.isChecked">{{ " "+ singleItem.text}}</label>
</div>
</template>

<script>
export default {
  name: "item",
  props: ['singleItem'],
  components: {
    /* "Declare" the component in the js of the parent*/
  },
};
</script>

<style>
.striked{
text-decoration: line-through;
}
</style>