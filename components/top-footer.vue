<template>
    <div>
      <div>
        <div class="is-flex is-justify-content-space-between">
          <div class="block-footer">
            <div class="is-flex">
              <div class="pl-5 hvr-icon-pulse-grow">
                <img src="../assets/télécharger.jpg" alt="" />
              </div>
              <div class="pl-5">
                <p>UMNG</p>
                <P
                  >Université Marien <br />
                  N'gouabi</P
                >
              </div>
            </div>
            <div>
              <p class="p-footer">
                C’est avec plaisir que nous vous accueillons au cours de cette
                année universitaire au sein de notre Etablissement.
              </p>
            </div>
            <div>
              <form action="" class="form">
                <b-field label="Email" label-position="inside">
                  <b-input class="form-control" type="email">
                  </b-input>
                </b-field>
                <b-button class="form-control">Envoyer</b-button>
                <p class="autor">
                  <a href=""
                    >creer par simeon poungui developpeur fullstack me contacter
                    par 06 752 69 94 </a
                  ><i class="mdi mdi-phone-classic"></i>
                </p>
              </form>
            </div>
          </div>
          <div class="block-footer">
            <h1 class="text-footer">MENU DU STE</h1>
            <div>
              <ul class="ul-f">
                <li>
                  <i class="mdi mdi-chevron-right"></i
                  ><a href="" class="hvr-underline-from-left">Accueil</a>
                </li>
                <li>
                  <i class="mdi mdi-chevron-right"></i
                  ><a href="" class="hvr-underline-from-left">Programme</a>
                </li>
                <li>
                  <i class="mdi mdi-chevron-right"></i
                  ><a href="" class="hvr-underline-from-left">Actualités</a>
                </li>
                <li>
                  <i class="mdi mdi-chevron-right"></i
                  ><a href="" class="hvr-underline-from-left">Formation</a>
                </li>
                <li>
                  <i class="mdi mdi-chevron-right"></i
                  ><a href="" class="hvr-underline-from-left">A propos</a>
                </li>
              </ul>
            </div>
          </div>
          <div class="block-footer">
            <h1 class="text-footer">ADRESSE</h1>
            <div>
              <h2 class="adresse">
                <i class="mdi mr-5 icon-footer mdi-atom-variant"></i> <span>Adresse:</span>
              </h2>
              <p class="t-adresse">
                177 rue Mayama, croisement Madoukou Tsekele, arrêt JANE VIALLE
              </p>
              <h2 class="adresse">
                <i class="mdi mr-5 icon-footer mdi-phone"></i><span>Telephone</span>
              </h2>
              <p class="t-adresse">
                (+242) 06 752 69 94 <br />
                (+242) 06 752 69 94 <br />
                (+242) 06 752 69 94
              </p>
              <h2 class="adresse">
                <i class="mdi mr-5 icon-footer mdi-email"></i><span>Email:</span>
              </h2>
              <p class="t-adresse">simeonpougui@gmail.com</p>
            </div>
          </div>
          <div class="block-footer">
            <h1 class="text-footer">HEURES D'OUVERTURE</h1>
            <p class="adresse">
              <i class="mdi mr-5 mdi-calendar"></i><span>Lundi-Venddredi</span>
            </p>
            <p class="horaire">De 7h15 à 20h15</p>
            <p class="adresse-f">
              <i class="mdi mr-5 mdi-calendar"></i><span>Samedi:</span>
            </p>
            <p class="horaire">De 7h15 à 20h15</p>
            <p class="adresse-f">
              <i class="mdi mr-5 mdi-calendar"></i><span>Dimanche:</span>
            </p>
            <p class="horaire">Sur rendez-vous!</p>
            <div class="is-flex link-footer is-justify-content-space-end">
              <div>
                <a href="" class="lien-f"
                  ><i class="mdi logo-footer mdi-facebook"></i
                ></a>
              </div>
              <div>
                <a href="" class="lien-f"
                  ><i class="mdi logo-footer mdi-youtube"></i
                ></a>
              </div>
              <div>
                <a href="" class="lien-f"
                  ><i class="mdi logo-footer mdi-whatsapp"></i
                ></a>
              </div>
              <div>
                <a href="" class="lien-f"
                  ><i class="mdi logo-footer mdi-twitter"></i
                ></a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {};
  </script>
  
  <style>
  .block-footer {
    width: 30%;
    height: 80vh;
    color: white;
    margin-top: 90px;
  }
  .text-footer {
    text-align: center;
  }
  .ul-f {
    margin-top: 40px;
    padding-left: 80px;
  }
  .ul-f > li > a {
    color: white;
    font-size: 20px;
  }
  .p-footer {
    padding-top: 50px;
    padding-left: 20px;
    font-size: 17px;
  }
  .form {
    margin-top: 30px;
  }
  .form-control {
    width: 100%;
    color: white;
    font-size: 18px;
    background-color: transparent;
  }
  .adresse {
    text-align: center;
    padding-top: 50px;
  }
  .adresse-f {
    padding-left: 80px;
    padding-top: 50px;
  }
  .t-adresse {
    padding-left: 120px;
    padding-top: 10px;
  }
  .horaire {
    padding-top: 10px;
    padding-left: 100px;
    font-size: 20px;
  }
  .mdi-calendar{
    color: orange;
    font-size: 25px;
  }
  .icon-footer{
    color: orange;
    font-size: 25px;
  }
  .link-footer {
    margin-left: 70px;
    padding-top: 8px;
  }
  .logo-footer {
    font-size: 30px;
    padding-left: 10px;
  }
  .lien-f {
    color: white;
  }
  .lien-f:hover {
    color: white;
  }
  .autor {
    margin-top: 50px;
  }
  .autor > a {
    color: white;
  }
  </style>
  