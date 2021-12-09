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
                        <!-- <div>
                          
                          <p></p>
                          <img src="https://images.fyndiq.se/images/f_auto/t_600x600/prod/2dd30c4404074a9e/1d003859a205/flag-danmark" class="">
                          <button></button>
                          <div>
                            <div>
                              <p>Japansk</p>
                            </div>
                            <div>
                              <p>Engelsk</p>
                            </div>
                            <div>
                              <p>Canadisk</p>
                            </div>
                            <div>
                              <p>Danmark</p>
                            </div>
                          </div>
                        </div> -->

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
                    <div class="heroUnderBoks2">
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
        showNotNavbarThings: true
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

        // Bruger eventer scroll for at se hvornår man rækker sig op eller ned på siden
        if(window.scrollY > 0){
          navbar.classList.add("sticky");
          forside.classList.add("strickyForsideHeigth");
        }
        else{
          navbar.classList.remove("sticky");
          forside.classList.remove("strickyForsideHeigth");
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
        console.log(this.windowswidth);

        if(this.windowswidth < 601){
          console.log("under 600");
          this.showNavbarButton = true;
          this.showNotNavbarThings = false;
        }
        else{
          console.log("over 600");
          this.showNavbarButton = false;
          this.showNotNavbarThings = true;
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
    height: 35.9em;
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
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 766px;
    } */

    .produktBoks3 {
      padding: 1em 13.3em 0 0;
    }

    .produktBoks6 {
      padding: 6em 13.3em 0 0;
    }
  }

  @media screen and (max-width: 1350px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 756px;
    } */

    .produktBoks3 {
      padding: 1em 12.5em 0 0;
    }

    .produktBoks6 {
      padding: 6em 12.5em 0 0;
    }
  }

  @media screen and (max-width: 1340px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 746px;
    } */

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
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 736px;
    } */

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

  @media screen and (max-width: 1320px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 726px;
    } */

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

  @media screen and (max-width: 1310px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 716px;
    } */

    .produktBoks2{
      padding: 1em 5.4em 0 5.4em;
    }

    .produktBoks5 {
      padding: 5em 5.4em 0 5.4em;
    }
  }

  @media screen and (max-width: 1300px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 706px;
    } */

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

  @media screen and (max-width: 1290px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 696px;
    } */

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

  @media screen and (max-width: 1280px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 686px;
    } */

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

  @media screen and (max-width: 1270px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 676px;
    } */

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

  @media screen and (max-width: 1260px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 666px;
    } */

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

  @media screen and (max-width: 1250px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 656px;
    } */

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
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 646px;
    } */

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

  /* @media screen and (max-width: 1230px){
    .heroOverskift {
        margin: -4.5em 0 3.5em 636px;
    }
  } */

  @media screen and (max-width: 1220px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 626px;
    } */

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

  @media screen and (max-width: 1210px){
    /* .heroOverskift {
        margin: -4.5em 0 3.5em 616px;
    } */

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

  @media screen and (max-width: 1200px){
    .heroOverskift {
      font-size: 5.7em;
      /* margin: -431px 0 3.5em 632px; */
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

  @media screen and (max-width: 1190px){
    .heroOverskift {
      font-size: 5.7em;
      /* margin: -431px 0 3.5em 622px; */
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

  @media screen and (max-width: 1180px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 612px;
    } */

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

  @media screen and (max-width: 1170px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 602px;
    } */

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

  @media screen and (max-width: 1160px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 592px;
    } */

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

  @media screen and (max-width: 1150px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 582px;
    } */

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
  
  @media screen and (max-width: 1140px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 572px;
    } */

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

  /* @media screen and (max-width: 1130px){
    .heroOverskift {
      margin: -431px 0 3.5em 562px;
    }
  } */

  @media screen and (max-width: 1120px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 552px;
    } */

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

  @media screen and (max-width: 1110px){
    .heroOverskift {
      font-size: 5.5em;
      /* margin: -431px 0 3.5em 559px; */
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

  @media screen and (max-width: 1100px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 549px;
    } */

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

  @media screen and (max-width: 1090px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 539px;
    } */
  }

  @media screen and (max-width: 1080px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 529px;
    } */
  }

  @media screen and (max-width: 1070px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 519px;
    } */

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
    /* .heroOverskift {
      margin: -431px 0 3.5em 509px;
    } */

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

  @media screen and (max-width: 1050px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 499px;
    } */
  }

  @media screen and (max-width: 1040px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 489px;
    } */

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

  @media screen and (max-width: 1030px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 479px;
    } */
  }

  @media screen and (max-width: 1020px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 469px;
    } */

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

  @media screen and (max-width: 1010px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 459px;
    } */
  }

  @media screen and (max-width: 1000px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 449px;
    } */
  }

  @media screen and (max-width: 990px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 439px;
    } */
  }

  @media screen and (max-width: 980px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 429px;
    } */

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

  @media screen and (max-width: 970px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 419px;
    } */

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

  /* @media screen and (max-width: 960px){
    .heroOverskift {
      margin: -431px 0 3.5em 409px;
    }
  } */

  @media screen and (max-width: 950px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 399px;
    } */

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

  @media screen and (max-width: 940px){
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

  @media screen and (max-width: 930px){
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

  /* @media screen and (max-width: 920px){
    .heroOverskift {
      font-size: 4.8em;
      margin: -431px 0 3.5em 429px;
    }
  } */

  @media screen and (max-width: 910px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 419px;
    } */

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
    /* .heroOverskift {
      margin: -431px 0 3.5em 409px;
    } */

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

  /* @media screen and (max-width: 890px){
    .heroOverskift {
      margin: -431px 0 3.5em 399px;
    }
  } */

  /* @media screen and (max-width: 880px){
    .heroOverskift {
      margin: -431px 0 3.5em 389px;
    }
  } */

  @media screen and (max-width: 870px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 379px;
    } */

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
    /* .heroOverskift {
      margin: -431px 0 3.5em 369px;
    } */

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

  /* @media screen and (max-width: 850px){
    .heroOverskift {
      margin: -431px 0 3.5em 359px;
    }
  } */

  /* @media screen and (max-width: 840px){
    .heroOverskift {
      margin: -431px 0 3.5em 349px;
    }
  } */

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

  /* @media screen and (max-width: 820px){
    .heroOverskift {
      margin: -431px 0 3.5em 355px;
    }
  } */

  @media screen and (max-width: 810px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 345px;
    } */

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
    /* .heroOverskift {
      margin: -431px 0 3.5em 335px;
    } */

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
  }

  @media screen and (max-width: 790px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 325px;
    } */

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
    /* .heroOverskift {
      margin: -431px 0 3.5em 315px;
    } */

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

  @media screen and (max-width: 770px){
    /* .heroOverskift {
      margin: -401px 0 3.5em 305px;
    } */

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
    /* .heroOverskift {
      margin: -401px 0 3.5em 303px;
    } */

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

  /* @media screen and (max-width: 760px){
    .heroOverskift {
      margin: -401px 0 3.5em 295px;
    }
  } */

  @media screen and (max-width: 750px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 285px;
    } */

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
    /* .heroOverskift {
      margin: -431px 0 3.5em 275px;
    } */

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
  }

  @media screen and (max-width: 730px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 265px;
    } */

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
    /* .heroOverskift {
      margin: -431px 0 3.5em 255px;
    } */

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
  }

  @media screen and (max-width: 710px){
    /* .heroOverskift {
      margin: -431px 0 3.5em 245px;
    } */

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
    /* .heroOverskift {
      margin: -431px 0 3.5em 235px;
    } */

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
    .menu{
      display: flex;
      justify-content: space-between;
      align-items: baseline;
    }

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

  @media screen and (max-width: 540px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 5.5em 0 5.5em;
    }
  }

  @media screen and (max-width: 520px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 5em 0 5em;
    }
  }

  @media screen and (max-width: 500px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 4.5em 0 4.5em;
    }
  }

  @media screen and (max-width: 477px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 3em 4em 0 4em;
    }
  }

  @media screen and (max-width: 461px){
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
  }

  @media screen and (max-width: 448px){
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
  }

  @media screen and (max-width: 435px){
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
    }

    .threeKontaktTekstSpace{
      padding-bottom: 2em;
    }
  }

  @media screen and (max-width: 415px){
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
  }

  @media screen and (max-width: 398px){
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
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 3em 0 3em;
    }
  }

  @media screen and (max-width: 376px){
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
  }

  @media screen and (max-width: 349px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 2.7em 0 2.7em;
    }
  }

  @media screen and (max-width: 340px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 2.5em 0 2.5em;
    }
  }

  @media screen and (max-width: 333px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 2.3em 0 2.3em;
    }
  }

  @media screen and (max-width: 327px){
    .produktBoks1, .produktBoks2, .produktBoks3, .produktBoks4, .produktBoks5, .produktBoks6 {
      padding: 2em 2em 0 2em;
    }
  }
</style>