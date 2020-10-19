<template>
    <v-container>
    <v-expansion-panels popout >
      <v-expansion-panel
        v-for="(item,i) in userData"
        :key="i"
        id="panels"
        class="white--text"
      >
        <v-expansion-panel-header >
            <v-row
                align="center"
                class="spacer"
                no-gutters
              >
                <v-col  >
                    <v-avatar size="36px">
                        <img alt="Avatar" :src="userData[i].dp" >
                    </v-avatar>
                </v-col>
                <v-col cols=8 lg=10>
                    <span id="custom-text-color" class="pr-2 text--bold">{{i+1}}. </span>
                    {{userData[i].name}}
                    <v-card id="panels" elevation="0">
                        <v-card-text>
                            <v-progress-linear color="#F55F43" rounded :value="(userData[i].quests_status - 1) * 10"></v-progress-linear>
                        </v-card-text>
                    </v-card>
                </v-col>
                <v-col  >
                    {{userData[i].quests_status}} Quests
                </v-col>
            </v-row>
            <template v-slot:actions>
                <v-icon color="#F55F43">
                $expand
                </v-icon>
            </template>
        </v-expansion-panel-header>
        <v-expansion-panel-content>
          <v-row>
            <v-col
            v-for="(quest,j) in userData[i].quests"
            :key="j"
            class="d-flex child-flex"
            xs="12"
            md="3"
            >
                <v-img
                    :src="userData[i].quests[j].imageSrc"
                    :lazy-src="userData[i].quests[j].imageSrc"
                    
                    class="grey lighten-2"
                >
                    <template v-slot:placeholder>
                    <v-row
                        class="fill-height ma-0"
                        align="center"
                        justify="center"
                    >
                        <v-progress-circular
                        indeterminate
                        color="grey lighten-5"
                        ></v-progress-circular>
                    </v-row>
                    </template>
                </v-img>
            </v-col>
        </v-row>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
    </v-container>
</template>

<script>
  export default {
    name: 'Leaderboard',
    data: () => ({
        userData : []
    }),
    methods : {
        fetchData() {
            fetch(`https://qwiklabs-ranking-dsccu.herokuapp.com/api`)
				.then((res) => res.json())
				.then((data) => {
                    this.userData = data;
                })
				.catch((err) => {
					console.log(err);
					// alert("Sorry unable to get data");
				});
        }
    },
    mounted() {
		this.fetchData(this.name);
	},
  }
</script>

<style scoped>
#leader {
    background-color: #F55F43;
}
#panels {
    background-color: #35394B;

}
#custom-text-color {
    color:  #F55F43;
}
</style>
