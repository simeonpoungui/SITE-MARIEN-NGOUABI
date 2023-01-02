<template>
    <div>
      <div class="is-flex">
        <div class="tr"><Sidebar /></div>
        <div class="bored">
          <div><Topbar /></div>
          <div class="mt-20">
            <div class="content-menu m-0">
              <div class="pt-5">
                <div class="is-flex is-justify-content-space-between">
                  <div class="is-flex">
                    <div>
                      <b-icon
                        icon="home-circle-outline"
                        type="is-small"
                        class="mb-4"
                      ></b-icon>
                    </div>
                    <div class="pl-2">
                      <p>Accueil</p>
                    </div>
                    <div class="pl-2">
                      <b-icon icon="arrow-right" class="fleche"></b-icon>
                    </div>
                    <div class="pl-2">
                      <p>Liste des etudiants</p>
                    </div>
                  </div>
                  <div class="midle">
                    <a href=""><i class="mdi mdi-account"></i> Personnels administratifs</a>
                  </div>
                  <div class="midle"><a href="corps"><i class="mdi mdi-account"></i> Personnels enseignants</a></div>
                  <div class="is-flex"></div>
                </div>
                <div class="is-flex is-justify-content-space-between">
                  <div class="is-flex">
                    <div class="pl-5">
                      <b-field label="nom">
                        <b-input icon="account"></b-input>
                      </b-field>
                    </div>
                    <div class="pl-5">
                      <b-field label="prenom">
                        <b-input icon="account"></b-input>
                      </b-field>
                    </div>
  
                    <div class="pl-5">
                      <b-field label="parccours">
                        <b-input icon="account"></b-input>
                      </b-field>
                    </div>
                    <div>
                      <b-select placeholder="niveau" class="ml-3 mt">
                        <option>licence 1</option>
                        <option>licence 2</option>
                        <option>licence 3</option>
                      </b-select>
                    </div>
                    <div>
                      <b-select placeholder="etablissements" class="ml-3 mt">
                        <option></option>
                      </b-select>
                    </div>
                    <div class="pr-4 pl-3 mt">
                      <b-select placeholder="année">
                        <option>2020-2021</option>
                        <option>2021-2022</option>
                        <option>2022-2023</option>
                      </b-select>
                    </div>
                  </div>
                  <div class="is-flex">
                    <div class="pr-5 mt">
                      <b-button type="is-primary"
                        ><i class="mdi mdi-update"></i> valider</b-button
                      >
                    </div>
                  </div>
                </div>
              </div>
              <div></div>
              <div class="tab pt-3">
                <div class="btns is-flex is-justify-content-space-between">
                  <div>
                    <div class="is-flex">
                      <div class="pl-5 pt-4">
                        <b-button class="is-primary" icon="account"
                          ><i class="mdi mdi-format-list-bulleted-triangle"></i>
                          Liste des étudiants</b-button
                        >
                      </div>
                      <div class="pl-5 pt-4">
                        <b-button class="is-primary" icon="account"
                          ><i class="mdi mdi-format-list-bulleted-triangle"></i>
                          Imprimer la liste</b-button
                        >
                      </div>
                      <div class="pl-5 pt-4">
                        <b-button class="is-primary" icon="account">
                          <i class="mdi pr-2 mdi-printer"></i>Generer une attestation</b-button
                        >
                      </div>
                      <div class="pl-5 pt-4">
                        <b-button class="is-primary" icon="account">
                          <i class="mdi pr-2 mdi-printer"></i>Generer une carte etudiante</b-button
                        >
                      </div>
                      <div class="pl-5 pt-4">
                        <b-button class="" type="is-primary" @click="inscription">
                          <i class="mdi mdi-account-multiple-plus"></i> Ajouter un
                          etudiant
                        </b-button>
                      </div>
                    </div>
                  </div>
                  <div class="is-flex">
                    <div></div>
                  </div>
                </div>
                <div class="table mt-3 mr-0">
                    
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  <script>
  import Sidebar from "../layouts/sidebar.vue";
  import Topbar from "../layouts/topbar.vue";
  export default {
    data() {
      return {
       
      };
    },
    components: { Sidebar, Topbar },
  };
  </script>
  
  <style>
  .bored{
    width: 100%;
  }
  .mt-20 {
    height: 90vh;
    margin-left: 200px;
  }
  
  .is-lght:hover {
    color: #fca311;
  }
  .btn-tab {
    width: 85px;
    font-size: 13px;
  }
  .mt {
    margin-top: 33px;
  }
  .table {
    width: 100%;
  }
  .tab {
    width: 100%;
    height: 390px;
    padding-right: 0px;
  }
  .separator {
    width: 100%;
    border: 1px solid gray;
  }
  .tb {
    color: white;
  }
  .content-menu {
    width: 100%;
  }
  .etab {
    padding-top: 10px;
    padding-left: 10px;
    font-size: 25px;
  }
  .btn-primary {
    border-radius: 7px;
    width: 130px;
    height: 40px;
    border: 0px;
  }
  hr {
    border: 1px solid rgb(252, 245, 245);
  }
  .column {
    color: white;
  }
  .midle > a {
    color: black;
    cursor: pointer;
  }
  .midle > a:hover {
    color: #fca311;
    text-decoration: underline;
  }
  .mb-4 {
    color: black;
    margin-left: 20px;
  }
  .fleche {
    color: black;
  }
  .mdi-chevron-left {
    color: blue;
  }
  .mdi-chevron-right {
    color: blue;
  }
  </style>
  