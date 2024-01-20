<template>
   <div> <!-- Un seul élément racine ici -->
     <div v-for="task in tasks" :key="task.id">
       <Task @toggle-reminder="$emit('toggle-reminder',task.id)" @delete-task="$emit('delete-task',task.id)" :task="task"></Task>
     </div>
   </div>
 </template>
 
 <script>
import Task from './Task'
 export default {
   name: 'AppTasks',
   props: {
     tasks: Array
   },
   components:{
   Task
   },
   emits:['delete-task','toggle-reminder'],
 }
 </script>
 
 <style>
 /* Votre CSS ici */
 </style>