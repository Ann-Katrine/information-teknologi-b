<template>
    <div>
        <div id="forside">
            <nav id="navbar">
                <ul class="menu">
                    <li>
                        <a href="#hero" class="navOverskift">IntelRobotics</a>
                    </li>
                    <li v-show="showNotNavbarThings">
                        <a href="#produkt" @click="test()" class="underOverskift">Produkt</a>
                    </li>
                    <li v-show="showNotNavbarThings">
                        <a href="#kontakt" class="underOverskift">Kontakt</a>
                    </li>
                    <li v-show="showNotNavbarThings">
                        <select>
                          <option>Japansk                           
                          </option>
                          <option>Engelsk</option>
                          <option>Canadisk</option>
                          <option>Danmark</option>
                        </select>
                    </li>
                    <li v-show="showNavbarButton" class="navbarBtn">
                      <button @click="openNavbar()" class="navbarBtn">
                        <ion-icon class="navbar-icon" name="menu-outline"></ion-icon>
                      </button>
                    </li>
                </ul>
            </nav>
            <div id="hero">
                <div class="heroBoks">
                    <div class="heroUnderBoks1">
                      <img src="https://www.universal-robots.com/media/1803486/ur3-collaborative-table-top-robot-filter1.jpg" class="heroimages">
                    </div>
                    <div v-show="heroSite2" class="heroUnderBoks2">
                    </div>
                </div>
                <h1 class="heroOverskift">IntelRobotics</h1>
            </div>
            <div ref="produkt" id="produkt" class="produktBoks">
                <h2 class="underHeroOverskift">Produkter</h2>

                <!-- <div class="threeProduktUnderBoks" v-for="product in allProduct" :key="product.id">
                    <div class="produktBoks1">
                      <button @click="openModal()" class="produktImages">
                          <img :src="product." :alt="product." class="produktImages1">

                          <div class="produktBanner">
                              <p class="produktBannerOverskrift"> {{ product.name }} </p>
                              <p class="produktBannerOverskrift produktBannerTekstEnd"> {{ product.price }} </p>
                          </div>
                      </button>
                    </div>
                </div> -->
                
                <div class="threeProduktUnderBoks">
                    <div class="produktBoks1">
                      <button @click="openModal()" class="produktImages">
                          <img src="https://www.universal-robots.com/media/1800754/universal-robots-plus-a-robotics-ecosystem.jpg" class="produktImages1">

                          <div class="produktBanner">
                              <p class="produktBannerOverskrift">produkt</p>
                              <p class="produktBannerOverskrift produktBannerTekstEnd">pris</p>
                          </div>
                      </button>
                    </div>
                    <div class="produktBoks2">
                        <button @click="openModal()" class="produktImages">
                          <img src="https://www.universal-robots.com/img/product1.png" class="produktImages1">

                          <div class="produktBanner">
                              <p class="produktBannerOverskrift">produkt</p>
                              <p class="produktBannerOverskrift produktBannerTekstEnd">pris</p>
                          </div>
                      </button>
                    </div>
                    <div class="produktBoks3">
                        <button @click="openModal()" class="produktImages">
                          <img src="https://www.universal-robots.com/img/product2.png" class="produktImages1">

                          <div class="produktBanner">
                              <p class="produktBannerOverskrift">produkt</p>
                              <p class="produktBannerOverskrift produktBannerTekstEnd">pris</p>
                          </div>
                      </button>
                    </div>
                    <div class="produktBoks4">
                        <button @click="openModal()" class="produktImages">
                          <img src="https://www.universal-robots.com/img/product3.png" class="produktImages1">

                          <div class="produktBanner">
                              <p class="produktBannerOverskrift">produkt</p>
                              <p class="produktBannerOverskrift produktBannerTekstEnd">pris</p>
                          </div>
                      </button>
                    </div>
                    <div class="produktBoks5">
                        <button @click="openModal()" class="produktImages">
                          <img src="https://www.universal-robots.com/img/product4.png" class="produktImages1">

                          <div class="produktBanner">
                              <p class="produktBannerOverskrift">produkt</p>
                              <p class="produktBannerOverskrift produktBannerTekstEnd">pris</p>
                          </div>
                      </button>
                    </div>
                    <div class="produktBoks6">
                        <button @click="openModal()" class="produktImages">
                          <img src="https://www.universal-robots.com/img/product5.png" class="produktImages1">

                          <div class="produktBanner">
                              <p class="produktBannerOverskrift">produkt</p>
                              <p class="produktBannerOverskrift produktBannerTekstEnd">pris</p>
                          </div>
                      </button>
                    </div>
                </div>
            </div>
            <div id="kontakt" class="kontaktBoks">
                <h2 class="underHeroOverskift">Kontakt</h2>

                <!-- <div class="threeKontaktUnderBoks" v-for="info in allKontaktInfo" :key="info.id">
                    <div>
                        <p class="kontaktUnderBoksOverskift"> {{ info.country }} {{ info.name }} </p>
                        <p class="kontaktUnderBoksUnderOverskrift"> {{ info.address }} </p>
                        <p class="kontaktUnderBoksUnderOverskrift"> {{ info.city }} og {{ info.postalcode }} </p>
                        <p class="kontaktUnderBoksUnderOverskrift"> {{ info.e-mail }} </p>
                        <p class="kontaktUnderBoksUnderOverskrift"> {{ info.phonenumber }} </p>
                    </div>
                </div> -->

                <div class="threeKontaktUnderBoks">
                    <div class="threeKontaktTekstSpace">
                        <p class="kontaktUnderBoksOverskift">Danmark</p>
                        <p class="kontaktUnderBoksUnderOverskrift">Vejnavn</p>
                        <p class="kontaktUnderBoksUnderOverskrift">by og postnr</p>
                        <p class="kontaktUnderBoksUnderOverskrift">mail</p>
                        <p class="kontaktUnderBoksUnderOverskrift">telefon nr.</p>
                    </div>
                    <div class="threeKontaktTekstSpace">
                        <p class="kontaktUnderBoksOverskift">Japan</p>
                        <p class="kontaktUnderBoksUnderOverskrift">Vejnavn</p>
                        <p class="kontaktUnderBoksUnderOverskrift">by og postnr</p>
                        <p class="kontaktUnderBoksUnderOverskrift">mail</p>
                        <p class="kontaktUnderBoksUnderOverskrift">telefon nr.</p>
                    </div>
                    <div class="threeKontaktTekstSpace">
                        <p class="kontaktUnderBoksOverskift">Canada</p>
                        <p class="kontaktUnderBoksUnderOverskrift">Vejnavn</p>
                        <p class="kontaktUnderBoksUnderOverskrift">by og postnr</p>
                        <p class="kontaktUnderBoksUnderOverskrift">mail</p>
                        <p class="kontaktUnderBoksUnderOverskrift">telefon nr.</p>
                    </div>
                </div>
            </div>
        </div>

        <ShowProduct>
          <div class="billdeBoks">
            <button class="billedeBtn">
              <ion-icon name="chevron-back-outline" class="close-ikon"></ion-icon>
            </button>
            <img src="https://www.universal-robots.com/media/1803486/ur3-collaborative-table-top-robot-filter1.jpg" class="billedeSize">
            <button class="billedeBtn">
              <ion-icon name="chevron-forward-outline" class="close-ikon"></ion-icon>
            </button>
          </div>
          <div class="modal-circle-box">
            <div class="modal-circles"></div>
          </div>
          <h2 class="modalOverskrift modaltekstMellemrum">Projekt navn</h2>
          <h3 class="modalUnderOverskrift modaltekstMellemrum">Pris 100.000 kr.</h3>
          <p class="modalBeardText">tester 1 2 3...</p>
        
          <!-- <div class="billdeBoks">
            <button>
              <ion-icon name="chevron-back-outline" class="close-ikon"></ion-icon>
            </button>
            <img src="https://www.universal-robots.com/media/1803486/ur3-collaborative-table-top-robot-filter1.jpg" class="billedeSize">
            <button>
              <ion-icon name="chevron-forward-outline" class="close-ikon"></ion-icon>
            </button>
          </div>
          <div class="modal-circle-box">
            <div class="modal-circles"></div>
          </div>
          <h2 class="modalOverskrift modaltekstMellemrum"> {{ oneProduct.name }}</h2>
          <h3 class="modalUnderOverskrift modaltekstMellemrum"> {{ oneProduct.price }} </h3>
          <p class="modalBeardText"> {{ oneProduct.description }} </p> -->
        
        </ShowProduct>
        <Navbar></Navbar>
  </div>
