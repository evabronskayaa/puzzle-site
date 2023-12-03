<template>
  <div id="app" class="background">
    <div class="content">
      <h1>Enter number:</h1>
      <CustomInput :len="2" @fkValueChanged="handleFkValueChanged" theme="dark" />

      <button @click="handleCheckAnswer">Try to send</button>
      <p class="hint-text">Have difficulties? Get <a @click="handleClicks">hint</a></p>
    </div>
  </div>
</template>

<script>
import CustomInput from '../components/CustomInput.vue'

export default {
  name: 'FirstTask',
  components: {
    CustomInput
  },
  props: {
    goOn: {
      type: Function,
      required: true
    }
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
      if (this.clicks === 1) {
        alert("You need Andrew's birthday")
        this.clicks = 0
      }
    },

    handleCheckAnswer() {
      const t = this.fkValue.toUpperCase()

      let key = import.meta.env.VITE_FIRST_TASK_ANSWER
      if (t === key) alert("That's true")
      this.goOn();
    }
  }
}
</script>

<style scoped lang="scss">
.background {
  background-color: black;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  background-position: center;
  background-size: 100% 100%;
  background-repeat: no-repeat;
}

.content {
  text-align: center;
  display: inline-block;
  color: white;
}

.hint-text {
  margin-top: 25px;
  font-size: 20px;
}

h1 {
  color: white;
  font-size: 36px;
  margin-bottom: 100px;
  font-weight: 400;
}

a {
  text-decoration: underline;
}

button {
  background-color: white;
  padding: 12px 55px;
  border-radius: 10px;
  border: 0 solid #e2e8f0;
  font-size: 20px;
  margin: 25px 0;
  cursor: pointer;
}
</style>
