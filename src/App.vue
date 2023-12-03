<script>
import ThirdTask from './pages/ThirdTask.vue';
import TheWelcome from './pages/TheWelcome.vue';
import FirstTask from './pages/FirstTask.vue';
import SecondTask from './pages/SecondTask.vue';
import FourthTask from './pages/FourthTask.vue';
import YouWin from './pages/YouWin.vue';

export default{
components:{
  TheWelcome,
  FirstTask,
  SecondTask,
  ThirdTask,
  FourthTask,
  YouWin,
},
data() {
    return {
      page: 0,
    }
  },
  methods: {
    incrementPage() {
      this.page++;
    },
  }
}
</script>

<template>
  <TheWelcome v-if="page === 0" :goOn="incrementPage"/>
  <FirstTask v-if="page === 1" :goOn="incrementPage"/>
  <SecondTask v-if="page === 2" :goOn="incrementPage"/>
  <ThirdTask v-if="page === 3" :goOn="incrementPage"/>
  <FourthTask v-if="page === 4" :goOn="incrementPage"/>
  <YouWin v-if="page === 5"/>
</template>

<style scoped></style>