</template>

<script>
  import eventBus from '../eventBus'
  import axios from 'axios'
  import ShowProduct from '../components/showProduct.vue';
  import Navbar from '../components/navbarModal.vue'

  export default {
    name: 'forside',
    data(){
      return{
        allProduct: [],
        allKontaktInfo: [],
        oneProduct: [],
        showNavbarButton: false,
        showNotNavbarThings: true,
        heroSite2: true
      }
    },
    components:{
      ShowProduct,
      Navbar
    },
    created(){
      this.stickNavbar();
      /*this.getAllProducs();
      this.getAllKontaktInfo();
      this.getOneProduct();*/
    },
    mounted(){
      this.$nextTick(function() {
        window.addEventListener('resize', this.getWindowWidth);
        //Init
        this.getWindowWidth()
      })
      window.addEventListener('scroll', this.stickNavbar) // laver en event til når man scroller
    },
    methods:{
      stickNavbar(){
        let navbar = document.getElementById("navbar");
        let forside = document.getElementById("forside");
        let heroSektion = document.getElementById("hero");

        // Bruger eventer scroll for at se hvornår man rækker sig op eller ned på siden
        if(window.scrollY > 0){
          navbar.classList.add("sticky");
          forside.classList.add("strickyForsideHeigth");
          heroSektion.classList.add("heroBoksExtraPlads");
        }
        else{
          navbar.classList.remove("sticky");
          forside.classList.remove("strickyForsideHeigth");
          heroSektion.classList.remove("heroBoksExtraPlads");
        }
      },
      offSetAnchor(){
        var element = this.$refs["produkt"];
        var top = element.offsetTop - 83;

        window.scrollTo(0, top);
      },
      test() {
        window.setTimeout(() => {
          this.offSetAnchor();
        }, 0);
      },
      getAllProducs(){
        axios
          .get('')
          .then(Response => {
            this.allProduct = response.data
          })
          .catch(err => {
            console.log(err.toString());
          })
      },
      getAllKontaktInfo(){
        axios
          .get('',)
          .then(Response => {
            this.allKontaktInfo = response.data
          })
          .catch(err => {
            console.log(err.toString());
          })  
      },
      getOneProduct(){
        axios
          .get('')
          .then(Response => {
            this.oneProduct = response.data
          })
          .catch(err => {
            console.log(err.toString());
          })
      },
      openModal(){ // åbner modalen der vister info om den enkenlte projekt
        // console.log(id)
        // this.getOneProjekt(id)
        console.log("vriker")
        eventBus.$emit("showModal", true)
      },
      openNavbar(){
        console.log("vriker");
        eventBus.$emit("showNavbar", true)
      },
      getWindowWidth(event) { // for skærm størrelsen
        this.windowswidth = window.innerWidth;

        if(this.windowswidth < 769){
          this.showNavbarButton = true;
          this.showNotNavbarThings = false;
          this.heroSite2 = false;
        }
        else{
          this.showNavbarButton = false;
          this.showNotNavbarThings = true;
          this.heroSite2 = true;
        }
      }
    }
  }
</script>

