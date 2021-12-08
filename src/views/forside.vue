<template>
    <div>
        <div id="forside">
            <nav id="navbar">
                <ul class="menu">
                    <li>
                        <a href="#hero" class="navOverskift">IntelRoboties</a>
                    </li>
                    <li>
                        <a href="#produkt" @click="test()" class="underOverskift">Produkt</a>
                    </li>
                    <li>
                        <a href="#kontakt" class="underOverskift">Kontakt</a>
                    </li>
                    <li>
                        <div>
                          
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
                        </div>

                        <select>
                          <option>Japansk                           
                          </option>
                          <option>Engelsk</option>
                          <option>Canadisk</option>
                          <option>Danmark</option>
                        </select>
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
                <h1 class="heroOverskift">IntelRoboties</h1>
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
                </div>
                <div class="threeProduktUnderBoks">
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
                    <div>
                        <p class="kontaktUnderBoksOverskift">Danmark</p>
                        <p class="kontaktUnderBoksUnderOverskrift">Vejnavn</p>
                        <p class="kontaktUnderBoksUnderOverskrift">by og postnr</p>
                        <p class="kontaktUnderBoksUnderOverskrift">mail</p>
                        <p class="kontaktUnderBoksUnderOverskrift">telefon nr.</p>
                    </div>
                    <div>
                        <p class="kontaktUnderBoksOverskift">Japan</p>
                        <p class="kontaktUnderBoksUnderOverskrift">Vejnavn</p>
                        <p class="kontaktUnderBoksUnderOverskrift">by og postnr</p>
                        <p class="kontaktUnderBoksUnderOverskrift">mail</p>
                        <p class="kontaktUnderBoksUnderOverskrift">telefon nr.</p>
                    </div>
                    <div>
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
  </div>
</template>

<script>
  import eventBus from '../eventBus'
  import axios from 'axios'
  import ShowProduct from '../components/showProduct.vue';

  export default {
    name: 'forside',
    data(){
      return{
        allProduct: [],
        allKontaktInfo: [],
        oneProduct: []
      }
    },
    components:{
      ShowProduct
    },
    created(){
      this.stickNavbar();
      /*this.getAllProducs();
      this.getAllKontaktInfo();
      this.getOneProduct();*/
    },
    mounted(){
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

  /*************************************************/
  /*                    hero                       */
  /*************************************************/

  .heroOverskift{
    position: absolute;
    font-size: 6em;
    background-color: #CCDAE3;
    margin: -4.5em 0 3.5em 8em;
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
    width: 59em;
    height: 36em;
  }

  /*************************************************/
  /*                  produkter                    */
  /*************************************************/

  .produktBoks{
    height: 38em;
  }

    .threeProduktUnderBoks{
        display: flex;
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
  /* @media screen and (max-width: ){
    
  } */
</style>