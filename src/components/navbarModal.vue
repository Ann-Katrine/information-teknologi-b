<template>
    <div>
        <div v-show="showNavbar" class="navbartest">
            <button @click="closeNavbar()"  class="btnModal navbarKryds">
                <ion-icon class="navbar-icon" name="close-outline" ></ion-icon>
            </button>
            <nav id="">
                <ul class="menuModal">
                    <li>
                        <a href="#hero" @click="closeNavbar()" class="navOverskift">IntelRobotics</a>
                    </li>
                    <li>
                        <a href="#produkt" @click="closeNavbar()" class="underOverskift">Produkt</a>
                    </li>
                    <li>
                        <a href="#kontakt" @click="closeNavbar()" class="underOverskift">Kontakt</a>
                    </li>
                    <li>
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
        </div>
    </div>
</template>

<script>
    import eventBus from '../eventBus'

    export default {
        name: "navbarModal",
        data(){
            return{
                showNavbar: false
            }
        },
        created(){
            eventBus.$on("showNavbar", (status) =>{
                this.showNavbar = status
                console.log("navbar modal er åben")
            })
        },
        methods:{
            closeNavbar(){
                this.showNavbar = false;
            }
        }
    }
</script>

<style>
    .navbartest{
      z-index: 1;
      display: flex;
      justify-content: center;
      align-content: center;
      position: fixed;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: #968787;
    }

    .menuModal{
        display: flex;
        flex-wrap: nowrap;
        flex-direction: column;
        align-items: center;
        width: 100%;
        height: 1em;
        padding: 0;
        padding-bottom: 5%;
    }

    .navbarKryds{
        right: 0px;
    }

    .navbar-icon{
        color: #000;
        width: 2em;
        height: 2em;
    }
</style>