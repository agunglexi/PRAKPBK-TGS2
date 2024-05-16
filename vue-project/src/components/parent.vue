<template>
    <div class="container">
      <h2>Head of Department</h2>
      <p>Data from Secretary: {{ secretaryData }}</p>
      <div class="secretaries">
        <Secretary1 @data-from-secretary="handleDataFromSecretary" />
        <Secretary2 @data-from-secretary="handleDataFromSecretary" />
      </div>
    </div>
  </template>
  
  <script>
  import Secretary1 from './secretary1.vue';
  import Secretary2 from './secretary2.vue';
  
  export default {
    name: 'Head',
    components: {
      Secretary1,
      Secretary2
    },
    data() {
      return {
        secretaryData: ''
      };
    },
    methods: {
      handleDataFromSecretary(data) {
        this.secretaryData = data;
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
    background: linear-gradient(135deg, #cfd9df 0%, #e2ebf0 100%);
    border-radius: 15px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    padding: 30px;
    width: 400px;
    margin: 20px auto;
    text-align: center;
  }
  
  h2 {
    font-family: 'Arial', sans-serif;
    color: #333;
    margin-bottom: 15px;
  }
  
  p {
    font-family: 'Arial', sans-serif;
    color: #555;
    background: #f5f5f5;
    border-radius: 10px;
    padding: 10px;
    width: 100%;
    box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 20px;
  }
  
  .secretaries {
    display: flex;
    justify-content: space-between;
    width: 100%;
  }
  
  .secretaries > * {
    flex: 1;
    margin: 0 10px;
  }
  </style>