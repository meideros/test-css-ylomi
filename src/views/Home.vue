<template>
  <div>
    <header class="header">
      <div class="header-content">
        <div class="banner">
          <span class="banner-left">
            <img src="../assets/images/ylomi-logo.svg" alt="ylomi">

            <span class="menu" @click="openMenu">
              <i class="fal fa-bars fa-2x"></i>
            </span>
          </span>

          <span class="banner-right" id="menu">
            <span class="logo-close">
              <img src="../assets/images/ylomi-logo.svg" alt="ylomi">
              <i class="fal fa-times fa-2x" @click="closeMenu"></i>
            </span>
            
            <span class="links">
              <router-link to="/">
                <span class="ask-service">Demander un service</span>
              </router-link>

              <router-link to="/">
                <span>Devenir Professionnel</span>
              </router-link>
            </span>
            
            <span class="buttons">
              <router-link to="/">
                <button class="login">Connexion</button>
              </router-link>

              <router-link to="/">
                <button class="signup">Inscription</button>
              </router-link>
            </span>
          </span>
        </div>

        <div class="after-banner">
          <h1>
            Trouvez le prestataire <span>idéal</span>
            pour tous les services au Bénin
          </h1>

          <h4 class="first">There's a lot to discover. From home. Or a short drive away.</h4>

          
          <div class="search-bar">
            <i class="fal fa-search icon"></i>
            <input class="search" type="search" placeholder="Trouver votre service">
          </div>

          <h4 class="second">Ce sont les Services populaires en ce moment.</h4>

          <div class="services-pop">
            <span>Plombiers</span>
            <span>Aide au déménagement</span>
            <span>Aide au déménagement</span>
            <span>Aide au déménagement</span>
            <span>Aide au déménagement</span>
          </div>
        </div>
      </div>
    </header>

    <div class="covid-info">
      <span>
        Découvrez nos actions sur le COVID à Cotonou
        <i class="fal fa-long-arrow-right"></i>
        <i class="far fa-chevron-right chevron"></i>
      </span>
    </div>
    <div class="body">
      <div class="informations">
        <h1>Pourquoi utiliser Ylomi?</h1>
        <span class="infos">
          <div>
            <i class="fad fa-users fa-2x"></i>
            <span>
              <h2 class="title">Professionnels Qualifiés</h2>
              <p class="desc">There's a lot to discover. From home. Or a short drive away.</p>
            </span>
            
          </div>
          <div>
            <i class="fad fa-shield-check fa-2x"></i>
            <span>
              <h2 class="title">Une assurance de Qualité</h2>
              <p class="desc">There's a lot to discover. From home. Or a short drive away.</p>
            </span>
          </div>
          <div>
            <i class="fad fa-map-marker-alt fa-2x"></i>
            <span>
              <h2 class="title">Dans votre zone</h2>
              <p class="desc">There's a lot to discover. From home. Or a short drive away.</p>
            </span>
          </div>
        </span>
      </div>
    </div>
    
  </div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',

  components: {
    //HelloWorld
  },

  methods: {
    closeMenu: function() {
      closeMenu();
    },
    openMenu: function() {
      openMenu();
    }
  }
}

var closeMenu = function(){
  return document.getElementById("menu").style.display = 'none';
}

var openMenu = function(){
  return document.getElementById("menu").style.display = 'flex';
}
</script>

<style scoped>
/*On large screens like tablet, laptop, large screen laptop ...*/

