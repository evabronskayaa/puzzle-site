<template>
  <div id="app" class="background">
    <div class="content">
      <h1>
        fB6ulcJRFN2kJkEPlTW/UGl4TnU8GacMc56MyUoh2PDC/<br />sCdKA0orbLdSTogNtNvH/6OYmWypc5KrrRfNXw+q0vw8<br />7C/fOi19dbi7FJFqLw/WsTogCMLTeRJrrKKBfwK
      </h1>
      <p>https://magictool.ai/tool/encrypt-text/ru/</p>
      <CustomInput :len="9" @fkValueChanged="handleFkValueChanged" theme="light" />

      <button @click="handleCheckAnswer">Try to send</button>
    </div>
  </div>
</template>

<script>
import CustomInput from '../components/CustomInput.vue'

export default {
  name: 'SecondTask',
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

    handleCheckAnswer() {
      const t = this.fkValue.toUpperCase()
      let key = import.meta.env.VITE_SECOND_TASK_ANSWER
      if (t === key) {
        alert("That's true")
        this.goOn()
      }
    }
  }
}
</script>

<style scoped lang="scss">
.background {
  background-color: white;
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
  width: 900px;
}

.hint-text {
  margin-top: 25px;
  font-size: 20px;
}

h1 {
  color: black;
  font-size: 30px;
  margin-bottom: 100px;
  font-weight: 400;
}

p {
  color: white;
  bottom: 0;
  left: 0;
}

button {
  background-color: black;
  color: white;
  padding: 12px 55px;
  border-radius: 10px;
  border: 0 solid #e2e8f0;
  font-size: 20px;
  margin: 80px 0;
  cursor: pointer;
}
</style>