<style>
  /*********************************************************************************************************/
  /*                                            Det generelt design                                        */
  /*********************************************************************************************************/
  body{
    background-color: #E4E4E4;
  }

  /*************************************************/
  /*                    Navbar                     */
  /*************************************************/
  nav{
    background-color: #968787; 
    height: 78px;     
  }

  .menu{
    display: block;
    width: 100%;
    height: 1em;
    padding: 0;
    padding-bottom: 5%;
  }

  ul{ 
    margin: 0;
    padding: 0;
    list-style-type: none; /* så a-tags prikker ikke bliver vist*/
  }

  li{
    display: inline; /* den bruger når man er på IE6-7 for der virker inline-block ikke*/
    position: relative;
  }

  li a{
    display: inline-block; /* går at linkene ikke begynder at sætte sig under hinanden */
    padding: 0.4em;
    text-decoration: none;
    font-size: 1.3em;
  }

  .navOverskift{
    font-size: 2.7em;
    color: #000;
  }

  .underOverskift{
    font-size: 1.7em;
    color: #000;
  }

  .sticky{
    position: fixed;
    top: 0;
    width: 100%;
	z-index: 1;
  }

  .strickyForsideHeigth{
    height: 6em;
  }

  .navbarBtn{
    background-color: transparent;
    border: none;
  }

  /*************************************************/
  /*                    hero                       */
  /*************************************************/

  .heroBoksExtraPlads{
    margin: 79px 0 0 0;
  }

  .heroOverskift{
    position: absolute;
    font-size: 6em;
    background-color: #CCDAE3;
    margin: -4.5em 0 3.5em 0em;
    right: 0px;

    padding: 10px 40px 20px 20px;
  }

  .heroBoks{
    display: flex;
  }

  .heroUnderBoks1{
    height: 36.2em;
    flex: 70%;
  }

  .heroUnderBoks2{
    padding: 2em 0 0 0;
    flex: 30%;
  }

  .underHeroOverskift{
    font-size: 2em;
    padding: 0.5em 0 0.5em 2em;
  }

  .produktBanner{
    display: flex;
    position: absolute;
    background-color: crimson;
    height: 1em;
    width: 1em;
  }

  .heroimages{
    /* width: 59em;
    height: 36em; */
    width: 100%;
    height: 100%;
  }

  /*************************************************/
  /*                  produkter                    */
  /*************************************************/

  .produktBoks{
    height: 38em;
  }

    .threeProduktUnderBoks{
        display: flex;
        flex-wrap: wrap;
    }

    .produktBoks1{
        padding: 1em 0 0 13.6em;
    }

    .produktBoks2{
        padding: 1em 6em 0 6em;
    }

    .produktBoks3{
        padding: 1em 13.6em 0 0;
    }

    .produktBoks4{
        padding: 6em 0 0 13.6em;
    }

    .produktBoks5{
        padding: 6em 6em 0 6em;
    }

    .produktBoks6{
        padding: 6em 13.6em 0 0;
    }

    .produktImages{
      height: 14.3em;
      width: 18em;
      border: 1px solid #000;
    }

    .produktBanner{
      display: flex;
      justify-content: space-between;
      position: absolute;
      background-color: #CCDAE3;
      height: 2em;
      width: 16.1em;
      padding: 5px 11px;
      margin: -3.5em 0 0 -0.4em;
    }

    .produktBannerOverskrift{
      font-size: 1.5em;
    }

    .produktImages1{
      height: 100%;
      width: 100%;
    }

  /*************************************************/
  /*                   kontakt                     */
  /*************************************************/

  .kontaktBoks{
    height: 14em;
    background-color: #968787;
  }

  .threeKontaktUnderBoks{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
  }

  .kontaktUnderBoksOverskift{
    font-size: 1.5em;

  }

  .kontaktUnderBoksUnderOverskrift{
    font-size: 1.2em;
  }
</style>