@media screen and
(min-width: 768px) and
(max-width: 1600px) and
(min-device-width: 768px) and
(max-device-width: 1600px) 
{
  .header {
    display: flex;
    background: #382DB8;
    background-image: url('../assets/images/header-bg-image.svg');
    background-repeat: no-repeat;
    background-position: 115%;
    min-height: 99vh;
    padding-left: 5vw;
  }

  .header .header-content .banner {
    display: flex;
    justify-content: space-between;
    margin: 8vh auto 15vh auto;
    width: 89vw;
  }

  .header .header-content .banner .banner-left .menu {
    display: none;
  }

  .header .header-content .banner .banner-right {
    display: flex;
  }

  .header .header-content .banner .banner-right .logo-close {
    display: none;
  }

  .header .header-content .banner .banner-right span,
  .header .header-content .banner .banner-right a {
    margin: auto 28px auto 0;
    text-decoration: none;
    font-weight: 500;
  }

  .header .header-content .banner .banner-right .ask-service {
    display: none;
  }

  .header .header-content .banner .banner-right a span {
    color: white;
    font-size: 14px;
  }

  .header .header-content .banner .banner-right a button {
    cursor: pointer;
    font-family: 'inter';
    color: white;
    border-radius: 8px;
    font-weight: 500;
    background: transparent;
    border: 1px solid white;
    padding: 11px 14px;
    font-size: 14px;
  }

  .header .header-content .banner .banner-right a .signup {
    background-color: #FFCC30;
    border: 1px solid #FFCC30;
    color: #382DB8;
  }

  .header .header-content .banner .after-banner {
    border: solid 1px red;
  }

  .header .header-content .after-banner {
    color: white;
  }

  .header .header-content .after-banner h1 {
    width: 57vw;
    font-weight: 700;
    font-size: 50px;
  }

  .header .header-content .after-banner h1 span {
    background: #48CAE4;
  }

  .header .header-content .after-banner .first {
    font-size: large;
    font-weight: normal;
  }

  .header .header-content .after-banner .search-bar{
    margin-top: 5px;
    position: relative;
  }

  .header .header-content .after-banner .search-bar .icon {
    position: absolute;
    left: 2.5vw;
    top: 1.8vw;
    font-size: xx-large;
    color: #382DB8;
  }

  .header .header-content .after-banner .search-bar .search {
    height: 12vh;
    width: 73vw;
    border: none;
    border-radius: 18px;
    padding-left: 5.5rem;
    padding-right: 2rem;
    font-size: medium;
    color: #382DB8;
  }

  .header .header-content .after-banner .search-bar .search:focus{
    outline: none;
  }

  ::-webkit-input-placeholder { /* WebKit, Blink, Edge */
      font-size: 12px;
      color: #C4C4C4;
  }
  :-moz-placeholder { /* Mozilla Firefox 4 to 18 */
      font-size: medium;
      color: #382DB8;
      opacity:  0.5;
  }
  ::-moz-placeholder { /* Mozilla Firefox 19+ */
      font-size: medium;
      color: #382DB8;
      opacity:  0.5;
  }
  :-ms-input-placeholder { /* Internet Explorer 10-11 */
      font-size: medium;
      color: #382DB8;
  }
  ::-ms-input-placeholder { /* Microsoft Edge */
      font-size: medium;
      color: #382DB8;
  }
  ::placeholder { /* Most modern browsers support this now. */
      font-size: medium;
      color: #382DB8;
  }

  .header .header-content .after-banner .second {
    font-size: large;
    font-weight: 600;
  }

  .header .header-content .after-banner .services-pop {
    display: flex;
    flex-flow: wrap;
  }

  .header .header-content .after-banner .services-pop span {
    border: 1px solid white;
    border-radius: 10px;
    padding: 10px 12px;
    margin: 5px 20px 5px 0;
  }

  .covid-info {
    display: flex;
    background-color: #48CAE4;
  }

  .covid-info span {
    margin: 2vh auto;
    font-weight: 500;
    color: white;
    display: flex;
  }

  .covid-info span i {
    font-weight: 400;
    font-size: x-large;
    margin: auto 15px;
  }

  .covid-info span .chevron {
    display: none;
  }

  .body {
    padding: 10vh 5vw;
  }

  .informations h1 {
    font-weight: 500;
    font-size: 28px;
  }

  .informations .infos, .informations .infos div {
    display: flex;
    justify-content: space-between;
  }

  .informations .infos div i {
    color: #FFCC30;
    margin: auto 40px;
  }

  .informations .infos div span .title {
    color: #382DB8;
    font-size: xx-large;
    margin-bottom: 15px;
  }

  .informations .infos div span .desc {
    font-weight: 300;
  }
}


/*On small screens like mobiles L, M or S*/

