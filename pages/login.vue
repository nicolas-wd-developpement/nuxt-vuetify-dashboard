<template>
<v-content class="white">
    <NavBar></NavBar>
    <v-content >
    <v-card black>
        <v-card-title  width="1900" class="mx-auto mt-5 white">
            <h1 class="display-1"> Login Page</h1>
        </v-card-title>
    </v-card>
      <!-- lOGIN modal-->
      <v-card width="400" class="mx-auto mt-5 grey">
        <v-card-title>
                <h2 class="display-2"> Login</h2>
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field label="UserName" prepend-icon="mdi-account-circle"></v-text-field>
            <v-text-field 
              :type= "showPassword ? 'text' : 'password'"
              label="password"
              prepend-icon="mdi-lock"
              :append-icon="showPassword ? 'mdi-eye' :'mdi-eye-off'"
              @click:append="showPassword = ! showPassword">
            </v-text-field>
          </v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>

          <v-btn color="success"> Register </v-btn>
                <v-spacer>   </v-spacer>
          <v-btn color="info"> Login </v-btn>
        </v-card-actions>
      </v-card>
    </v-content>
    <FooterComponent></FooterComponent>
  </v-content>
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
.display-1 {
    color: black;
}
.display-2 {
    color: white;
}
</style>
