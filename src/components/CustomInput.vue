<template>
  <div id="app">
    <vue-fake-input :length="len" :fontSize="40" v-model="fkValue" @input="updateFkValue" :theme="theme"  />
  </div>
</template>

<script>
import VueFakeInput from '../components/VueFakeInput.vue'

export default {
  name: 'CustomInput',
  components: {
    VueFakeInput
  },
  props: {
    len: Number,
    theme: String
  },
  data() {
    return {
      fkValue: ''
    }
  },
  methods: {
    updateFkValue(event) {
      if (event?.inputType === 'deleteContentBackward') {
        this.fkValue = this.fkValue.substring(0, this.fkValue.length - 1);
      } else {
        this.fkValue += event.target.value;
      }
      this.$emit('fkValueChanged', this.fkValue);
    }
  }
}
</script>
