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

        <v-navigation-drawer v-model="drawer" color="purple lighten-2" temporary absolute>
            <v-list>
                <v-list-item-group v-model="link">
                    <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                    <v-list-item-icon>
                        <v-icon v-text="link.icon" class="white--text"></v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title v-text="link.text" class="white--text"></v-list-item-title>
                    </v-list-item-content>
                    </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>

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