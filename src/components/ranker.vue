<template>
    <v-container>
        <v-row>
            <v-col cols="12" lg="4" >
                <v-card
                    max-width="344"
                >
                    <v-img
                    src=".././assets/Azeem Pasha.jpg"
                    height="200px"
                    ></v-img>

                    <v-card-title>
                    Azeem Pasha
                    </v-card-title>

                    <v-card-subtitle>
                        Top Contributor 
                    </v-card-subtitle>

                </v-card>
            </v-col>
            <v-col cols="12" lg="4" >
                <v-card
                    max-width="344"
                >
                    <v-img
                    src=".././assets/Ritush Kumar.jpg"
                    height="200px"
                    ></v-img>

                    <v-card-title>
                    Ritush Kumar
                    </v-card-title>

                    <v-card-subtitle>
                    Top Contributor 
                    </v-card-subtitle>

                </v-card>
            </v-col>
            
            <v-col cols="12" lg="4" >
                <v-card
                    max-width="344"
                >
                    <v-img
                    src=".././assets/Prajjwal Agrahari.jpg"
                    height="200px"
                    ></v-img>

                    <v-card-title>
                    Prajjwal Agrahari
                    </v-card-title>

                    <v-card-subtitle>
                        Top Contributor  
                    </v-card-subtitle>

                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
  export default {
    name: 'Ranker',
    data: () => ({
    }),
    methods : {
    },
    created() {
	},
  }
</script>

<style scoped>
    #leader {
        background-color: #F55F43;
    }
    #custom-text-color {
        color:  #F55F43;
    }
</style>
