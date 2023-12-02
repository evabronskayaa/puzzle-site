<template>
    <div id="app" class="main">
      <div class="content">
        <h1>Welcome Alex!</h1>
        <h2>Glad to see u here</h2>
        <br>
        <img src="../assets/arrow.png" width="222"/>
        <button>Start</button>
      </div>
    </div>
</template>
  
<script>
  
  export default {
    name: 'TheWelcome',
    components: {
    }
  }
</script>

<style scoped>

h1{
  font-size: 64px;
  color: white;

}

h2{
  font-size: 40px;
  color: white;

}
.main {
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: url("../assets/gradient_background.png");
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

.content{
  text-align: center;
  display: inline-block;
}

button {
  align-items: center;
  color: white;
  background: transparent;
  border: 0 solid #E2E8F0;
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
  text-transform: uppercase;
  margin: 10px 0;
}


</style>
  