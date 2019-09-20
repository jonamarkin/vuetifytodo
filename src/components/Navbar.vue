<template>
    <nav>
        <v-navigation-drawer v-model="drawer" app color="purple lighten-2">

            <v-layout column align-center>
                <v-flex class="mt-5">
                    <v-avatar size="100">
                        <img src="avatar-1.png" alt="">
                    </v-avatar>
                    <p class="white--text subheading mt-1">
                        Jonathan Ato Markin
                    </p>
                </v-flex>
            </v-layout>

            <v-list dense>
                <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                    <v-list-item-icon>
                        <v-icon v-text="link.icon" class="white--text"></v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title v-text="link.text" class="white--text"></v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>

        <v-app-bar app flat color="grey--text">
            <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="grey--text">
                <span class="font-weight-light">PROJECT</span>
                <span>TRACKER</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn flat color="grey lighten-1">
                <span>Sign Out</span>
                <v-icon right>exit_to_app</v-icon>
            </v-btn>
        </v-app-bar>
    </nav>
</template>


<script>
export default {
    data(){
        return{
            drawer:false,
            links:[
                {icon: 'dashboard', text: 'Dashboard', route: '/'},
                {icon: 'folder', text: 'My Projects', route: '/projects'},
                {icon: 'person', text: 'Team', route: '/team'}
            ]
        }
    }
}
</script>