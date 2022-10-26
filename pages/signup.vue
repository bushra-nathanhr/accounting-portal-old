<template>
    <v-container  :class="{
          'container pa-4 my-12': $vuetify.breakpoint.smAndDown,
          'container pa-10 my-12': $vuetify.breakpoint.mdAndUp,
        }" id="main">
      <!-- alert -->
      <v-row>
        <v-alert text type="success" border="left" width="100%" dismissible>
          Thank you <strong>Olive</strong>, Your Profile was created
          successfully !
        </v-alert>
      </v-row>
      <!-- avatar -->
      <v-row class="justify-center">
        <v-avatar size="150px">
          <img src="https://images.unsplash.com/photo-1633332755192-727a05c4013d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=580&q=80" />
        </v-avatar>
      </v-row>
      <!-- name -->
      <v-row class="justify-center pb-5">
        <span class="title text-secondary py-2 font-weight-bold">{{ name }}</span>
      </v-row>
      <v-text-field
        label="First Name"
        outlined
        shaped
        prepend-inner-icon="mdi-account"
      ></v-text-field>
      <v-text-field
        label="Last Name"
        outlined
        shaped
        prepend-inner-icon="mdi-account"
      ></v-text-field>
      <v-text-field
        label="Username"
        outlined
        shaped
        prepend-inner-icon="mdi-account"
      ></v-text-field>
      <v-text-field
        label="Email"
        outlined
        shaped
        prepend-inner-icon="mdi-email"
      ></v-text-field>
      <v-text-field
        label="Address"
        outlined
        shaped
        prepend-inner-icon="mdi-map-marker"
      ></v-text-field>
      <v-text-field
        label="Phone Number"
        outlined
        shaped
        prepend-inner-icon="mdi-phone"
      ></v-text-field>
      <v-row>
        <v-col cols="12" md="6">
          <v-btn
            color="secondary"
            outlined
            text
            block
            tile
            elevation="0"
            class="pa-6 font-weight-bold"
          >
            Cancel
          </v-btn>
        </v-col>
        <v-col cols="12" md="6">
          <v-btn
            color="info"
            class="pa-6 font-weight-bold"
            block
            tile
            elevation="0"
          >
            Save
          </v-btn>
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'index',
    layout: 'login',
    data() {
      return {
        loginImg: 'https://images.unsplash.com/photo-1531592937781-344ad608fabf?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=735&q=80'
      }
    },
  }
  </script>
  
  <style scoped>
    #main {
        background: white;
        padding: 20px;
        margin: 10px;
        border: 1px solid white;
        border-radius: 10px;
    }
  </style>