<template>
<div>
  <img v-bind:class="logo1" alt="Vue logo" src="./assets/logo2.svg">
  <HelloWorld msg="Login Page"/>

  <p> Doesn't have an account? </p>
  <button type="button" class="btn" @click="showModal">
      Sign Up!
  </button>

  <Modal
      v-show="isModalVisible"
      @close="closeModal"
    />
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Modal from './components/Modal.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    Modal,
  },
  data() {
    return {
      logo1: 'img1',
      isModalVisible: false,
    };
  },
  methods: {
      showModal() {
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
      }
    }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.img1 {
  width: 30%;
}

.btn {
  width: 30%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-bottom: 10px;
  background-color: #6c63ff;
  color: #fff;
}

.btn:hover {
  background-color: #4e48c0;
  cursor: pointer;
}
</style>
