<template>
  <v-app class="white">
    <NavBar></NavBar>
    <v-content >
    <v-card black>
        <v-card-title  width="1900" class="mx-auto mt-5 white">
            <h1 class="display-1"> Home Page</h1>
        </v-card-title>
    </v-card>
      <!-- lOGIN modal-->
      <v-card width="400" class="mx-auto mt-5 white">
        <v-card-title>
                <h2 class="display-3"> WELCOME</h2>
        </v-card-title>
      </v-card>
    </v-content>
    <FooterComponent></FooterComponent>
  </v-app>
</template>

<script>
import NavBar from '../components/NavBar.vue'
import FooterComponent from '../components/FooterComponent.vue'
export default {
  component: {
    NavBar,
    FooterComponent
  },
  name: 'IndexPage',
    data: () => ({
    showPassword: false,
    collapseOnScroll: true,
    links:[
      'home',
      'login',
      'register'
    ],
  })
}
</script>
<style>
.container {
  max-width: 1900px;
  padding: 0;
}
.v-main{
  padding-top: 60px !important;
}
.display-2 {
    color: black;
    text-align: center;
    padding-left: 50px;
    padding-right: 50px;
}
.display-3 {
    color: black;
    text-align: center;
    padding-left: 30px;
    padding-right: 20px;
}
</style>
