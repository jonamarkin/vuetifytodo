<template>
    <nav>
        <v-toolbar flat app>
            <v-app-bar-nav-icon color="grey--text" @click="drawer =!drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="grey--text">
                <span class="font-weight-light">VUETIFY</span>
                <span>TODO</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn flat color="grey lighten-1">
                <span>Sign Out</span>
                <v-icon right>exit_to_app</v-icon>
            </v-btn>
        </v-toolbar>

        <v-navigation-drawer v-model="drawer" class="indigo" temporary absolute>
            <p>test</p>
        </v-navigation-drawer>

    </nav>
</template>


<script>
export default {
    data(){
        return{
            drawer:false
        }
    }
}
</script>