<template>
    <div>
        <div v-show="showModal" class="outer-modal">
            <div id="indreModal" class="indre-modal">
                <div class="btn-rigth">
                    <button @click="closeModal()" class="btnModal">
                        <ion-icon class="close-ikon" name="close-outline" ></ion-icon>
                    </button>
                </div>
                <div class="modal-center">
                    <slot>

                    </slot>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import eventBus from '../eventBus'

    export default {
        name: "showProject",
        data(){
            return{
                showModal: false,
                modalHeigth: 0,
                tekstOpen: false
            }
        },
        created(){
            eventBus.$on("showModal", (status) =>{
                this.showModal = status
                console.log("modalen er åben")
            })
        },
        methods:{
            closeModal(){
                this.showModal = false
            }
        }
    }
</script>

<style>
    /*************************************************/
    /*                   modal                       */
    /*************************************************/
    .outer-modal{
        z-index: 1;
        display: flex;
        justify-content: center;
        align-items: center;
        position: fixed;
        top: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 50%);
    }

    .indre-modal{
       background-color: #CCDAE3;
       width: 800px;
       max-width: 100%;
       min-height: 430px;
       max-height: 600px;
       border-radius: 25px;
       overflow: auto;
    }

    .modal-center{
        text-align: left;
        padding: 0em 6em;
    }

    .btn-rigth{
        text-align: right;
        position: sticky;
        top: 1px;
    }

    .btnModal{
        background-color: transparent;
        border: none;
        padding: 1em 1em 0em 0em;
        position: fixed;
        margin: 0 0 0 -3em;
    }

    .close-ikon{
        color: #607272;
        width: 2em;
        height: 2em;
    }

    /*************************************************/
    /*                 ting til slot                 */
    /*************************************************/

    /* billede boks */
    .billdeBoks{
        display: flex;
        padding-top: 3em;
    }

    .billedeSize{
        height: 13em;
    }

    /* cirker til billede */
    .modal-circle-box{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-flow: row nowrap;
        padding-top: 4px;
    }

    .modal-circles{
        margin: 0.1em;
        background-color: #fff;
        width: 10px;
        height: 10px;
        border-radius: 100%;
    }

    /* tekst */
    .modalOverskrift{
        font-size: 2em;
    }

    .modalUnderOverskrift{
        font-size: 1.2em;
    }

    .modaltekstMellemrum{
        padding-bottom: 0.2em;
    }
    
    .modalBeardText{
        padding-bottom: 3em;
    }
</style>