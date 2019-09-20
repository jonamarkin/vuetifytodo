<template>
    <v-dialog v-model="dialog" width="500 ">
      <template v-slot:activator="{ on }">
        <v-btn color="green lighten-2" dark v-on="on">
          Add A New Project
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="headline" >
          <h3>Add A New Project</h3>
        </v-card-title>

        <v-card-text>
          <v-form class="px-3">
              <v-text-field label="Title" v-model="title" prepend-icon="folder"></v-text-field>
              <v-textarea label="Information" prepend-icon="edit" v-model="content"></v-textarea>
              <v-btn class="success mx-0 mt-3" @click="submit">ADD PROJECT</v-btn>
          </v-form>
        </v-card-text>

        <v-card-actions>
          
        </v-card-actions>
      </v-card>
    </v-dialog>
</template>

<script>
export default {
    data(){
        return{
            title: "",
            content: ""
        }
    },
    methods:{
        submit(){
            console.log(this.title, this.content)
        }
    }
}
</script>