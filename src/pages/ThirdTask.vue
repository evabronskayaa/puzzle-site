<template>
  <div id="app" class="background">
    <div>
      <div class="puzzle">
        <img src="../assets/javaMan.png" class="man" @click="handleClicks" />
        <div>
          <h1>
            Who is he? He can help you <br />
            to find next code
          </h1>
        </div>
      </div>
      <div class="answer">
        <CustomInput :len="4" @fkValueChanged="handleFkValueChanged" :theme="dark" />
        <button @click="handleCheckAnswer">Try to send</button>
      </div>
    </div>
  </div>
</template>

<script>
import CustomInput from '../components/CustomInput.vue'

export default {
  name: 'ThirdTask',
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
          '01110100 01101000 01100101 00100000 01110100 01101000 01101001 01101110 01100111 00100000 01100001 01100010 01101111 01110101 01110100 00100000 01101000 01101001 01110011 00100000 01100011 01110010 01100101 01100001 01110100 01101001 01101111 01101110 00100000 01101001 01110011 00100000 01101000 01101001 01100100 01100100 01100101 01101110 00100000 01101001 01101110 00100000 01101111 01110101 01110010 00100000 01101111 01100110 01100110 01101001 01100011 01100101'
        )
        this.clicks = 0
      }
    },

    handleCheckAnswer() {
      const t = this.fkValue.toUpperCase()
      let key = import.meta.env.VITE_THIRD_TASK_ANSWER
      if (t === key) alert("That's true")
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
  display: flex;
}

.content {
  text-align: center;
  display: inline-block;
  color: white;
}

.puzzle {
  margin: 60px 60px 200px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.answer {
  text-align: center;
}

.man {
  width: 402px;
  &:hover {
    cursor: pointer;
  }
}

h1 {
  display: table-cell;
  color: white;
  font-size: 64px;
  margin-bottom: 100px;
  font-weight: 400;
  vertical-align: middle;
  text-align: right;
}

button {
  background-color: white;
  padding: 12px 55px;
  border-radius: 7px;
  border: 0 solid #e2e8f0;
  font-size: 20px;
  margin: 80px 0;
  cursor: pointer;
}
</style>
