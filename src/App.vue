<template>
  <v-app>
  <!-- login -->
  <v-navigation-drawer
      absolute
      dark
      src="./assets/bg.png"
      width="100%"
      permanent
    >
      <v-list>
        <v-list-item
          v-for="([icon, text], i) in items"
          :key="i"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <!-- login -->
   <v-card width="400" class="mx-auto mt-5">
     <v-card-title>
    <h1 class="display-1">Login</h1>
     </v-card-title>
     <v-card-text>
       <v-form>
         <v-text-field label="Email"
         prepend-icon="mdi-account-circle"
          />
         <v-text-field
           :type="showPassword ? 'text' : 'password'"
          label="Password"
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
          @click:append="showPassword = !showPassword"
           />
       </v-form>
     </v-card-text>
     <v-divider></v-divider>
     <v-card-actions>
       <v-btn color="success">Register</v-btn>
       <v-spacer></v-spacer>
       <v-btn color="info">Login</v-btn>
       </v-card-actions>
   </v-card>
   </v-navigation-drawer>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
    
  },

  data: () => ({
    showPassword: false
  }),
};
</script>
