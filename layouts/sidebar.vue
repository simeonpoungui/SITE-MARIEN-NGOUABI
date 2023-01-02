<template>
    <div class="main has-background-light">
        <div class="sideM">
          <div class="is-flex">
            <div><P ><i class="mdi logo mdi-triforce"></i></P></div>
            <div class="menu"><a href="accueil"><i class="mdi mdi-menu"></i></a></div>
          </div>
          <div class="is-flex mb-3 is-flex-direction-row">
            <div class="pr-4">
              <b-icon icon="forum" class="icon"></b-icon>
            </div>
            <div>
              <nuxt-link to="/admin"><p class="tb hvr-underline-from-center">Tableau de bord</p></nuxt-link>
            </div>
          </div>
          <div class="separator"></div>
          <div class="is-flex mt-3 mb-3">
            <div class="pr-4"><b-icon icon="account"></b-icon></div>
            <div>
              <nuxt-link to="/liste_etudiant"
                ><p class="tb hvr-underline-from-center">Liste des etudiants</p>
              </nuxt-link>
            </div>
          </div>
          <div class="separator"></div>
          <div class="is-flex mt-3 mb-3">
            <div class="pr-4"><b-icon icon="account-edit"></b-icon></div>
            <div>
              <nuxt-link to="/corps_enseignants"
                ><p class="tb hvr-underline-from-center">Corps enseignants</p>
              </nuxt-link>
            </div>
          </div>

          <div class="separator"></div>
          <div class="is-flex mt-3 mb-3">
            <div class="pr-4"><b-icon icon="account-edit"></b-icon></div>
            <div>
              <nuxt-link to="/personnels_admin"
                ><p class="tb hvr-underline-from-center">Personnels admin</p>
              </nuxt-link>
            </div>
          </div>
          <div class="separator"></div>
          <div class="is-flex mt-3 mb-3">
            <div class="pr-4"><b-icon icon="av-timer"></b-icon></div>
            <div>
              <nuxt-link to="/emploi"
                ><p class="tb hvr-underline-from-center">Emploi du temps</p>
              </nuxt-link>
            </div>
          </div>
          <div class="separator"></div>
          <div class="is-flex mt-3 mb-3">
            <div class="pr-4"><b-icon icon="calendar-sync" class="calendrier"></b-icon></div>
            <div>
              <nuxt-link to="/calendrier"
                ><p class="tb hvr-underline-from-center">Calendrier Scolaire</p>
              </nuxt-link>
            </div>
          </div>
          <div class="separator"></div>
          <div class="is-flex mt-3 mb-3">
            <div class="pr-4"><b-icon icon="currency-usd"></b-icon></div>
            <div>
              <nuxt-link to="/payement"
                ><p class="tb hvr-underline-from-center">Payements</p>
              </nuxt-link>
            </div>
          </div>
          <div class="separator"></div>
          <div class="is-flex mt-3 mb-3">
            <div class="pr-4"><b-icon icon="escalator-box"></b-icon></div>
            <div>
              <nuxt-link to="/examen"
                ><p class="tb hvr-underline-from-center">Examens</p>
              </nuxt-link>
            </div>
          </div>
      </div>
    </div>
  </template>
  <script>
  import chart from '../components/chart.vue';
  import('../assets/Hover-master/css/hover.css');
  export default {
    components: { chart },};
  </script>
  
  <style>
  .sideM {
    width: 16%;
    height: 100vh;
    z-index: 100;
    padding-left: 15px;
    position: fixed;
    padding-right: 15px;
    background-color: rgb(15,76,92);
  }
  .separator {
    width: 100%;
    border: 1px solid rgba(116, 114, 114,0.2);
  }
  .tb {
    color: white;
  }
  .tb:hover {
    color: yellow;
  }
  .calendrier{
    color: white;
  }
  
  hr{
    border: 1px solid rgb(252, 245, 245);
  }
  .icon{
    color: white;
  }
  .logo{
    font-size: 80px;
    color: white;
    padding-top: -30px;
  }
  .menu{
    padding-top: 60px;
  }
  .menu >a{
    color: white;
    padding-left: 30px;
    font-size: 20px;
  }
  </style>
  