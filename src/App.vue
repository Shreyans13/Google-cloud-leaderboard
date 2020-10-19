<template>
  <v-app>
    <Navbar />
    <v-main  id='leader'>
      <Rankers />
      <LeaderBoard/>
      <p class="text-center white--text" id="leader">
        Made with <v-icon>mdi-heart</v-icon> by <a href="https://github.com/SwarnimDoegar">Swarnim Deogar</a>, 
        <a href="https://github.com/vtrrix">Vivek Sony</a> and 
        <a href="https://github.com/shreyans13">Shreyans Jain</a>
      </p>
    </v-main>
  </v-app>
</template>

<script>
import LeaderBoard from './components/leaderboard';
import Navbar from './components/navbar';
import Rankers from './components/ranker';

export default {
  name: 'App',

  components: {
    LeaderBoard,
    Navbar,
    Rankers
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
    #leader {
        background-color: #F55F43;
    }
</style>
