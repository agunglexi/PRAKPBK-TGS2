<template>
  <div class="container">
    <h3>Secretary 1</h3>
    <button @click="sendData">Send Data to Head</button>
  </div>
</template>

<script>
export default {
  name: 'secretary1',
  methods: {
    sendData() {
      this.$emit('data-from-secretary', 'Data from secretary 1');
    }
  }
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
  border-radius: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  padding: 20px;
  width: 300px;
  margin: 20px auto;
  text-align: center;
}

h3 {
  font-family: 'Arial', sans-serif;
  color: #fff;
  margin-bottom: 20px;
}

button {
  background: #f6d365;
  background: -webkit-linear-gradient(to right, #fda085, #f6d365);
  background: linear-gradient(to right, #fda085, #f6d365);
  border: none;
  border-radius: 25px;
  color: #fff;
  cursor: pointer;
  font-size: 16px;
  padding: 10px 20px;
  text-transform: uppercase;
  transition: all 0.3s ease;
}

button:hover {
  background: #f093fb;
  background: -webkit-linear-gradient(to right, #f5576c, #f093fb);
  background: linear-gradient(to right, #f5576c, #f093fb);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}
</style>