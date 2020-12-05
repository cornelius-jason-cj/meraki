<template>
  <div id="Produtcs">
    <v-container>
      <v-row justify="center">
        <v-col cols="12" md="6">
          <v-row>
            <v-col cols="12" md="2">
              <v-row
                v-for="n in products"
                :key="n.id"
                class="ma-2"
              >
              <v-img
                :src="n.src"
                @click="changeImage(n.src)"
              >
              </v-img>
              </v-row>

            </v-col>

            <v-col cols="12" md="10">
              <v-img
                :src="imageBigSrc"
              >
              </v-img>
          </v-col>
          </v-row>
        </v-col>

        <v-col cols="12" md="4">
          <template>
            <v-card
              class="mx-auto my-12"
              max-width="100%"
              elevation="0"
            >

              <v-card-title>Lapis Legit</v-card-title>

              <v-card-text>
                <div>It is a long established fact that a reader will be distracted by the readable <br> content of a page when looking at its layout.</div>
                <br>
                <v-row
                  align="center"
                  class="mx-0"
                >
                  <v-rating
                    :value="4.5"
                    color="amber"
                    dense
                    half-increments
                    readonly
                    size="14"
                  ></v-rating>

                  <div class="grey--text ml-4">
                    4.5 (413)
                  </div>
                </v-row>

              </v-card-text>

              <v-divider class="mx-4"></v-divider>

              <v-card-title>Order Availability</v-card-title>

              <v-card-text>
                <v-chip-group
                  active-class="deep-purple accent-4 white--text"
                  column
                >
                  <v-chip>7:00 AM - 20:00 PM</v-chip>
                </v-chip-group>
              </v-card-text>

              <v-card-actions>
                <v-btn
                  color="deep-purple lighten-2"
                  text
                >
                  Reserve
                </v-btn>
              </v-card-actions>
            </v-card>
          </template>

        </v-col>
      </v-row>
    </v-container>
  </div>  
</template>

<script>
  export default {
    data: () => ({
      products:[
        {
          id:1,
          name:'LapisLegit-1',
          src: require('../assets/LapisLegit-1.jpg')
        },
        {
          id:2,
          name:'LapisLegit-2',
          src: require('../assets/LapisLegit-2.jpg')
        },
        {
          id:3,
          name:'LapisLegit-3',
          src: require('../assets/LapisLegit-3.jpg')
        },
        {
          id:4,
          name:'LapisLegit-4',
          src: require('../assets/LapisLegit-4.jpg')
        },
        {
          id:5,
          name:'LapisLegit-5',
          src: require('../assets/LapisLegit-5.jpg')
        },
      ],
      imageBigSrc:require('../assets/LapisLegit-1.jpg'),
      IntroducingImage: require('../assets/IntroducingImage.png')
  }),
  methods: {
    changeImage (src) {
      this.imageBigSrc = src 
    }
  }
    
}
</script>

<style scoped>
#Produtcs {
  margin: auto;
  height: 900px;
}

</style>