<template>
  <div class="form-container sign-in-container mt-12">
    <v-img src="https://static.vecteezy.com/system/resources/thumbnails/004/417/585/small_2x/unlock-personal-password-account-security-free-vector.jpg" width="531" height="636" class="img-mid"></v-img>
    <v-form
      action="#"
      :class="{
        'px-2': $vuetify.breakpoint.smAndDown,
        'px-8': $vuetify.breakpoint.mdAndUp,
      }"
    >
      <img src="https://static.vecteezy.com/system/resources/thumbnails/004/417/585/small_2x/unlock-personal-password-account-security-free-vector.jpg" class="team-img pt-8" />
      <h1 class="pb-8 font-weight-bold">SIGNIN</h1>
      <v-text-field
        prepend-inner-icon="mdi-account"
        placeholder="E-mail"
        filled
      ></v-text-field>
      <v-text-field
        prepend-inner-icon="mdi-lock"
        placeholder="Password"
        type="password"
        filled
      ></v-text-field>
      <v-btn
        color="info"
        block
        dark
        tile
        class="pa-6 font-weight-bold"
        elevation="0"
        @click="login()"
        >Sign In</v-btn
      >
      <v-row class="justify-center py-10">
        <span
          :class="{
            'text-secondary forgot-password-sm': $vuetify.breakpoint.smAndDown,
            'text-secondary forgot-password-md': $vuetify.breakpoint.mdAndUp,
          }"
          >Forgot your password?</span
        >
      </v-row>
    </v-form>
  </div>
</template>
<script>
export default {
  layout:'login',
  data: () => {
    return {
      username: null,
      password: null,
    };
  },
  methods: {
    login() {
      this.$store.dispatch("authPageModule/loginAndSaveToken", {
        username: this.username,
        asswor: this.password,
      });
    },
  },
};
</script>

<style scoped>
  form {
  background-color: #ffffff;
  height: 100%;
}

  .sign-in-container {
    left: 0;
    width: 50%;
    z-index: 2;
  }
  .team-img {
    width: 50%;
  }
  .container.right-panel-active .sign-in-container {
    transform: translateX(100%);
  }
  .container.right-panel-active .overlay-container {
    transform: translateX(-100%);
  }
  .forgot-password-sm {
    font-size: 12px;
  }
  .forgot-password-md {
    font-size: 15px;
  }
  @import url("https://fonts.googleapis.com/css2?family=Raleway:wght@300;400;500;600;700;800;900&display=swap");

#app {
  font-family: Raleway, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: url("https://images.unsplash.com/photo-1497366216548-37526070297c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80")
    no-repeat center center fixed;
  background-repeat: no-repeat;
  background-size: cover;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
}

.sm-main-style {
  margin: auto;
  width: 95%;
}
.md-main-style {
  margin: auto;
  width: 70%;
}

.footer-md {
  padding: 30px 0px;
}
.footer-md a {
  text-decoration: none;
  color: white !important;
  font-size: 1.1rem;
  font-family: cursive;
  font-weight: 600;
}

.footer-sm {
  padding: 20px 0px;
}
.footer-sm a {
  text-decoration: none;
  color: white !important;
  font-size: 0.8rem;
  font-family: cursive;
  font-weight: 600;
}
.img-mid {
  position: absolute;
  right: 240px;
}
  </style>