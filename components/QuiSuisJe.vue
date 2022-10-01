<template>
  <div id="presentation">
    <v-container :fluid="true">
      <v-row justify="center">
        <v-col cols="12" md="4">
          <div class="titre">
            <h2>
              <span class="question1">Qui</span><br>
              <span class="question2">suis-je</span>
            </h2>
            <h1 class="questionTag">
              ?
            </h1>
          </div>
        </v-col>
        <v-col md="8">
          <div class="description">
            Je suis un acteur citoyen engagé pour le développement et l’épanouissement
            de l’humanité.
            <br>
            <br>Après mes études primaires et secondaires dominées par la passion des
            sciences notamment des mathématiques, et mes études universitaires dans
            les domaines de l’eau, de l’agriculture et des ressources naturelles, je dirige
            dès le début de ma carrière professionnelle un portefeuille de projets publics
            avec un passage au PNUD, des missions d’expertise avec l’UNESCO et la
            DANIDA, avant d’occuper le poste de Directeur Général des Ressources en
            Eau du Bénin.
            <br>
            <br>
            Très engagé sur les enjeux du développement, je suis Chargé de Mission à la
            Présidence de la République du Bénin depuis 2017. A ce titre, je supervise le
            Pôle Développement Durable au Bureau d’Analyse et d’Investigation de la
            Présidence, et j’appuie la gouvernance publique, la gestion des entreprises
            d’Etat, la définition des politiques et stratégies de développement, la
            conception, la mise en œuvre et le suivi du Programme d’Actions du
            Gouvernement, notamment dans les secteurs de l’eau, de l’énergie, de
            l’environnement, de l’assainissement, du cadre de vie, des mines et du
            pétrole.
            <br>
            <br>Hydrologue et Expert Sénior en ressources naturelles, infrastructures et
            développement durable avec plusieurs références à l’international, je suis
            auteur de plusieurs publications et communications scientifiques.
            <br>
            <br>J’enseigne la gestion intégrée des ressources en eau dans des universités du
            Bénin et d’Afrique, et réalise des missions de conseils et d’expertise en
            relation avec mes domaines de compétences.
            <br>
            <br>Acteur citoyen de développement, je reste à l’écoute de tous et demeure très
            engagé dans la vie associative et dans les activités communautaires pour
            l’épanouissement durable de l’humanité.
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'QuiSuisJe'
}
</script>

<style>
/* Importation de la police */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@500&display=swap');
/* Style */
#presentation {
    display: inline-flex;
    flex-direction: row;
    border: 1px solid black;
    height: auto;
    padding-top: 85px;
    padding-bottom: 80px;
    background: rgb(19, 5, 100);
}
.titre{
    color: rgba(255, 122, 80, 1);
    font-family: 'Montserrat', sans-serif;
    display: flex;
    justify-content: center;
}
.description{
    font-family: 'Montserrat', sans-serif;
    color: rgb(233, 233, 233);
    text-align: justify;
    font-size: 25px;
    font-weight: 300;
    line-height: 33px;
    letter-spacing: 0.5px;
    margin-left: 3%;
}
.global{
    line-height: 44.5px;
    /* line-height: 2%; */
}
.titre h2{
    /* display: inline; */
    font-size: 500%;
    font-weight: 600;
    /* background: #fff; */
}
.qui, .questions{
    font-size: 4.37rem;
}
.questions{
    width: auto;
    line-height: 44px;
}
.quiztag{
    font-size: 8rem;
    font-weight: 600;
    line-height: 2.87rem;
    letter-spacing: 0px;
}
h2 .question2 {
    min-width: 275,93px;
}
h1.questionTag {
    font-size: 180px;
    color: rgba(255, 122, 80, 1);
    font-weight: 600;
    margin-bottom: 0;
}
</style>
