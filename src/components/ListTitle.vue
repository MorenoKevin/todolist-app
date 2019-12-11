<template>
<div>
    <div>
        <em>Set a title and press Enter</em> <!--This is the text that appears above the input -->
        <!--v-bind is a vue directive which links the javascript variables to the html
        for the input below, the value is coming from a js variable called title-->
        <input v-bind:value="title" v-on: @keyup.enter="onEnter"/>
        <!-- v-on is also a vue directive, that allows to set a behavior on a specific event-->
    </div>
</div>
</template>

<script>
export default {
    /*When children components want to have access to the parent's data,
    they must declare "props" on the component initialization
    The list title is set in this component, but the parent App.vue has to show the list title, this is why it's a prop
    */
    props: ['title'],
    methods: {
        /*this method is called when the Enter key is pressed inside the input (see v-on: on the input up)*/
        onEnter (event) {
            /* since the value of the list title is in the App.vue component (parent), we need to inform it that we want to change the title
            this is why we need to "send" the event to the parent with the $emit function */
            this.$emit('onEnter',event.target.value); /*param1 : event name, param2 : the value sent to the parent (here input value=new title)*/
            this.title = ""; /*reset the input after emitting the event */
        }
    }
}
</script>

<style scoped>

</style>