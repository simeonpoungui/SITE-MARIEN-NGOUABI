<template>
    <div>
      <div>
        <Sidebar/>
      </div>
      <div>
        <Topbar/>
      </div>
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
                      <p>Liste des Enseignants</p>
                    </div>
                  </div>
                  <div class="midle">
                    <a href=""><i class="mdi mdi-account"></i> Personnels administratifs</a>
                  </div>
                  <div class="midle"><a href="liste_etudiant"><i class="mdi mdi-account"></i> Voir la liste des etudiants</a></div>
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
                          Liste</b-button
                        >
                      </div>
                      <div class="pl-5 pt-4">
                        <b-button class="is-primary" icon="account">
                          <i class="mdi mdi-printer"></i> imprimer</b-button
                        >
                      </div>
                      <div class="pl-5 pt-4">
                        <b-button class="" type="is-primary" @click="inscription">
                          <i class="mdi mdi-account-multiple-plus"></i> Ajouter un
                          enseignant
                        </b-button>
                      </div>
                    </div>
                  </div>
                  <div class="is-flex">
                    <div></div>
                  </div>
                </div>
                <div class="table mt-3 mr-0">
                  <b-table
                    class="column"
                    :data="data"
                    :bordered="false"
                    :hoverable="true"
                    :loading="isLoading"
                    :per-page="3"
                    paginated
                    :focusable="true"
                    :mobile-cards="false"
                  >
                    <b-table-column
                      field="idmembre"
                      label="ID"
                      searchable
                      v-slot="props"
                    >
                      {{ props.row.idmembre }}
                    </b-table-column>
                    <b-table-column
                      field="code_membre"
                      label="code_membre"
                      searchable
                      v-slot="props"
                    >
                      {{ props.row.code_membre }}
                    </b-table-column>
                    <b-table-column
                      field="nom"
                      label="nom"
                      searchable
                      v-slot="props"
                    >
                      {{ props.row.nom }}
                    </b-table-column>
                    <b-table-column
                      field="prenom"
                      label="prenom"
                      searchable
                      v-slot="props"
                    >
                      {{ props.row.prenom }}
                    </b-table-column>
                    <b-table-column
                      field="date_de_naissance"
                      label="date_naissance"
                      searchable
                      v-slot="props"
                    >
                      {{ props.row.date_de_naissance }}
                    </b-table-column>
                    <b-table-column
                      field="telephone"
                      label="telephone"
                      searchable
                      v-slot="props"
                    >
                      {{ props.row.telephone }}
                    </b-table-column>
                    <b-table-column
                      field="password"
                      label="password"
                      searchable
                      v-slot="props"
                    >
                      {{ props.row.password }}
                    </b-table-column>
                    <b-table-column
                      field="Actions"
                      label="Actions"
                      searchable
                      v-slot="props"
                    >
                      <div class="is-flex">
                        <div>
                          <b-button
                            type="is-danger"
                            class="btn-tab"
                            @click="confirm(props.row.idmembre)"
                            ><i class="mdi mdi-delete"></i> supprimer
                          </b-button>
                        </div>
                        <div>
                          <b-button
                            type="is-primary"
                            class="btn-tab ml-2"
                            @click="update(props.row.idmembre)"
                            ><i class="mdi mr-1 mdi-update"></i>modifier
                          </b-button>
                        </div>
                      </div>
                    </b-table-column>
                  </b-table>
                </div>
              </div>
            </div>
          </div>
    </div>
  </template>
  
  <script>
  import Sidebar from '../layouts/sidebar.vue';
  import Topbar from '../layouts/topbar.vue';
  export default {
      components: { Sidebar, Topbar }
  }
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