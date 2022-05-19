<template>
    <v-content class="white">
     <NavBar></NavBar>
        <v-container>
            <v-card>
                <v-text>
                    <h1>Sign up</h1>
                </v-text>
            </v-card>
            <v-spacer></v-spacer>
        </v-container>
        <v-container >
            <v-row>
                <v-col cols="12" md="3">
                <v-spacer></v-spacer>
                </v-col>
                <v-col cols="12" md="6">
                    <v-form>
                        <v-text-field label="email" type="mail"></v-text-field>
                        <v-autocomplete
                           :items="browser"
                           label="Prefered Browser"
                        >
                        </v-autocomplete>
                            <v-file-input
                                accept="image/*"
                                label="Profile Picture"
                                >
                            </v-file-input>
                            <v-row>
                                <v-col
                                cols="12"
                                sm="6"
                                md="4"
                                >
                                    <v-menu
                                        v-model="menu2"
                                        :close-on-content-click="false"
                                        :nudge-right="40"
                                        transition="scale-transition"
                                        offset-y
                                        min-width="auto"
                                    >
                                        <template v-slot:activator="{ on, attrs }">
                                        <v-text-field
                                            v-model="birthday"
                                            label="birthday"
                                            prepend-icon="mdi-calendar"
                                            readonly
                                            v-bind="attrs"
                                            v-on="on"
                                        ></v-text-field>
                                        </template>
                                        <v-date-picker
                                        v-model="birthday"
                                        @input="menu2 = false"
                                        ></v-date-picker>
                                    </v-menu>
                                </v-col>
                            <v-spacer></v-spacer>
                        </v-row>
                    </v-form>
                </v-col>
                <v-col cols="12" md="3">
                <v-spacer></v-spacer>
                </v-col>
            </v-row>
        </v-container>
    </v-content>
</template>

<script>
    export default {
        data: () => ({
            browser: ['firefox', 'chrome', 'opera', 'buzz'],
            birthday:'',
    }),
    }
</script>

<style lang="scss" scoped>
.v-application .white {
    background-color: #FFFFFF !important;
    border-color: #FFFFFF !important;
}
</style>