<template >
  <v-app class="white">
      <!-- Nav Bar -->
      <v-app-bar app color="primary" dark>
        <v-toolbar-title> Vuetify toolbar title</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn text rounded >Home</v-btn>
        <v-btn text rounded >Login</v-btn>
      </v-app-bar>
    <v-content >
      <!-- lOGIN modal-->
      <v-card width="400" class="mx-auto mt-5 black">
        <v-card-title>
                <h1 class="display-1"> Login</h1>
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
    <!--Footer-->
    <v-footer
      color="primary lighten-1"
      padless
    >
      <v-row
        justify="center"
        no-gutters
      >
        <v-btn
          v-for="link in links"
          :key="link"
          color="white"
          text
          rounded
          class="my-2"
        >
          {{ link }}
        </v-btn>
        <v-col
          class="primary lighten-2 py-4 text-center white--text"
          cols="12"
        >
          {{ new Date().getFullYear() }} — <strong>Vuetify toolbar </strong>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
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
</style>
