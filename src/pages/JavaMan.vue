<template>
  <div>
    <vue-fake-input
      :length="5"
      :fontSize="40"
      inputColor="fff"
      fontColor="fff"
      :allowPaste="false"
      v-model="fullValue"
    />
    <p>text</p>
  </div>
</template>

<script>
import VueFakeInput from 'vue-fake-input'

export default {
  name: 'JavaMan',
  components: {
    VueFakeInput
  }
}
</script>
