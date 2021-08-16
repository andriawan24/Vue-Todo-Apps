<template>
  <div id="app">
    <div class="container">
      <div class="row header mb-5 p-3">
        <div class="col-lg-12">
          <h2>What am I gonna do today</h2>
        </div>
      </div>
      <div class="row content">
        <div class="col-lg-12">
          <div class="pekerjaan-rumah">
            <div class="row text-start">
              <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="tugas mb-3 col-lg-12">
                <ItemTugas v-bind:tugasSaya="tugasSaya" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import "bootstrap/dist/css/bootstrap.css"

import ItemTugas from './components/ItemTugas.vue'

export default {
  name: 'App',
  data: function() {
    return {
      tugas: [
        {
          id: 1,
          namaTugas: "Menyapu Rumah",
          isDone: false,
        },
        {
          id: 2,
          namaTugas: "Ngoding Android",
          isDone: false,
        },
        {
          id: 3,
          namaTugas: "Beli SSD",
          isDone: false,
        },
        {
          id: 4,
          namaTugas: "Makan Bakso",
          isDone: false,
        }
      ]
    }
  },
  components: {
    ItemTugas
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.header {
  background: #1ABC9C;
}

.header h2 {
  margin: 0;
}

.tugas .item {
  font-size: 20px;
}

.item-completed {
  color: #1ABC9C;
}
</style>
