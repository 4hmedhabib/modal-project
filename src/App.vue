<template>
  <h1>Welcome My First App Vuejs</h1>
  <p>Welcome...</p>
  <div v-if="showModal">
    <Modal theme='' @close='toggleModal'>
      <template v-slot:links>
        <a href="#">Sign up</a>
        <a href="#">Show info</a>
      </template>
      <h1>The Modal Header</h1>
      <p>Modal view in vuejs crash course in ninja</p>
    </Modal>
  </div>
  <button @click="toggleModal">Show Modal</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal },
  data () {
    return {
      title: 'My First Vue App :)',
      header: 'The Modal Header',
      text: 'Modal view in vuejs crash course in ninja',
      showModal: false
    }
  },
  methods: {
    toggleModal () {
      this.showModal = !this.showModal
    }
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
</style>
