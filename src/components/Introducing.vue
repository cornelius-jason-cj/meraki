<template>
  <div id="Introducing">
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="4">
           <v-card
            class="mx-auto introducingText"
            max-width="80%"
            elevation="0"
          >
            <v-card-text>
              <p class="display-1 text--primary">
                Introducing our NEW perfectly Lapis Legit and Marmer cake
              </p>
              <div class="text--primary">
                well meaning and kindly.<br>
                "a benevolent smile"
              </div>
            </v-card-text>
            <v-card-actions>
              <v-btn
                text
                color="deep-purple accent-4"
              >
                Learn More
              </v-btn>
            </v-card-actions>
          </v-card>

        </v-col>
        <v-col cols="12" md="6">
          <v-img
            :src="IntroducingImage"
            max-width="100%"
            max-height="100%"
            margin="auto"
          >
          </v-img>
        </v-col>
      </v-row>
    </v-container>
  </div>  
</template>

<script>
  export default {
    data: () => ({
      IntroducingImage: require('../assets/IntroducingImage.png')
  }),
    
}
</script>

<style scoped>
#Introducing{
  margin: auto;
  height: 850px;
}

</style>