<style>
  /*********************************************************************************************************/
  /*                                            Responsiv                                                  */
  /*********************************************************************************************************/
  /*************************************************/
  /*                   Computer                    */
  /*************************************************/
  @media screen and (max-width: 1360px){
    .produktBoks3 {
      padding: 1em 13.3em 0 0;
    }

    .produktBoks6 {
      padding: 6em 13.3em 0 0;
    }
  }

  @media screen and (max-width: 1359px){
    .produktBoks3 {
      padding: 1em 12.5em 0 0;
    }

    .produktBoks6 {
      padding: 6em 12.5em 0 0;
    }
  }

  @media screen and (max-width: 1347px){
    .produktBoks1 {
      padding: 1em 0 0 12.5em;
    }

    .produktBoks3 {
      padding: 1em 12.5em 0 0;
    }

    .produktBoks4 {
      padding: 6em 0 0 12.5em;
    }

    .produktBoks6 {
      padding: 6em 12.5em 0 0;
    }
  }

  @media screen and (max-width: 1330px){
    .produktBoks1 {
      padding: 1em 0 0 12.5em;
    }

    .produktBoks3 {
      padding: 1em 12.5em 0 0;
    }

    .produktBoks4 {
      padding: 6em 0 0 12.5em;
    }

    .produktBoks6 {
      padding: 6em 12.5em 0 0;
    }
  }

  @media screen and (max-width: 1328px){
    .produktBoks2{
      padding: 1em 5.7em 0 5.7em;
    }

    .produktBoks4 {
      padding: 5em 0 0 12.5em;
    }

    .produktBoks5 {
      padding: 5em 5.7em 0 5.7em;
    }

    .produktBoks6 {
      padding: 5em 12.5em 0 0;
    }
  }

  @media screen and (max-width: 1319px){
    .produktBoks2{
      padding: 1em 5.4em 0 5.4em;
    }

    .produktBoks5 {
      padding: 5em 5.4em 0 5.4em;
    }
  }

  @media screen and (max-width: 1309px){
    .produktBoks1 {
      padding: 1em 0 0 12em;
    }

    .produktBoks3 {
      padding: 1em 12em 0 0;
    }

    .produktBoks4 {
      padding: 5em 0 0 12em;
    }

    .produktBoks6 {
      padding: 5em 12em 0 0;
    }
  }

  @media screen and (max-width: 1293px){
    .produktBoks1 {
      padding: 1em 0 0 11.8em;
    }

    .produktBoks3 {
      padding: 1em 11.8em 0 0;
    }

    .produktBoks4 {
      padding: 5em 0 0 11.8em;
    }

    .produktBoks6 {
      padding: 5em 11.8em 0 0;
    }
  }

  @media screen and (max-width: 1287px){
    .produktBoks1 {
      padding: 1em 0 0 11.5em;
    }

    .produktBoks3 {
      padding: 1em 11.5em 0 0;
    }

    .produktBoks4 {
      padding: 5em 0 0 11.5em;
    }

    .produktBoks6 {
      padding: 5em 11.5em 0 0;
    }
  }  

  @media screen and (max-width: 1277px){
    .produktBoks1 {
      padding: 1em 0 0 11em;
    }

    .produktBoks3 {
      padding: 1em 11em 0 0;
    }

    .produktBoks4 {
      padding: 5em 0 0 11em;
    }

    .produktBoks6 {
      padding: 5em 11em 0 0;
    }
  }

  @media screen and (max-width: 1261px){
    .produktBoks1 {
      padding: 1em 0 0 11em;
    }

    .produktBoks2{
      padding: 1em 5.3em 0 5.3em;
    }

    .produktBoks3 {
      padding: 1em 11em 0 0;
    }

    .produktBoks4 {
      padding: 5em 0 0 11em;
    }

    .produktBoks5 {
      padding: 5em 5.3em 0 5.3em;
    }

    .produktBoks6 {
      padding: 5em 11em 0 0;
    }
  }

  @media screen and (max-width: 1258px){
    .produktBoks1 {
      padding: 1em 0 0 10.5em;
    }

    .produktBoks2{
      padding: 1em 5.2em 0 5.2em;
    }

    .produktBoks3 {
      padding: 1em 10.5em 0 0;
    }

    .produktBoks4 {
      padding: 4.8em 0 0 10.5em;
    }

    .produktBoks5 {
      padding: 4.8em 5.2em 0 5.2em;
    }

    .produktBoks6 {
      padding: 4.8em 10.5em 0 0;
    }
  }

  @media screen and (max-width: 1240px){
    .produktBoks1 {
      padding: 1em 0 0 10.5em;
    }

    .produktBoks2{
      padding: 1em 4.7em 0 4.7em;
    }

    .produktBoks3 {
      padding: 1em 10.5em 0 0;
    }

    .produktBoks4 {
      padding: 4.8em 0 0 10.5em;
    }

    .produktBoks5 {
      padding: 4.8em 4.7em 0 4.7em;
    }

    .produktBoks6 {
      padding: 4.8em 10.5em 0 0;
    }
  }

  @media screen and (max-width: 1223px){
    .produktBoks1 {
      padding: 1em 0 0 10.3em;
    }

    .produktBoks3 {
      padding: 1em 10.3em 0 0;
    }

    .produktBoks4 {
      padding: 4.8em 0 0 10.3em;
    }

    .produktBoks6 {
      padding: 4.8em 10.3em 0 0;
    }
  }

  @media screen and (max-width: 1216px){
    .produktBoks1 {
      padding: 1em 0 0 10em;
    }

    .produktBoks3 {
      padding: 1em 10em 0 0;
    }

    .produktBoks4 {
      padding: 4.8em 0 0 10em;
    }

    .produktBoks6 {
      padding: 4.8em 10em 0 0;
    }
  }

  @media screen and (max-width: 1207px){
    .heroOverskift {
      font-size: 5.7em;
    }

    .produktBoks1 {
      padding: 1em 0 0 9.5em;
    }

    .produktBoks3 {
      padding: 1em 9.5em 0 0;
    }

    .produktBoks4 {
      padding: 4.8em 0 0 9.5em;
    }

    .produktBoks6 {
      padding: 4.8em 9.5em 0 0;
    }
  }

  @media screen and (max-width: 1191px){
    .heroOverskift {
      font-size: 5.7em;
    }

    .produktBoks1 {
      padding: 1em 0 0 9.4em;
    }

    .produktBoks3 {
      padding: 1em 9.4em 0 0;
    }

    .produktBoks4 {
      padding: 4.8em 0 0 9.4em;
    }

    .produktBoks6 {
      padding: 4.8em 9.4em 0 0;
    }
  }

  @media screen and (max-width: 1189px){
    .produktBoks1 {
      padding: 1em 0 0 9em;
    }

    .produktBoks2{
      padding: 1em 4.6em 0 4.6em;
    }


    .produktBoks3 {
      padding: 1em 9em 0 0;
    }

    .produktBoks4 {
      padding: 4.7em 0 0 9em;
    }

    .produktBoks5 {
      padding: 4.7em 4.6em 0 4.6em;
    }

    .produktBoks6 {
      padding: 4.7em 9em 0 0;
    }
  }

  @media screen and (max-width: 1172px){
    .produktBoks1 {
      padding: 1em 0 0 9em;
    }

    .produktBoks2{
      padding: 1em 4.5em 0 4.5em;
    }

    .produktBoks3 {
      padding: 1em 9em 0 0;
    }

    .produktBoks4 {
      padding: 4.3em 0 0 9em;
    }

    .produktBoks5 {
      padding: 4.3em 4.5em 0 4.5em;
    }

    .produktBoks6 {
      padding: 4.3em 9em 0 0;
    }
  }

  @media screen and (max-width: 1168px){
    .produktBoks1 {
      padding: 1em 0 0 8.5em;
    }

    .produktBoks3 {
      padding: 1em 8.5em 0 0;
    }

    .produktBoks4 {
      padding: 4.3em 0 0 8.5em;
    }

    .produktBoks6 {
      padding: 4.3em 8.5em 0 0;
    }
  }

  @media screen and (max-width: 1152px){
    .produktBoks1 {
      padding: 1em 0 0 8.3em;
    }

    .produktBoks3 {
      padding: 1em 8.3em 0 0;
    }

    .produktBoks4 {
      padding: 4.3em 0 0 8.3em;
    }

    .produktBoks6 {
      padding: 4.3em 8.3em 0 0;
    }
  }
  
  @media screen and (max-width: 1146px){
    .produktBoks1 {
      padding: 1em 0 0 8em;
    }

    .produktBoks2{
      padding: 1em 4em 0 4em;
    }

    .produktBoks3 {
      padding: 1em 8em 0 0;
    }

    .produktBoks4 {
      padding: 4em 0 0 8em;
    }

    .produktBoks5 {
      padding: 4em 4em 0 4em;
    }

    .produktBoks6 {
      padding: 4em 8em 0 0;
    }
  }

  @media screen and (max-width: 1120px){
    .produktBoks1 {
      padding: 1em 0 0 7.9em;
    }

    .produktBoks3 {
      padding: 1em 7.9em 0 0;
    }

    .produktBoks4 {
      padding: 4em 0 0 7.9em;
    }

    .produktBoks6 {
      padding: 4em 7.9em 0 0;
    }
  }

  @media screen and (max-width: 1117px){
    .heroOverskift {
      font-size: 5.5em;
    }

    .produktBoks1 {
      padding: 1em 0 0 7.5em;
    }

    .produktBoks3 {
      padding: 1em 7.5em 0 0;
    }

    .produktBoks4 {
      padding: 4em 0 0 7.5em;
    }

    .produktBoks6 {
      padding: 4em 7.5em 0 0;
    }
  }

  @media screen and (max-width: 1104px){
    .produktBoks1 {
      padding: 1em 0 0 8.5em;
    }

    .produktBoks2{
      padding: 1em 3.5em 0 3.5em;
    }

    .produktBoks3 {
      padding: 1em 7.5em 0 0;
    }

    .produktBoks4 {
      padding: 3.5em 0 0 8.5em;
    }

    .produktBoks5 {
      padding: 3.5em 3.5em 0 3.5em;
    }

    .produktBoks6 {
      padding: 3.5em 7.5em 0 0;
    }

    .produktImages {
      height: 13.6em;
      width: 17.3em;
    }

    .produktBanner {
      height: 2em;
      width: 15.5em;
    }
  }

  @media screen and (max-width: 1076px){
    .produktBoks1 {
      padding: 1em 0 0 8em;
    }

    .produktBoks2{
      padding: 1em 3.5em 0 3.5em;
    }

    .produktBoks3 {
      padding: 1em 7em 0 0;
    }

    .produktBoks4 {
      padding: 3.5em 0 0 8em;
    }

    .produktBoks5 {
      padding: 3.5em 3.5em 0 3.5em;
    }

    .produktBoks6 {
      padding: 3.5em 7em 0 0;
    }
  }

  @media screen and (max-width: 1060px){
    .produktBoks1 {
      padding: 1em 0 0 7.5em;
    }

    .produktBoks2{
      padding: 1em 3.4em 0 3.4em;
    }

    .produktBoks3 {
      padding: 1em 6.5em 0 0;
    }

    .produktBoks4 {
      padding: 3.4em 0 0 7.5em;
    }

    .produktBoks5 {
      padding: 3.4em 3.4em 0 3.4em;
    }

    .produktBoks6 {
      padding: 3.4em 6.5em 0 0;
    }
  }

  @media screen and (max-width: 1042px){
    .produktBoks1 {
      padding: 1em 0 0 7em;
    }

    .produktBoks2{
      padding: 1em 3.4em 0 3.4em;
    }

    .produktBoks3 {
      padding: 1em 6em 0 0;
    }

    .produktBoks4 {
      padding: 3.4em 0 0 7em;
    }

    .produktBoks5 {
      padding: 3.4em 3.4em 0 3.4em;
    }

    .produktBoks6 {
      padding: 3.4em 6em 0 0;
    }
  }

  @media screen and (max-width: 1025px){
    .produktBoks1 {
      padding: 1em 0 0 7em;
    }

    .produktBoks2{
      padding: 1em 3.2em 0 3.2em;
    }

    .produktBoks3 {
      padding: 1em 5.5em 0 0;
    }

    .produktBoks4 {
      padding: 3.2em 0 0 7em;
    }

    .produktBoks5 {
      padding: 3.2em 3.2em 0 3.2em;
    }

    .produktBoks6 {
      padding: 3.2em 5.5em 0 0;
    }

    .produktImages {
      height: 13em;
      width: 16.7em;
    }

    .produktBanner {
      width: 14.9em;
    }
  }

  @media screen and (max-width: 987px){
    .produktBoks1 {
      padding: 1em 0 0 6.5em;
    }

    .produktBoks2{
      padding: 1em 3.2em 0 3.2em;
    }

    .produktBoks3 {
      padding: 1em 5em 0 0;
    }

    .produktBoks4 {
      padding: 3.2em 0 0 6.5em;
    }

    .produktBoks5 {
      padding: 3.2em 3.2em 0 3.2em;
    }

    .produktBoks6 {
      padding: 3.2em 5em 0 0;
    }

    .produktImages {
      height: 13em;
      width: 16.7em;
    }

    .produktBanner {
      width: 14.9em;
    }
  }

  @media screen and (max-width: 971px){
    .produktBoks1 {
      padding: 1em 0 0 6em;
    }

    .produktBoks2{
      padding: 1em 3.2em 0 3.2em;
    }

    .produktBoks3 {
      padding: 1em 4.5em 0 0;
    }

    .produktBoks4 {
      padding: 3.2em 0 0 6em;
    }

    .produktBoks5 {
      padding: 3.2em 3.2em 0 3.2em;
    }

    .produktBoks6 {
      padding: 3.2em 4.5em 0 0;
    }

    .produktImages {
      height: 13em;
      width: 16.7em;
    }

    .produktBanner {
      width: 14.9em;
    }
  }

  @media screen and (max-width: 955px){
    .produktBoks1 {
      padding: 1em 0 0 6.5em;
    }

    .produktBoks2{
      padding: 1em 3em 0 3em;
    }

    .produktBoks3 {
      padding: 1em 5em 0 0;
    }

    .produktBoks4 {
      padding: 3em 0 0 6.5em;
    }

    .produktBoks5 {
      padding: 3em 3em 0 3em;
    }

    .produktBoks6 {
      padding: 3em 5em 0 0;
    }

    .produktImages {
      height: 12.6em;
      width: 16.3em;
    }

    .produktBanner {
      width: 14.4em;
    }
  }

  @media screen and (max-width: 948px){
    .heroOverskift {
      font-size: 5em;
      margin: -431px 0 3.5em 0;
    }

    .produktBoks1 {
      padding: 1em 0 0 5.5em;
    }

    .produktBoks2{
      padding: 1em 3em 0 3em;
    }

    .produktBoks3 {
      padding: 1em 5em 0 0;
    }

    .produktBoks4 {
      padding: 3em 0 0 5.5em;
    }

    .produktBoks5 {
      padding: 3em 3em 0 3em;
    }

    .produktBoks6 {
      padding: 3em 5em 0 0;
    }

    .produktImages {
      height: 12.6em;
      width: 16.3em;
    }

    .produktBanner {
      width: 14.4em;
    }
  }

  @media screen and (max-width: 932px){
    .heroOverskift {
      font-size: 4.8em;
      margin: -431px 0 3.5em 0;
    }

    .produktBoks1 {
      padding: 1em 0 0 5em;
    }

    .produktBoks2{
      padding: 1em 3em 0 3em;
    }

    .produktBoks3 {
      padding: 1em 4.5em 0 0;
    }

    .produktBoks4 {
      padding: 3em 0 0 5em;
    }

    .produktBoks5 {
      padding: 3em 3em 0 3em;
    }

    .produktBoks6 {
      padding: 3em 4.5em 0 0;
    }
  }

  @media screen and (max-width: 916px){
    .produktBoks1 {
      padding: 1em 0 0 4.5em;
    }

    .produktBoks2{
      padding: 1em 3em 0 3em;
    }

    .produktBoks3 {
      padding: 1em 4em 0 0;
    }

    .produktBoks4 {
      padding: 3em 0 0 4.5em;
    }

    .produktBoks5 {
      padding: 3em 3em 0 3em;
    }

    .produktBoks6 {
      padding: 3em 4em 0 0;
    }
  }

  @media screen and (max-width: 900px){
    .produktBoks1 {
      padding: 1em 0 0 5.5em;
    }

    .produktBoks2{
      padding: 1em 3em 0 3em;
    }

    .produktBoks3 {
      padding: 1em 4em 0 0;
    }

    .produktBoks4 {
      padding: 3em 0 0 5.5em;
    }

    .produktBoks5 {
      padding: 3em 3em 0 3em;
    }

    .produktBoks6 {
      padding: 3em 4em 0 0;
    }

    .produktImages {
      height: 11.7em;
      width: 15.3em;
    }

    .produktBanner {
      width: 13.4em;
    }
  }

  @media screen and (max-width: 876px){
    .produktBoks1 {
      padding: 1em 0 0 5em;
    }

    .produktBoks2{
      padding: 1em 3em 0 3em;
    }

    .produktBoks3 {
      padding: 1em 3.5em 0 0;
    }

    .produktBoks4 {
      padding: 3em 0 0 5em;
    }

    .produktBoks5 {
      padding: 3em 3em 0 3em;
    }

    .produktBoks6 {
      padding: 3em 3.5em 0 0;
    }
  }

  @media screen and (max-width: 860px){
    .produktBoks {
      height: 59em;
    }

    .produktBoks1 {
      padding: 1em 0 0 8em;
    }

    .produktBoks2{
      padding: 1em 0 0 6em;
    }

    .produktBoks3 {
      padding: 5em 0 0 8em;
    }

    .produktBoks4 {
      padding: 5em 0 0 6em;
    }

    .produktBoks5 {
      padding: 5em 0 0 8em;
    }

    .produktBoks6 {
      padding: 5em 0 0 6em;
    }

    .produktImages {
      height: 16em;
      width: 19.3em;
    }

    .produktBanner {
      width: 17.4em;
    }
  }

  @media screen and (max-width: 830px){
    .heroOverskift {
      font-size: 4.5em;
      margin: -401px 0 3.5em 0;
    }

    .produktBoks {
      height: 59em;
    }

    .produktBoks1 {
      padding: 1em 0 0 7.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 5.5em;
    }

    .produktBoks3 {
      padding: 5em 0 0 7.5em;
    }

    .produktBoks4 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks5 {
      padding: 5em 0 0 7.5em;
    }

    .produktBoks6 {
      padding: 5em 0 0 5.5em;
    }

    .produktImages {
      height: 16em;
      width: 19.3em;
    }

    .produktBanner {
      width: 17.4em;
    }
  }

  @media screen and (max-width: 818px){
    .indre-modal{
      height: 100%;
      width: 100%;
      border-radius: 0;
      max-height: none;
    }
  }

  @media screen and (max-width: 810px){
    .produktBoks1 {
      padding: 1em 0 0 6.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 5.5em;
    }

    .produktBoks3 {
      padding: 5em 0 0 6.5em;
    }

    .produktBoks4 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks5 {
      padding: 5em 0 0 6.5em;
    }

    .produktBoks6 {
      padding: 5em 0 0 5.5em;
    }
  }

  @media screen and (max-width: 800px){
    .produktBoks {
      height: 58.7em;
    }

    .produktBoks1 {
      padding: 1em 0 0 5.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 5.5em;
    }

    .produktBoks3 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks4 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks5 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks6 {
      padding: 5em 0 0 5.5em;
    }

    .billedeSize {
      height: 13em;
      width: 34.5em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 5.5em;
    }
  }

  @media screen and (max-width: 790px){
    .produktBoks1 {
      padding: 1em 0 0 5.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 5.5em;
    }

    .produktBoks3 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks4 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks5 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks6 {
      padding: 5em 0 0 5.5em;
    }
  }

  @media screen and (max-width: 780px){
    .produktBoks1 {
      padding: 1em 0 0 5em;
    }

    .produktBoks2{
      padding: 1em 0 0 5.5em;
    }

    .produktBoks3 {
      padding: 5em 0 0 5em;
    }

    .produktBoks4 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks5 {
      padding: 5em 0 0 5em;
    }

    .produktBoks6 {
      padding: 5em 0 0 5.5em;
    }

    .billedeSize {
      height: 13em;
      width: 34em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 5em;
    }
  }

  @media screen and (max-width: 770px){
    .produktBoks {
      height: 58.5em;
    }

    .produktBoks1 {
      padding: 1em 0 0 5em;
    }

    .produktBoks2{
      padding: 1em 0 0 5.5em;
    }

    .produktBoks3 {
      padding: 5em 0 0 5em;
    }

    .produktBoks4 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks5 {
      padding: 5em 0 0 5em;
    }

    .produktBoks6 {
      padding: 5em 0 0 5.5em;
    }
  }

  /*************************************************/
  /*                    tabelt                     */
  /*************************************************/
  @media screen and (max-width: 768px){
    .heroOverskift {
    }

    .heroimages {
      height: 83%;
    }

    .heroOverskift {
      right: 17%;
      padding: 10px 20px 20px 20px; 
    }

    .menu{
      display: flex;
      justify-content: space-between;
      align-items: baseline;
    }

    .produktBoks1 {
      padding: 1em 0 0 5em;
    }

    .produktBoks2{
      padding: 1em 0 0 5.5em;
    }

    .produktBoks3 {
      padding: 5em 0 0 5em;
    }

    .produktBoks4 {
      padding: 5em 0 0 5.5em;
    }

    .produktBoks5 {
      padding: 5em 0 0 5em;
    }

    .produktBoks6 {
      padding: 5em 0 0 5.5em;
    }

    .billedeSize {
      height: 13em;
      width: 30em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 5em;
    }
  }

  @media screen and (max-width: 750px){
    .produktBoks1 {
      padding: 1em 0 0 4.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 5em;
    }

    .produktBoks3 {
      padding: 5em 0 0 4.5em;
    }

    .produktBoks4 {
      padding: 5em 0 0 5em;
    }

    .produktBoks5 {
      padding: 5em 0 0 4.5em;
    }

    .produktBoks6 {
      padding: 5em 0 0 5em;
    }
  }

  @media screen and (max-width: 740px){
    .produktBoks {
      height: 58em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 4.5em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4.5em;
    }

    .billedeSize {
      height: 13em;
      width: 29.5em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4.5em;
    }
  }

  @media screen and (max-width: 730px){
    .produktBoks {
      height: 58em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4em;
    }

    .produktBoks2{
      padding: 1em 0 0 4.5em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4.5em;
    }
  }

  @media screen and (max-width: 720px){
    .produktBoks {
      height: 57.1em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4.1em;
    }

    .produktBoks2{
      padding: 1em 0 0 4.2em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4.1em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4.2em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4.1em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4.2em;
    }

    .billedeSize {
      height: 13em;
      width: 29em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4em;
    }
  }

  @media screen and (max-width: 710px){
    .produktBoks {
      height: 57.1em;
    }

    .produktBoks1 {
      padding: 1em 0 0 3.8em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 3.8em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 3.8em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }
  }

  @media screen and (max-width: 700px){
    .produktBoks {
      height: 57.1em;
    }

    .produktBoks1 {
      padding: 1em 0 0 3.3em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 3.3em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 3.3em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }

    .billedeSize {
      height: 13em;
      width: 28em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4em;
    }
  }

  @media screen and (max-width: 690px){
    .heroOverskift {
      font-size: 4.2em;
      margin: -431px 0 3.5em 0;
    }

    .produktBoks {
      height: 55em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }

    .produktImages {
      height: 15.2em;
      width: 17.6em;
    }

    .produktBanner {
      width: 15.7em;
    }
  }

  @media screen and (max-width: 680px){
    .heroOverskift {
      font-size: 4.2em;
      margin: -431px 0 3.5em 0;
    }

    .produktBoks {
      height: 55em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }

    .billedeSize {
      height: 13em;
      width: 27em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4em;
    }
  }

  @media screen and (max-width: 660px){
    .produktBoks {
      height: 54em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }

    .produktImages {
      height: 14.2em;
      width: 16.6em;
    }

    .produktBanner {
      width: 14.7em;
    }

    .billedeSize {
      height: 13em;
      width: 26em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4em;
    }
  }

  @media screen and (max-width: 650px){
    .produktBoks {
      height: 53em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }
  }

  @media screen and (max-width: 640px){
    .produktBoks {
      height: 52.5em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }

    .billedeSize {
      height: 12.5em;
      width: 25em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4em;
    }
  }

  @media screen and (max-width: 630px){
    .heroOverskift {
      font-size: 3.5em;
      margin: -381px 0 3.5em 0;
    }

    .produktBoks {
      height: 51em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4.5em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }

    .produktImages {
      height: 13em;
      width: 15.4em;
    }

    .produktBanner {
      width: 13.5em;
    }
  }

  @media screen and (max-width: 620px){
    .produktBoks {
      height: 50em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 4em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 4em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }

    .billedeSize {
      height: 12.5em;
      width: 24em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4em;
    }
  }

  @media screen and (max-width: 610px){
    .produktBoks {
      height: 50em;
    }

    .produktBoks1 {
      padding: 1em 0 0 3.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 4em 0 0 3.5em;
    }

    .produktBoks4 {
      padding: 4em 0 0 4em;
    }

    .produktBoks5 {
      padding: 4em 0 0 3.5em;
    }

    .produktBoks6 {
      padding: 4em 0 0 4em;
    }
  }

  @media screen and (max-width: 600px){
    .produktBoks {
      height: 48.5em;
    }

    .produktBoks1 {
      padding: 1em 0 0 3.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 4em;
    }

    .produktBoks3 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktBoks4 {
      padding: 3.5em 0 0 4em;
    }

    .produktBoks5 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktBoks6 {
      padding: 3.5em 0 0 4em;
    }

    .billedeSize {
      height: 12em;
      width: 22.5em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4em;
    }
  }

  @media screen and (max-width: 590px){
    .produktBoks {
      height: 48.5em;
    }

    .produktBoks1 {
      padding: 1em 0 0 3.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 3.5em;
    }

    .produktBoks3 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktBoks4 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktBoks5 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktBoks6 {
      padding: 3.5em 0 0 3.5em;
    }
  }

  @media screen and (max-width: 580px){
    .produktBoks {
      height: 46em;
    }

    .produktBoks1 {
      padding: 1em 0 0 4em;
    }

    .produktBoks2{
      padding: 1em 0 0 3.5em;
    }

    .produktBoks3 {
      padding: 3.5em 0 0 4em;
    }

    .produktBoks4 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktBoks5 {
      padding: 3.5em 0 0 4em;
    }

    .produktBoks6 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktImages {
      height: 12em;
      width: 14.4em;
    }

    .produktBanner {
      width: 12.5em;
    }

    .billedeSize {
      height: 11.5em;
      width: 21em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4em;
    }
  }

  @media screen and (max-width: 570px){
    .produktBoks1 {
      padding: 1em 0 0 3.5em;
    }

    .produktBoks2{
      padding: 1em 0 0 3.5em;
    }

    .produktBoks3 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktBoks4 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktBoks5 {
      padding: 3.5em 0 0 3.5em;
    }

    .produktBoks6 {
      padding: 3.5em 0 0 3.5em;
    }
  }

  @media screen and (max-width: 560px){
    .heroOverskift {
      right: 16%;
    }

    .produktBoks1 {
      padding: 1em 0 0 3em;
    }

    .produktBoks2{
      padding: 1em 0 0 3.5em;
    }

    .produktBoks3 {
      padding: 3em 0 0 3em;
    }

    .produktBoks4 {
      padding: 3em 0 0 3.5em;
    }

    .produktBoks5 {
      padding: 3em 0 0 3em;
    }

    .produktBoks6 {
      padding: 3em 0 0 3.5em;
    }

    .billedeSize {
      height: 11em;
      width: 20em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 4em;
    }
  }

  @media screen and (max-width: 550px){
    .produktBoks {
      height: 86em;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 6.2em 0 6.2em;
    }

    .produktImages {
      height: 12em;
      width: 25em;
    }

    .produktBanner {
      width: 23em;
    }
  }

  @media screen and (max-width: 548px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 5.5em 0 5.5em;
    }

    .billedeSize {
      height: 11em;
      width: 20em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 3.5em;
    }
  }

  @media screen and (max-width: 525px){
    .heroOverskift {
      right: 15%;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 5em 0 5em;
    }

    .billedeSize {
      height: 11em;
      width: 19em;
    }

    .modal-center {
      text-align: left;
      padding: 0em 3em;
    }
  }

  @media screen and (max-width: 509px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 4.5em 0 4.5em;
    }
  }

  @media screen and (max-width: 500px){
    .heroOverskift {
      right: 14%;
    }

    .billedeSize {
      height: 11em;
      width: 24.5em;
      margin: 0 -38px 0 -39px;
    }

    .billedeBtn{
      z-index: 1;
      background-color: rgba(255, 255, 255, 50%);
      border: none;
    }
  }

  @media screen and (max-width: 480px){
    .billedeSize {
      height: 11em;
      width: 23em;
      margin: 0 -38px 0 -39px;
    }
  }

  @media screen and (max-width: 477px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 4em 0 4em;
    }
  }

  @media screen and (max-width: 461px){
    .heroOverskift {
      right: 13%;
    }

    .produktBoks {
      height: 80em;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 4em 0 4em;
    }

    .produktImages {
      height: 11em;
      width: 24em;
    }

    .produktBanner {
      width: 22em;
    }

    .billedeSize {
      height: 11em;
      width: 22em;
      margin: 0 -38px 0 -39px;
    }

    .billedeSize {
      height: 11em;
      width: 22.5em;
      margin: 0 -38px 0 -39px;
    }
  }

  @media screen and (max-width: 448px){
    .heroOverskift {
      right: 12.5%;
    }

    .produktBoks {
      height: 77.8em;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 4em 0 4em;
    }

    .produktImages {
      height: 10.5em;
      width: 23em;
    }

    .produktBanner {
      width: 21em;
    }

    .billedeSize {
      height: 11em;
      width: 21em;
      margin: 0 -38px 0 -39px;
    }
  }

  @media screen and (max-width: 435px){
    .heroOverskift {
      right: 11%;
    }

    .produktBoks {
      height: 77.8em;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 3.7em 0 3.7em;
    }

    .produktImages {
      height: 10.5em;
      width: 23em;
    }

    .produktBanner {
      width: 21em;
    }
  }

  /*************************************************/
  /*                    mobil                      */
  /*************************************************/
  @media screen and (max-width: 425px){
    .heroOverskift {
      right: 10%;
    }

    .produktBoks {
      height: 77.8em;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 3.4em 0 3.4em;
    }

    .produktImages {
      height: 10.5em;
      width: 23em;
    }

    .produktBanner {
      width: 21em;
    }

    .kontaktBoks {
      height: 28.5em;
    }

    .threeKontaktUnderBoks {
      flex-direction: column;
      align-items: center;
    }

    .threeKontaktTekstSpace{
      padding-bottom: 2em;
    }

    .billedeSize {
      height: 11em;
      width: 20em;
      margin: 0 -38px 0 -39px;
    }
  }

  @media screen and (max-width: 415px){
    .heroOverskift {
      font-size: 3em;
      right: 13.5%;
    }

    .produktBoks {
      height: 75.5em;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 3.6em 0 3.6em;
    }

    .produktImages {
      height: 10em;
      width: 22em;
    }

    .produktBanner {
      width: 20em;
    }
  }

  @media screen and (max-width: 409px){
    .produktBoks {
      height: 71.5em;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 3.7em 0 3.7em;
    }

    .produktImages {
      height: 10.5em;
      width: 21em;
    }

    .produktBanner {
      width: 19.1em;
    }

    .modal-center {
      padding: 0em 2.5em;
    }

    .billedeSize {
      height: 11em;
      width: 19em;
      margin: 0 -38px 0 -39px;
    }
  }

  @media screen and (max-width: 398px){
    .heroOverskift {
      right: 12%;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 3.5em 0 3.5em;
    }
  }

  @media screen and (max-width: 392px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 3em 0 3.5em;
    }
  }

  @media screen and (max-width: 384px){
    .heroOverskift {
      right: 11%;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 3em 0 3em;
    }

    .billedeSize {
      height: 10.5em;
      width: 18em;
      margin: 0 -38px 0 -39px;
    }
  }

  @media screen and (max-width: 376px){
    .heroOverskift {
      right: 10%;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 3em 0 3em;
    }

    .produktImages {
      height: 10.5em;
      width: 20em;
    }

    .produktBanner {
      width: 18.2em;
    }
  }

  @media screen and (max-width: 376px){
    .heroOverskift {
      font-size: 3em;
      right: 9%;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 3em 0 3em;
    }

    .produktImages {
      height: 10.5em;
      width: 20em;
    }

    .produktBanner {
      width: 18.2em;
    }
  }

  @media screen and (max-width: 363px){
    .produktBoks {
      height: 69em;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 3em 0 3em;
    }

    .produktImages {
      height: 10em;
      width: 19em;
    }

    .produktBanner {
      width: 17em;
    }

    .billedeSize {
      height: 10.5em;
      width: 17em;
      margin: 0 -38px 0 -39px;
    }
  }

  @media screen and (max-width: 349px){
    .heroOverskift {
      right: 8%;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 2.7em 0 2.7em;
    }
  }

  @media screen and (max-width: 340px){
    .heroOverskift {
      padding: 15px;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 2.5em 0 2.5em;
    }

    .modal-center {
      padding: 0em 2em;
    }

    .billedeSize {
      height: 10.5em;
      width: 16.5em;
      margin: 0 -38px 0 -39px;
    }
  }

  @media screen and (max-width: 333px){
    .heroOverskift {
      right: 7%;
      padding: 15px;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 2.3em 0 2.3em;
    }

    .modal-center {
      padding: 0em 2em;
    }

    .billedeSize {
      height: 10.5em;
      width: 16em;
      margin: 0 -38px 0 -39px;
    }
  }

  @media screen and (max-width: 327px){
    .heroOverskift {
      right: 6%;
      padding: 15px;
    }

    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 2em 0 2em;
    }

    .modal-center {
      padding: 0em 2.2em;
    }
  }
</style>