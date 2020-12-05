<template>
  <div id="Navbar">
    <v-row justify="center" id="titleMeraki">
      <v-col cols="12" md="12">
        <h1 style="text-align:center">Meráki Bakehouse</h1>
      </v-col>
    </v-row>


    <v-row justify="center" id="NavbarItems">
      <v-col
        cols="12"
        md="7"
      >
      <p>logo</p>
      </v-col>

      <v-col
        cols="12"
        md="5"
        class="navbarList"
      >
      <v-row>
        <v-col
          cols="12"
          md="3"
        >
          <v-menu
              open-on-hover
              offset-y
            > 
              <template v-slot:activator="{ on, attrs }">
                <div
                  v-bind="attrs"
                  v-on="on"
                >
                  Products <i class="arrow down"></i>
                </div>
              </template>

              <v-list>
                <v-list-item
                  v-for="(item, index) in Products"
                  :key="index"
                >
                  <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item>
              </v-list>
            </v-menu>
          </v-col>

          <v-col
            cols="12"
            md="3"
          >
            <div>About Us</div>
          </v-col>

          <v-col
            cols="12"
            md="3"
          >
            <div>Where to buy</div>
          </v-col>
          
          <v-col
            cols="12"
            md="3"
          >
            <v-menu
                open-on-hover
                offset-y
              > 
                <template v-slot:activator="{ on, attrs }">
                  <div
                    v-bind="attrs"
                    v-on="on"
                  >
                    En <i class="arrow down"></i>
                  </div>
                </template>

                <v-list>
                  <v-list-item
                    v-for="(item, index) in Languanges"
                    :key="index"
                  >
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-menu>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
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
  }),
}
</script>

<style scoped>

#titleMeraki{
  background-color: rgb(255, 235, 218);
}

#Navbar{
  z-index: 9999; 
  margin: auto;
}

.arrow {
  border: solid black;
  border-width: 0 3px 3px 0;
  display: inline-block;
  padding: 3px;
}

.down {
  transform: rotate(45deg);
  -webkit-transform: rotate(45deg);
}
</style>