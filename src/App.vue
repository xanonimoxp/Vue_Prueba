<template>
<div>
  <div id="header"></div>
  <div id="maincontainer">
    <h2>Todos</h2>
    <Todos v-bind:todoslist="copyTodos" />
  </div>
</div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import Search from './components/Serch.vue';
import Todos from './components/Todo';
//import TodoApp from './components/Todoitem.vue';

export default {
  name: 'App',
  components: {
    Todos
  },
  data(){
    return {
      todos: [
        {
          id:0,
          title:'comprar',
          completed:false
        },
                {
          id:3,
          title:'chec',
          completed:false
        },
                {
          id:1,
          title:'cena',
          completed:true
        },
                {
          id:0,
          title:'xbox',
          completed:false
        }
      ],
      copyTodos: []
    }
  },
  created(){
    this.copyTodos=[...this.todos];
  }
}
</script>

<style>
 *{
    box-sizing: border-box;
  }
  body{
    font-family: Arial, Helvetica, sans-serif;
    font-size: 1.5em;
    padding: 0;
    margin: 0;
  }
  #main-container{
    border: solid 1px #ccc;
    width: 600px;
    margin: 100px auto;
  }
  #header{
    background: black;
    padding: 10px;
  }
  h2{
    padding: 0 10px;
  }
</style>
