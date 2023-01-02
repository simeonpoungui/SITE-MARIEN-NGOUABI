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
            <p class="inscription">INSCRIPTION</p>
            <img src="../assets/logo.png" alt="" class="logo" />
            <b-field class="mt-3" label-position="inside" label="Nom">
              <b-input v-model="nom" icon="account" rounded> </b-input>
            </b-field>
            <b-field class="mt-3" label-position="inside" label="Prenom">
              <b-input v-model="prenom" icon="account" rounded> </b-input>
            </b-field>
  
            <b-field class="mt-3" label-position="inside" label="Telephone">
              <b-input v-model="telephone" icon="phone" rounded> </b-input>
            </b-field>
  
            <b-field class="mt-3 ml-1">
              <b-checkbox rounded> homme </b-checkbox>
              <b-checkbox rounded> femme </b-checkbox>
            </b-field>
  
            <b-field
              class="mt-3"
              label-position="inside"
              label="Date de naissance"
            >
              <b-input
                v-model="date_de_naissance"
                icon="datepicker"
                type="date"
                rounded
              >
              </b-input>
            </b-field>
  
            <b-field class="mt-3" label-position="inside" label="Email">
              <b-input v-model="email" icon="email" type="email" rounded>
              </b-input>
            </b-field>
  
            <b-field class="mt-3" label-position="inside" label="Mot de passe">
              <b-input v-model="password" icon="lock" type="password" rounded>
              </b-input>
            </b-field>
  
            <b-field
              class="mt-3"
              label-position="inside"
              label="Confirmer votre mot de passe"
            >
              <b-input
                v-model="retype_password"
                icon="lock"
                type="password"
                rounded
              >
              </b-input>
            </b-field>
  
            <b-button
              class="inscrit"
              rounded
              icon-right="content-save"
              label="S'INSCRIRE"
              type="is-link"
              @click="inscription"
            ></b-button
            ><br /><br /><br />
            <div style="color: black">
              Deja un compte?
              <nuxt-link to="/connexion">connectez-vous</nuxt-link>
            </div>
          </div>
        </div>
      </center>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isLoading: false,
        isFullPage: true,
        nom: "",
        prenom: "",
        telephone: "",
        email: "",
        date_de_naissance: "",
        password: "",
        retype_password: "",
      };
    },
    methods: {
      async inscription() {
        this.isLoading = true;
        await this.$axios
          .$post("/inscription", {
            nom: this.nom,
            prenom: this.prenom,
            telephone: this.telephone,
            email: this.email,
            date_de_naissance: this.date_de_naissance,
            password: this.password,
            retype_password: this.retype_password,
          })
          .then((res) => {
            console.log(res);
            setTimeout(() => {
              this.isLoading = false;
              this.success();
            }, 4 * 1000);
          })
          .catch((error) => {
            console.log(error);
          });
      },
      //fontcion qui affiche que la suppression a ete effectué
      success() {
        this.$buefy.dialog.alert({
          message: "Inscription effectuée avec succès",
          type: "is-success",
          title:"INSCRIPTION",
           hasIcon:true,
        });
      },
    },
  };
  </script>
  
  <style>
  body {
    background-attachment: fixed;
  }
  .inscrit {
    width: 100%;
    margin-top: 15px;
  }
  .inscription {
    color: #9990dd;
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
  .content {
    background: rgba(255, 255, 255, 0.5);
    overflow-y: scroll;
    height: 100vh;
  }
  .form {
    background: rgba(255, 255, 255, 0.6);
  }
  .logo {
    width: 80px;
  }
  </style>
  