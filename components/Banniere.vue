<template>
  <div id="banniere">
    <!-- Image de la bannière -->
    <v-img
      src="/Image1 1.png"
      class="image-banniere"
    />

    <div class="presentationFlottante">
      <v-container>
        <v-row>
          <v-col cols="12">
            <!-- Zone de présentation brève -->
            <div class="zonePresentationBreve">
              <!-- Contenu de présentation -->
              <div class="presentationBreve">
                <!-- Nom du docteur -->
                <h2>Dr Arnaud Yémalin ZANNOU</h2>

                <!-- Sous titre de la présentation -->
                <h5 class="ss-titre">
                  Hydrologue et Expert en ressources naturelles,<br>
                  infrastructures et développement durable
                </h5>

                <!-- Text -->
                <p class="simple">
                  Plus de 20 ans d’expérience de haut niveau
                </p>
                <p class="text-center slogan ">
                  <b>Je suis un acteur citoyen de developpement <br> au service de l'homme.</b>
                </p>
              </div>

              <!-- Réseaux sociaux -->
              <div class="coordonne">
                <div class="global">
                  <span><img src="/mail.jpg" class="icone" alt=""> contact@arnaudzannou.com </span><br>
                  <span><img src="/call.jpg" class="icone Cellule" alt=""> <span class="num">+229 91 91 66 66</span>
                    <span class="reseau">
                      <img src="/facebook.jpg" alt="">
                      <img src="/youtube.jpg" alt="">
                      <img src="/linkedin.jpg" alt="">
                      <img src="/insta.jpg" alt="">
                    </span>
                  </span>
                </div>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BanniereSection'
}
</script>

<style>
#banniere {
    position: relative;
    margin-top: 140px;
    padding: 0;
    margin-bottom: 0;
}
.presentationFlottante {
   position: absolute;
   right: 0;
   top: 0;
   color: black;
   width: 50%;
   /* height: 100%; */
   /* border: 1px solid rgba(2, 56, 137, 1); */
}
.zonePresentationBreve {
    display: flex;
    width: 100%;
    /* border: 1px solid rgba(2, 56, 137, 1); */
}
.presentationBreve {
   /* border: 1px solid rgba(2, 56, 137, 1); */
   /* position: absolute;
   top: 20px; */
}
.presentationBreve h2 {
    color: rgba(2, 56, 137, 1);
}
.coordonne {
    /* float: inline-end; */
    /* border: 1px solid rgba(2, 56, 137, 1); */
    /* position: absolute; */
    /* top: 100px; */
    /* right: 0;
    bottom: 0; */
    /* align-items: baseline; */
    display: flex;
    /* align-self: flex-end; */
}
</style>
