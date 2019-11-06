<template>
<div>
 <input type="text" placeholder="New todo" v-model="description" />
 <input type="date" placeholder="Date" v-model="date" />
 <button v-on:click="add">Add</button><br />
 <table>
 <tbody>
 <tr v-for="(todo, index) in todos"
v-bind:key="index"><td>{{todo.description}}</td><td>{{todo.date}}</td></tr>
 </tbody>
 </table>
 </div>
</template>

<script>
export default {
  name: 'TodoList',
  data(){
    return {
      todos:[ ]
      }
    }
  , 
  methods:{
    add: function (){
      this.todos.push({
        description:this.description,
        date:this.date});
     
    }
  }
}
</script>

<style>
  table {
    margin-left:auto; 
    margin-right:auto;
  }
</style>

