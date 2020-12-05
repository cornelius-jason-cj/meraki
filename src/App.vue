<template>
  <v-app>
    <v-main id="backgroundWeb">
      <div id="card">
        <v-container>
          <v-card
            width="100%"
            elevation="2"
            id="cardContain"
          >
            <Navbar/>
            <Welcome/>
            <Introducing/>
            <Products/>
            <AboutUs/>
          </v-card>
        </v-container>
      </div>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar';
import Welcome from './components/Welcome';
import Introducing from './components/Introducing';
import Products from './components/Products';
import AboutUs from './components/AboutUs';

export default {
  name: 'App',

  components: {
    Navbar,
    Welcome,
    Introducing,
    Products,
    AboutUs
  },
  data () {
    return {

    }
  }
};
</script>

<style scoped>

#backgroundWeb {
  background-color: rgb(248, 248, 248);
}

#card{
  background-color: rgb(255, 235, 218);
  width: 100%;
}


</style>
