<template>
<!-- Nav Bar -->
      <v-app-bar app color="primary" dark>
        <v-toolbar-title> Vuetify toolbar title</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn text rounded to="/">Home</v-btn>
         <v-btn text rounded to="/dashBoard">Dash Board</v-btn>
        <v-btn text rounded to="/login">Login</v-btn>
        <v-btn text rounded to="/signUp">Sign Up</v-btn>
    </v-app-bar>
</template>

<script>
export default {
     name: 'NavBar',
     
    setup () {
        

        return {}
    },

}
</script>

<style lang="scss" scoped>

</style>