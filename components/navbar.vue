<template>
    <div class="bg">
      <div>
        <b-navbar class="p-3 box mb-3 navbar">
          <template #brand>
             <img src="../assets/télécharger.jpg" alt="" class="image">
          </template>
          <template #start>
             <h1 class="umng"> UMNG ACADEMIC </h1>
          </template>
          <template #end>

            <b-navbar-item><a href=""><p class="nav-item">ACCUEIL</p></a></b-navbar-item>
            <b-navbar-item><a href="" class="cte">CONTACT</a></b-navbar-item>

            <b-navbar-dropdown label="ETABLISSEMENTS" class="nav-item">
                <b-navbar-item><a href="">Ecole Nationale Supérieure d'Agronomie <br> et de Foresterie (ENSAF)</a></b-navbar-item>
                <b-navbar-item><a href="">Ecole Nationale d'Administration <br> et de Magistrature (ENAM)</a></b-navbar-item>
                <b-navbar-item><a href="">Institut Supérieur d'Education Physique <br> et Sportive (ISEPS)</a></b-navbar-item>
                <b-navbar-item><a href="">Ecole Nationale Supérieure Polytechnique (ENSP)</a></b-navbar-item>
                <b-navbar-item><a href="">Faculté des Sciences et Techniques (FST)</a></b-navbar-item>
                <b-navbar-item><a href="">Faculté Des Sciences Economiques (FSE)</a></b-navbar-item>
                <b-navbar-item><a href="">Faculté Des Sciences et de la Santé (FSSA)</a></b-navbar-item>
                <b-navbar-item><a href="">Faculté des Lettres, des Arts et des Sciences <br> Humaines (FLASH)</a></b-navbar-item>
                <b-navbar-item><a href="">Institut Supérieur de Gestion (ISG)</a></b-navbar-item>
                <b-navbar-item><a href="">Ecole Normale Supérieure (ENS)</a></b-navbar-item>
                <b-navbar-item><a href="">Faculté Des Droits (FD)</a></b-navbar-item>
              </b-navbar-dropdown>

              <b-navbar-dropdown label="ACTUALITES" class="nav-item">
                <b-navbar-item><a href="">Actualités en images</a></b-navbar-item>
                <b-navbar-item><a href="">Actualités vidéos</a></b-navbar-item>
              </b-navbar-dropdown>  

              <b-navbar-dropdown label="A PROPOS" class="nav-item">
                <b-navbar-item><a href="">Enseignants</a></b-navbar-item>
                <b-navbar-item><a href="">Etudiants</a></b-navbar-item>
                <b-navbar-item><a href="">Bourses</a></b-navbar-item>
                <b-navbar-item><a href="">Autres...</a></b-navbar-item>

              </b-navbar-dropdown>  
                 
          </template>
      </b-navbar>
      </div>
      <div class="tr">
  
      </div>
    </div>
  </template>
  
  <script>
  export default {
  
  }
  </script>
  
  <style>
  body{
    padding: 0px;
  }
  .cte{
    color: black;
  }
  .cte:hover{
    color:#7957d5;
  }
  img{
      border-radius: 5px;
      width: 50px;
  }
  .navbar{
   position: fixed !important;
    border-radius: 0px; 
    width: 100%;
  }
  ul{
    padding-right: 30px;
  }
  .nav-item{
    font-size:15px;
    color: black;
    font-weight: 500;
  }
  .nav-item:hover{
    color:orange;
  }
  h1{
    font-size: 25px;
  }
  .image{
    width:40px;
    margin-left:10px;
  }
  .umng{
    padding-left:25px;
    padding-top:10px;
    font-weight: bold;
  }
  
  </style>
  
  
  <!-- <div
  class="is-flex is-flex-direction-row is-justify-content-space-between"
  >
  <div class="block2 m-5">
      <p class="h3">
        L'Université Marien Ngouabi est un établissement public de l'Etat à
        caractère scientifique culturel et technique chargée de
        l'enseignement supérieur et de la recherche scientifique. Elle jouit
        de la personnalité morale et de l'autonomie scientifique,
        administrative et financière. L'UMNG comprend des écoles et des
        instituts. Les écoles et instituts sont des structures
        d'enseignement supérieur et de recherche scientifique ayant pour
        mission la formation théorique appliquée et professionnalisée.
        L'Université Marien Ngouabi a pour mission fondamentale la recherche
        de la connaissance et sa transmission en formant des hommes et des
        femmes pour les besoins de la nation.
      </p>
  </div>
  <div class="block1 m-5">
   
    <div>
      <p class="p-3">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex
        dolores rem est repudiandae quas ab, molestias itaque! Id illum
        consectetur animi! Sed, omnis nobis! Quia illo tempore dolores
        temporibus perferendis.
      </p>
    </div>
  </div>
  
  </div> -->