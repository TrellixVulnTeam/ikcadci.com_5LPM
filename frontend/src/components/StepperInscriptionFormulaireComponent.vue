<template>
    <div id="app" >
        <div class="p">
        <div class="p__Form">
            <div class="p__Form__head">
                <img  class="p__Form__head__img" src="../assets/maquette/maq-gle/masque_kemet.png" alt="😍" >
                <div class="p__Form__head__title">INSTITUT KEMETMAAT-CHEIKH ANTA DIOP 
                        ASSOCIATION KEMETMAAT 
                </div>
            </div>
            <div class="p__Form__header">
                        Face Inspection Générale  du Ministère de l’Environnement
                        kemetmaatabidjan@gmail.com
                        Whatsaap kemetmaat : 225 0758662960 
            </div>
            <div class="p__Form__articleun">
                Formulaire de pré-inscription.
            </div>
            <div class="p__Form__articledeux">
                La campagne d’inscription aux enseignements en ligne de la deuxième session  de l’année 2022 se déroulera du 1er avril au 30 juin. Les cours débutent le vendredi 1er juillet 2022 avec un réunion de présentation en live. Les places étant limitées, il est conseillé de nous retourner le bulletin le plus tôt possible. Pour des informations détaillées ; demandez la « note de présentation du seshw et seshw-nsw de kamitologie » et « le catalogue-descriptif des formations » à l’adresse mail: kemetmaatabidjan@gmail.com
            </div>

            <div class="p__Form__block">
                <div class="p__Form__block__titre">1 - Situation à l’ Etat Civil</div>
                <div class="p__Form__block__view">
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Nom :</div>
                        <div class="p__Form__block__view__content__input">{{ profile.username }}</div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Prénom :</div>
                        <div class="p__Form__block__view__content__input">{{ profile.lastname }}</div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Né(é) le :</div>
                        <div class="p__Form__block__view__content__input">{{ profile.dateBirthday}}</div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">A :</div>
                        <div class="p__Form__block__view__content__input">{{ profile.townBirthday}}</div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Sexe :</div>
                        <div class="p__Form__block__view__content__input"> {{ profile.sexe}} </div>
                    </div>
                </div>
                <div class="p__Form__block__titre">2 – Identité culturelle africaine</div>
                <div class="p__Form__block__view">
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Nom tradition:</div>
                        <div class="p__Form__block__view__content__input"> {{ profile.usernameTradition}} </div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Prénom tradition:</div>
                        <div class="p__Form__block__view__content__input">{{ profile.lastnameTradition}} </div>
                    </div>
                </div>
                <div class="p__Form__block__titre">3 –Adresse de résidence</div>
                <div class="p__Form__block__view">
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Adresse:</div>
                        <div class="p__Form__block__view__content__input">{{ profile.adresseResid}} </div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">ville:</div>
                        <div class="p__Form__block__view__content__input"> {{ profile.villeResid}}</div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Email:</div>
                        <div class="p__Form__block__view__content__input"> {{ profile.email }}</div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Tél-1:</div>
                        <div class="p__Form__block__view__content__input"> {{ profile.tel1}}</div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Tél-2:</div>
                        <div class="p__Form__block__view__content__input"> {{ profile.tel2}}</div>
                    </div>
                    <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Tél-3:</div>
                        <div class="p__Form__block__view__content__input"> {{ profile.tel3}}</div>
                    </div>
                </div>
                <div class="p__Form__block__titre">4 –Situation professionnelle </div>
                <div class="p__Form__block__view">
                 <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Profession:</div>
                        <div class="p__Form__block__view__content__input"> {{ profile.tel3}}</div>
                 </div> <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label">Activite:</div>
                        <div class="p__Form__block__view__content__input"> {{ profile.tel3}}</div>
                 </div>
                </div>
                <div class="p__Form__block__titre">5 –Choix de formation  </div>
                <div class="p__Form__block__view">
                 <div class="p__Form__block__view__content">
                        <div class="p__Form__block__view__content__label--bis">Inscription :</div>
                        <div class="p__Form__block__view__content__input--bis"> <p> {{ profile.seshsw}} </p><p> {{ profile.seshswNsw}} </p><p> {{ profile.seba}} </p></div>
                 </div>
                 </div>
             </div>
    </div>
    </div>
    </div>

</template>

