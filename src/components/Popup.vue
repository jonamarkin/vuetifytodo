<template>
    <v-dialog v-model="dialog" width="500 ">
      <template v-slot:activator="{ on }">
        <v-btn color="red lighten-2" dark v-on="on">
          Add A New Project
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="headline grey lighten-2" primary-title  >
          <h2>Add A New Project</h2>
        </v-card-title>

        <v-card-text>
          
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          
        </v-card-actions>
      </v-card>
    </v-dialog>
</template>

<script>
export default {
    
}
</script>