<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Enter to your account 
    </p>
    
    <form>
      <input v-model="value" type="text" placeholder="Enter your e-mail">
      <input v-model="value" type="text" placeholder="Enter your password">
    </form>
    <button>Submit</button> 
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Fuzzy+Bubbles:wght@700&display=swap');

h1 {
  font-family: 'Fuzzy Bubbles', cursive;
  font-size: 3em;
}
a {
  color: #6c63ff;
}

form {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
}

input {
  width: 50%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-bottom: 10px;
}

input:focus {
  outline: none;
}

button {
  width: 30%;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
  margin-bottom: 10px;
  background-color: #6c63ff;
  color: #fff;
}

button:hover {
  background-color: #4e48c0;
  cursor: pointer;
}
</style>
