<template>
  
  <div id="app">
    <h1>To Do List</h1>
    <task-list :tasks="tasks" />
    <input type="text" v-model="newTask" placeholder="Tambahkan kegiatan" />
    <button @click="addTask">Tambah</button>
        <button @click="cancelActivity(index)">Batalkan</button>
        
   
  </div>
</template>

<script>
import TaskList from './components/TaskList.vue';

export default {
  name: 'App',
  components: {
    TaskList
  },
  data() {
    return {
      tasks: [
        { id: 1, name: 'Belajar Vue.js' },
        { id: 2, name: 'Menulis kode' },
        { id: 3, name: 'Membuat proyek baru' }
      ],
      newTask: ''
    };
  },
  methods: {
    addTask() {
      if (this.newTask.trim() !== '') {
        this.tasks.push({ id: this.tasks.length + 1, name: this.newTask });
        this.newTask = '';
        cancelActivity(index) 
          this.activities.splice(index, 1);
        
      }
    }
  }
};
</script>