<script>
    import axios from 'axios';
    export default {
        data: function() {
            return {
                isShowingFinale: false,
                isShowingSeshsw: false,
                isShowingSeshswNsw: false,
                isShowingSeba: false,

                visible: true,
                myStr: '',
                message: "Je suis un yankee",
                checkedFormations: [],
                profile: '',
                posts: {
                    username: '',
                    email: '',
                    biographie: '',
                    lastname: '',
                    usernameTradition: '',
                    lastnameTradition: '',
                    dateBirthday: '',
                    townBirthday: '',
                    sexe: '',
                    nationalite: '',
                    adresseResid: '',
                    villeResid: '',
                    paysResid: '',
                    tel1: '',
                    tel2: '',
                    tel3: '',
                    picked: '',
                    seshsw: '',
                    seshswNsh: '',
                    seba: '',
                    profession: '',
                    activite: ''
                }
            }
        },
        mounted() {
            this.$root.$on('bv::collapse::state', (collapseId, isJustShown) => {
                console.log('collapseId:', collapseId)
                console.log('isJustShown:', isJustShown)
            })
        },
        created() {
            let objMySession = localStorage.getItem("obj")
            let myStorageToken = JSON.parse(objMySession)
            let token = myStorageToken.myToken;
            axios
                .get('https://212.227.142.69:3000/api/users/me/', {
                    headers: {
                        'Authorization': token
                    }
                })
                .then(response => {
                    this.profile = response.data
                    this.testUser = this.profile.testUser
                    console.log(this.testUser) // this.$store.dispatch("beforeLogged")
                    if (this.testUser == 'testOk') {
                        this.$store.dispatch("beforeLogged")
                    }
                })
                .catch(error => console.log(error()))
        },
        methods: {
            myFunction: function() {
                this.posts.seba = JSON.stringify(this.checkedFormations)
            },
            postData(e) {
                let objMySession = localStorage.getItem("obj")
                let myStorageToken = JSON.parse(objMySession)
                let token = myStorageToken.myToken;

                this.axios.put('https://212.227.142.69:3000/api/users/me/', this.posts, {
                        headers: {
                            'Authorization': token
                        }
                    })
                    .then(response => {
                        this.profile.biographie = response.data.biographie
                        this.profile.lastname = response.data.lastname
                        this.profile.usernameTradition = response.data.usernameTradition
                        this.profile.lastnameTradition = response.data.lastnameTradition
                        this.profile.dateBirthday = response.data.dateBirthday
                        this.profile.townBirthday = response.data.townBirthday
                        this.profile.sexe = response.data.sexe
                        this.profile.nationalite = response.data.nationalite
                        this.profile.adresseResid = response.data.adresseResid
                        this.profile.villeResid = response.data.villeResid
                        this.profile.paysResid = response.data.paysResid
                        this.profile.tel1 = response.data.tel1
                        this.profile.tel2 = response.data.tel2
                        this.profile.tel3 = response.data.tel3
                        this.profile.picked = response.data.picked
                        this.profile.seshsw = response.data.seshsw
                        this.profile.seshswNsw = response.data.seshswNsw
                        this.profile.seba = response.data.seba
                        this.profile.profession = response.data.profession
                        this.profile.activite = response.data.activite
                    })
                    .catch(error => console.log(error()))

                e.preventDefault();
            },
            delProfil() {
                let objMySession = localStorage.getItem("obj")
                let myStorageToken = JSON.parse(objMySession)
                let token = myStorageToken.myToken;

                this.axios.post('https://212.227.142.69:3000/api/users/delProfil', null, {
                        headers: {
                            'Authorization': token
                        }
                    })
                    .then(response => {
                        this.profile = response.data
                    })
                    .catch(error => console.log(error()))

            }
        }
    }
</script>

<style lang="scss" scoped>

.collapsed > .when-open,
.not-collapsed > .when-closed {
  display: none;
}
 $bodybis-color: #818181;
    $border: #DDDDDD;
    $yellow: #FFB715;
    $white: #ffffff;
    $purple: #800080;
    $nav-bg: #F5F7FA;
    $white: #ffffff;
    $background-image-linear-blue: linear-gradient(to bottom, #016BA8, #569BCA, #9FC5E8);
    $orange: #FFB715;
    $blue:#016BA8;
    $muted:#707070;
    $border: #DDDDDD;
    $purple: linear-gradient(180deg, rgba(226,48,219,1) 7%, rgba(193,53,163,1) 41%, rgba(119,21,128,1) 94%);

bodybis{
  background: $purple;
  height: 100vh;
}

.seperator {
        margin-top: 25px;
        border-top: 1px solid $nav-bg;
        padding-top: 25px;
    }

.blueBar {
    background: $nav-bg;
    color: $muted;
    padding: 15px 20px;
    margin-top: 15px;
    box-shadow: 0px 3px 5px 0px rgba(0,0,0,0.75);
    border-radius: 50px;
    &:hover {
      opacity: 0.8;
        cursor: pointer;
        transition: all 1s;
        h5 {
            color: $white;
        }
    }

    h2 {
        text-transform: uppercase;
        margin: 0;
        color: $muted;
        font-size: 16px;
    }
    .fa-bars {
        transform: rotate(90deg);
    }
}

.red {
    .fa-chevron-down,
    .fa-plus {
        animation: rotate-in 0.5s forwards;
    }
    @keyframes rotate-in {
        from {
            transform: rotate(0deg);
        }
        to {
            transform: rotate(45deg);
        }
    }
}

.slide-enter-active {
    -moz-transition-duration: 0.5s;
    -webkit-transition-duration: 0.5s;
    -o-transition-duration: 0.5s;
    transition-duration: 0.5s;
    -moz-transition-timing-function: ease-in;
    -webkit-transition-timing-function: ease-in;
    -o-transition-timing-function: ease-in;
    transition-timing-function: ease-in;
}

.slide-leave-active {
    -moz-transition-duration: 0.5s;
    -webkit-transition-duration: 0.5s;
    -o-transition-duration: 0.5s;
    transition-duration: 0.5s;
    -moz-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
    -webkit-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
    -o-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
    transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
}

.slide-enter-to,
.slide-leave {
    max-height: 100px;
    overflow: hidden;
}

.slide-enter,
.slide-leave-to {
    overflow: hidden;
    max-height: 0;
}

.content{
  margin-top: 20px;
  background: none;
  color: $white;
}

.internalPadding {
    padding: 0 11px;
}

button{
  background: #nag-bg;
  color: $muted;
  border: none;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 2px;
  padding:5px 15px;
  border-radius: 5px;
  font-family: 'Montserrat', sans-serif;
  font-weight: bold;
  transition: all 1s;
  &:hover{
    background: $yellow;
    box-shadow: none;
    cursor: pointer;
  }&:focus{
    outline: none;
  }
}

.tab-container{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 50%;
}

 h1 {
        text-transform: uppercase;
        margin: 0;
        color: $nav-bg;
        font-size: 48px;
        letter-spacing: 25px;
        margin-bottom: 1rem;
        font-weight: light;
        
    }
</style>
