<template>
    <div id="app">
      <CustomInput :len="5" @fkValueChanged="handleFkValueChanged" />
      <h2>Value: {{ fkValue }}</h2>
    </div>
  </template>
  
  <script>
  import CustomInput from '../components/CustomInput.vue'
  
  export default {
    name: 'JavaMan',
    components: {
      CustomInput
    },
    data() {
      return {
        fkValue: ''
      }
    },
    methods: {
      handleFkValueChanged(value) {
        this.fkValue = value;
      }
    }
  }
  </script>
  