@media screen and
(min-width: 320px) and
(max-width: 767px),
(min-device-width: 320px) and
(max-device-width: 767px) {
  .header {
    display: flex;
    background: #382DB8;
    background-image: url('../assets/images/header-bg-image.svg');
    background-repeat: no-repeat;
    min-height: 99vh;
    width: 90vw;
    padding-left: 5vw;
    padding-right: 5vw;
  }

  .header .header-content .banner {
    display: flex;
    justify-content: space-between;
    margin: 8vh auto 8vh auto;
    width: 89vw;
  }

  .header .header-content .banner .banner-left {
    display: flex;
    justify-content: space-between;
    width: 100%;
  }

  .header .header-content .banner .banner-left img {
    width: 100px;
  }

  .header .header-content .banner .banner-left .menu {
    color: white;
    margin: auto 20px;
  }

  .header .header-content .banner .banner-right {
    display: flex;
    flex-flow: column;
    height: 100vh;
    width: 90vw;
    position: fixed;
    z-index: 10000;
    top: 0;
    left: 0;
    background: #382DB8;
    padding: 5vh 8vw 0 8vw;
  }

  .header .header-content .banner .banner-right .logo-close {
    display: flex;
    justify-content: space-between;
    padding: 5px 25px 0 5px;
  }

  .header .header-content .banner .banner-right .logo-close img {
    width: 100px;
  }

  .header .header-content .banner .banner-right .logo-close i {
    color: white;
  }

  .header .header-content .banner .banner-right .buttons {
    margin-top: auto;
    margin-bottom: 40px;
    margin-left: auto;
    margin-right: auto;
    display: flex;
    flex-flow: column;
  }

  .header .header-content .banner .banner-right .links {
    margin: auto auto auto 0;
    display: flex;
    width: 70vw;
    flex-flow: column;
  }

  .header .header-content .banner .banner-right a {
    margin: auto 28px auto 0;
    text-decoration: none;
    font-weight: 500;
  }

  .header .header-content .banner .banner-right a span {
    color: white;
    font-size: 14px;
  }

  .header .header-content .banner .banner-right a button {
    cursor: pointer;
    font-family: 'inter';
    color: white;
    border-radius: 8px;
    font-weight: 500;
    background: transparent;
    border: 1px solid white;
    padding: 13px 14px;
    font-size: 14px;
    width: 80vw;
    margin: 12px 0;
  }

  .header .header-content .banner .banner-right a .signup {
    background-color: #FFCC30;
    border: 1px solid #FFCC30;
    color: #382DB8;
  }

  .header .header-content .banner .banner-right .links a {
    margin-bottom: 20px;
    margin-top: 20px;
  }

  .header .header-content .banner .banner-right .links span {
    font-size: x-large;
    font-weight: 600;
    margin-bottom: 30px;
  }

  .header .header-content .banner .after-banner {
    border: solid 1px red;
  }

  .header .header-content .after-banner {
    color: white;
  }

  .header .header-content .after-banner h1 {
    width: 85%;
    font-weight: 700;
    margin-bottom: 0;
  }

  .header .header-content .after-banner h1 span {
    background: #48CAE4;
  }

  .header .header-content .after-banner .first {
    font-size: small;
    font-weight: normal;
    margin: 5px 20px 25px 0;
    width: 90%;
  }

  .header .header-content .after-banner .search-bar{
    margin-top: 5px;
    position: relative;
  }

  .header .header-content .after-banner .search-bar .icon {
    position: absolute;
    left: 5%;
    top: 33%;
    font-size: x-large;
    color: #382DB8;
  }

  .header .header-content .after-banner .search-bar .search {
    height: 9vh;
    width: 100%;
    border: none;
    border-radius: 10px;
    padding-left: 3.5rem;
    padding-right: 2rem;
    font-size: smaller;
    color: #382DB8;
  }

  .header .header-content .after-banner .search-bar .search:focus{
    outline: none;
  }

  ::-webkit-input-placeholder { /* WebKit, Blink, Edge */
      font-size: small;
      color: #C4C4C4;
  }
  :-moz-placeholder { /* Mozilla Firefox 4 to 18 */
      font-size: small;
      color: #382DB8;
      opacity:  0.5;
  }
  ::-moz-placeholder { /* Mozilla Firefox 19+ */
      font-size: small;
      color: #382DB8;
      opacity:  0.5;
  }
  :-ms-input-placeholder { /* Internet Explorer 10-11 */
      font-size: small;
      color: #382DB8;
  }
  ::-ms-input-placeholder { /* Microsoft Edge */
      font-size: small;
      color: #382DB8;
  }
  ::placeholder { /* Most modern browsers support this now. */
      font-size: small;
      color: #382DB8;
  }

  .header .header-content .after-banner .second {
    font-size: small;
    font-weight: 600;
  }

  .header .header-content .after-banner .services-pop {
    display: flex;
    flex-flow: row wrap;
  }

  .header .header-content .after-banner .services-pop span {
    border: 1px solid white;
    border-radius: 10px;
    padding: 10px 12px;
    margin: 5px 10px 5px 0;
    font-size: small;
  }

  .covid-info {
    display: flex;
    background-color: #48CAE4;
  }

  .covid-info span {
    margin: 2vh auto;
    font-weight: 500;
    color: white;
    display: flex;
    font-size: x-small;
  }

  .covid-info span i {
    display: none;
  }

  .covid-info span .chevron {
    display: inline;
    font-weight: 400;
    font-size: x-small;
    margin: auto 15px;
  }

  .body {
    padding: 7vh 5vw;
  }

  .informations {
    display: flex;
    flex-flow: column;
  }

  .informations h1 {
    font-weight: 500;
    font-size: large;
    margin: 0 auto;
  }

  .informations .infos, .informations .infos div {
    display: flex;
    flex-flow: column;
    justify-content: space-between;
  }

  .informations .infos div {
    width: 60%;
    display: flex;
    flex-flow: column;
    margin: 15px auto;
  }

  .informations .infos div i {
    display: none;
  }

  .informations .infos div span {
    display: flex;
    flex-flow: column;
  }

  .informations .infos div span .title {
    color: #382DB8;
    font-size: large;
    font-weight: 500;
    margin-bottom: 5px;
    text-align: center;
  }

  .informations .infos div span .desc {
    font-weight: 300;
    font-size: small;
    margin-top: 0;
    text-align: center;
  }
}

</style>