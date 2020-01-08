<template>
  <div id="app" class="container">
    <div class="col-mb-4">
      <h2>{{ title }}</h2> <!-- {{ double brackets make it possible to use the vue variables directly in html,
                                    here you use the title coming from the data section of this component (App.vue) -->
      <div class="footer">
        <hr />
          <AddItem></AddItem>
          <Items></Items>
        <!-- v-on directive that will process a custom event called onEnter (emitted by child component), if this event
        occurs, the parent will call the method changeTitle -->
        <list-title v-on:onEnter="changeTitle"></list-title> <!--use a specific tag which is your component name in kebab-case (list-title) -->
      </div>
    </div>
  </div>
</template>

<script>
/*import the file containing the component definition */
import ListTitle from "./components/ListTitle.vue";
import Items from "./components/Items.vue";
import AddItem from "./components/AddItem.vue";

export default {
  name: "app",
  components: {
    /* "Declare" the component in the js of the parent*/
    ListTitle,
    Items,
    AddItem,
  },
  data() {
    return {
      title: 'MyVueJS todo List', /* variable containing the title of the page */
    }
  },
  methods: {
    /* the method changeTitle, will change the title of the page when the onEnter event occurs */
    changeTitle(text){
      this.title = text;
    },
    sum(text) {
      this.item = text;
    }
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.col-mb-4 {
  width: 60%;
}
</style>
