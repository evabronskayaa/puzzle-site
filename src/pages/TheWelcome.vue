<template>
  <div id="app" class="main">
    <div class="content">
      <h1>Welcome Alex!</h1>
      <h2>Glad to see u here</h2>
      <br />
      <img src="../assets/arrow.png" width="222" />
      <br />
      <button @click="goOn">Start</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheWelcome',
  components: {},
  props: {
    goOn: {
      type: Function,
      required: true
    }
  }
}
</script>

<style scoped>
h1,
h2 {
  color: white;
}

h1 {
  font-size: 64px;
  text-transform: uppercase;
  margin-bottom: 10px;
  font-weight: 500;
}

h2 {
  font-size: 40px;
  margin-top: 0;
  font-weight: 400;
}

.main {
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: url('../assets/gradient_background.png');
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
}

button {
  align-items: center;
  color: white;
  background: transparent;
  border: 0 solid #e2e8f0;
  display: inline-flex;
  font-size: 1rem;
  font-weight: 500;
  justify-content: center;
  padding: 10px 30px;
  text-decoration: none;
  width: auto;
  cursor: pointer;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  text-transform: lowercase;
  margin: 10px 0;
}
</style>
