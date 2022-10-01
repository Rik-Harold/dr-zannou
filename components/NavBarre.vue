<template>
  <nav id="navbar">
    <!-- Titre du site -->
    <div class="titreSite">
      <h1>{{ titre }}</h1>
    </div>

    <!-- Liste des liens d'accès -->
    <div v-if="!responsive" class="listMenu">
      <v-btn
        v-for="(menu, index) in navigation"
        :key="index"
        x-large
        text
        :to="menu.toComposant"
        :style="{ margin: 'auto ' + margeEntete + 'px' }"
        color="rgb(0,0,0)"
      >
        <span>{{ menu.name }}</span>
      </v-btn>
    </div>

    <!-- Bouton d'ouverture du menu latéral gauche -->
    <div v-else class="zoneMenu">
      <button
        type="button"
        aria-label="toggle curtain navigation"
        :class="{ 'active': menuOk }"
        @click="menuOk = !menuOk"
      >
        <span class="line l1" />
        <span class="line l2" />
        <span class="line l3" />
      </button>
    </div>

    <!-- Bouton d'ouverture du menu latéral gauche --
    <div v-else class="listeMenu">
      <div class="zoneMenu">
        <button
          type="button"
          aria-label="toggle curtain navigation"
          :class="{ 'active': menuOk }"
          @click="menuOk = !menuOk"
        >
          <span class="line l1" />
          <span class="line l2" />
          <span class="line l3" />
        </button>
      </div>
    </div> -->

    <!-- Conteneur responsive de la barre de navigation -->
    <div v-if="menuOk" class="zoneMenuResponsive">
      <v-btn v-for="(menu, index) in navigation" :key="index" large text :to="menu.toComposant">
        <div>{{ menu.name }}</div>
      </v-btn>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavBarre',
  data () {
    return {
      titre: 'Dr Arnaud Yémalin ZANNOU',
      margeEntete: '20',
      menuOk: false,
      largeur: false,
      responsive: false,
      menuActif: '',
      navigation: [
        {
          name: 'COMPETENCES',
          route: '',
          actif: false
        },
        {
          name: 'EXPERIENCES',
          route: '',
          actif: false
        },
        {
          name: 'FORMATION',
          route: '',
          actif: false
        },
        {
          name: 'LEADERSHIP',
          route: '',
          actif: false
        },
        {
          name: 'CONTACT',
          route: '',
          actif: false
        }
      ]
    }
  },
  mounted () {
    const instance = this
    // Alerte à la réduction de la largeur de la fenêtre
    window.addEventListener('resize', function (e) {
      if (document.documentElement.clientWidth < 1560) {
        // Modification du style
        instance.margeEntete = '5'
      }
      if (document.documentElement.clientWidth > 1515) {
        instance.responsive = false
      } else {
        instance.responsive = true
      }
    })
  }
}
</script>

<style>
/* Importation de la police */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');
/* Style */
#navbar {
    width: 100%;
    padding: 40px 35px;
    display: flex;
    align-items: center;
    background-color: #fff;
    justify-content: space-between;
    box-shadow: 1.2px 1.2px 1.2px 1.2px  rgb(207, 200, 200);
    position: fixed;
    top: 0;
    z-index: 1;
}
.titreSite {
    font-size: 27px;
    color: rgba(2, 56, 137, 1);
    font-family: 'Montserrat', sans-serif;
}
/* .listMenu {
    color: black !important;
} */
/* Style du bouton hamburger */
.zoneMenu {
    position: relative;
    width: 50px;
    height: 50px;
    margin-right: 50px;
    margin: 0;
    padding: 0;
    /* padding: 5px; */
    /* border: 1px solid black; */
}
.zoneMenu button {
    width: 100%;
    height: 100%;
}
/* Style des lignes du menu hamburger */
.line {
  height: 6px;
  width: 100%;
  display: block;
  position: absolute;
  background-color: rgba(2, 56, 137, 1);
  transition: transform 0.3s ease-out, opacity 0.1s ease-out;
}
.l1 {
  transform: translateY(-10px);
}
.l3 {
  transform: translateY(10px);
}
/* Animation du menu hamburger */
.active .l1 {
  transform: translateY(0px) rotate(135deg);
}
.active .l2 {
  opacity: 0;
}
.active .l3 {
  transform: translateY(0px) rotate(-135deg);
}
/* Style du menu responsif actif */
.zoneMenuResponsive {
  z-index: 1;
  display: flex;
  flex-direction: column;
  position: absolute;
  top: 140px;
  right: 0;
  background-color: rgba(2, 56, 137, 1);
  border-radius: 10%;
}
.zoneMenuResponsive div {
  padding: 25px;
  font-size: 125%;
}
.zoneMenuResponsive div:hover {
  cursor: pointer;
  /* color: black; */
  color: #fff;
}
</style>
