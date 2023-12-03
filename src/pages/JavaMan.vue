<template>
  <div id="app" class="background">
    <img src="./javaMan.png" class="man" @click="handleClicks" />
    <p>Who is he? He can help you to find next code</p>
    <CustomInput :len="4" @fkValueChanged="handleFkValueChanged" :theme="black" />
    <button @click="handleCheckAnswer">Try to send</button>
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
      fkValue: '',
      clicks: 0
    }
  },
  methods: {
    handleFkValueChanged(value) {
      this.fkValue = value
    },

    handleClicks() {
      this.clicks++
      if (this.clicks === 5) {
        alert(
          '110100011010011110011100000110001111100101100101110000111101001101001110111111011101000001101001111001110000011010001101001110010011001001100101110111010000011010011101110100000110111111101011110010100000110111111001101100110110100111000111100101 his creation is hidden in our office (press ctrl+C to copy this text) ((https://planetcalc.ru/6604/))'
        )
        this.clicks = 0;
      }
    },

    handleCheckAnswer() {
        const t = this.fkValue.toUpperCase();
        console.log(t)
        if (t === "LENA")
            alert("That's true")
    }
  }
}
</script>

<style scoped lang="scss">
.background {
  width: 100vw;
  height: 100vh;
  background: black;
  color: white;
  padding: 0;
  margin: -8px;
}

.man {
  &:hover {
    cursor: pointer;
  }
}
</style>
