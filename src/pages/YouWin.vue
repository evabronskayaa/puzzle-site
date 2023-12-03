<template>
    <div id="app" class="main">
      <div class="content">
        <h1>You win</h1>
        <h2>Thank you for playing this game</h2>
        <br>
        <a href="https://drive.google.com/drive/folders/1dddi36sHEQRUF00fWzKtGxonZDrmqN5I?usp=sharing">It's just a link...</a>
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
h1, h2{
  color: white;
}


h1{
  font-size: 64px;
  text-transform: uppercase;
  margin-bottom: 10px;
  font-weight: 500;
}

h2{
  font-size: 40px;
  margin-top: 0;
  font-weight: 400;
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
  text-transform: lowercase;
  margin: 10px 0;
}


</style>
  