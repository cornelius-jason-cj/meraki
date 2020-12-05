<template>
  <div id="Welcome">
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="8">
          <v-img
            :src="WelcomeImage"
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
      Products: [
        { title: 'Kue Lapis' },
        { title: 'Kue Marmer' }
      ],
      Languanges: [
        { title: 'English' },
        { title: 'Bahasa Indonesia' }
      ],
      WelcomeImage: require('../assets/WelcomeImage.png')
  }),
}
</script>

<style scoped>
#Welcome {
  height: 1000px;
}

</style>