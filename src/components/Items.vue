<template>
  <div>
    <ul>
      <Item v-for="item in todoitems" v-bind:key="item.id" v-bind:singleItem="item"> </Item>    
    </ul>
  </div>
</template>

<script>
const uuidv1 = require('uuid/v1');
import Item from "./Item.vue";

export default {
  name: "items",
  components: {
    /* "Declare" the component in the js of the parent*/
    Item,
  },
  data() {
    return {
      todoitems: [{
        id: 1, 
        text: "oui", 
        isChecked: false 
      },
      {
        id: 2, 
        text: "peut-être", 
        isChecked: false 
      }]
    }
  },
  methods: {
    addItem(itemText){
      this.todoitems.push({
        id: uuidv1(), 
        text: itemText, 
        isChecked: false 
        });
    }
  }
}
</script>

<style scoped>

</style>