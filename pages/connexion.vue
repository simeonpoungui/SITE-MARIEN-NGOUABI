<template>
    <div class="main">
      <b-loading
        :is-full-page="isFullPage"
        v-model="isLoading"
        :can-cancel="true"
      ></b-loading>
      <center>
        <div class="content pt-1">
          <div></div>
          <div class="form column is-two-fifths box p-5">
            <p class="connexion">CONNEXION</p>
            <img src="../assets/logo.png" alt="" class="logo" />
  
            <b-field class="mt-3" label-position="inside" label="Email">
              <b-input icon="email" type="email" rounded> </b-input>
            </b-field>
  
            <b-field class="mt-3" label-position="inside" label="Mot de passe">
              <b-input icon="lock" type="password" rounded> </b-input>
            </b-field>
            <div class="forget">
              <nuxt-link to="/connexion">Mot de passe oublié?</nuxt-link>
            </div>
            <br />
            <b-button
              class="mt-3 connecter"
              rounded
              icon-right="arrow-right"
              label="SE CONNECTER"
              type="is-link"
              @click="authentification"
            ></b-button
            ><br /><br /><br />
            <div>
              Pas de compte?
              <nuxt-link to="/inscription">inscrivez-vous !</nuxt-link>
            </div>
          </div>
        </div>
      </center>
  
    </div>
  </template>
  <script>
  
  export default {
    components: {  },
    data() {
      return {
        isLoading: false,
        isFullPage: true,
      };
    },
    methods: {
      async authentification() {
        this.isLoading = true;
        await this.$axios
          .$post("/authentification", {
            email: this.email,
            password: this.password,
          })
          .then((res) => {
            console.log(res);
            setTimeout(() => {
              this.isLoading = false;
              this.success();
            }, 6 * 1000);
          })
          .catch((error) => {
            console.log(error);
          });
      },
      success() {
        this.$buefy.dialog.alert({
          message:
            "Vous etes connecté",
          type: "is-success",
          title: "CONNEXION ETABLIE",
          hasIcon: true,
        });
      },
    },
  };
  </script>
  <style>
  body {
    background-attachment: fixed;
  }
  .connexion {
    color: #7957d5;
    font-size: 20px;
    font-weight: bold;
  }
  .main {
    background-image: url("../assets/img-20210720-wa0038.jpg");
    background-attachment: fixed;
    overflow: hidden;
    background-size: cover;
    width: 100%;
    height: 100vh;
  }
  .connecter {
    width: 100%;
  }
  .content {
    background: rgba(255, 255, 255, 0.5);
    overflow-y: scroll;
    height: 100vh;
  }
  .form {
    background: rgba(255, 255, 255, 0.6);
    margin-top: 50px;
    border-radius: 20px;
  }
  .logo {
    width: 80px;
  }
  .forget {
    padding-top: 20px;
    font-size: 12px;
  }
  </style>
  