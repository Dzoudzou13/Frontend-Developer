<!-- eslint-disable no-unused-vars -->
<template>
    <div id="bg-site">
        <main>
            <div class="container">
                <div class="pink">           
                    <h2>Rýchle výsledky pomocou UX auditu.</h2>
                    <img src="./../assets/images/pink.svg" alt="" class="pink1">
                </div>    
                <div class="images">
                    <img src="./../assets/images/premier-google-partner-RGB-search-mobile-vid-disp-shop.jpg" alt="google partner" class="google">
                    <img src="./../assets/images/memberofadma.png" alt="member of adma" class="adma">
                </div>
            </div>
            <div class="list container">
                <p>UX auditom vášho riešenia lepšie pochopíte, ako vaši zákazníci používajú váš produkt, <b> zvýšite ich spokojnosť <br> a hlavne vaše zisky.</b></p>
                <ul>
                    <li>Odhalíme nedostatky na vašej stránke</li>
                    <li>Zvýšime konverzný pomer vašich stránok</li>
                    <li>Zvýšime výkon marketingových kampaní</li>
                    <li>Znížime vaše náklady na vývoj</li>
                    <li>Zvýšime návštevnosť vašich stránok</li>
                </ul>
            </div>
            <div class="UX container">
                <p>Dosiahnite lepšie výsledky vašej webstránky alebo e-shopu <b>pomocou UX auditu.</b></p>
                <button @click="openModal">Mám záujem o UX audit</button>
                 <teleport to="#app">
                    <div id="modal"  class="bg-modal" v-if="isOpen">
                        <div class="modal-header">
                            <h1>Jednoducho nám napíšte a my sa vám ozveme.</h1>
                            <img src="./../assets/images/exit.png" alt="" @click="isOpen = false">
                        </div>
                        <form @submit.prevent="odoslatFormular">
                            <div class="name">
                                <p>Meno <span>*</span></p>
                                <input type="text" name="meno" id="meno" v-model="formData.meno">
                                <span v-for="error in v$.meno.$errors" :key="error.$uid" class="error"> 
                                    {{ error.$message }}
                                </span>
                            </div>
                            <div class="mail-tel">
                                <div class="modal-mail">
                                    <p>E-mail: <span>*</span> </p>
                                    <input type="email" name="email" id="email"  v-model="formData.email">
                                     <span v-for="error in v$.email.$errors" :key="error.$uid" class="error"> 
                                    {{ error.$message }}
                                </span>
                                </div>
                                <div class="modal-tel">
                                    <p>Tel.číslo:</p>
                                    <input type="text" name="" id="">
                                </div>
                            </div>
                            <div class="web">
                                <p>Webstránka:</p>
                                <input type="text" name="" id="">
                            </div>
                            <div class="note">
                                <p>Poznámka:</p>
                                <input type="text" name="" id="" placeholder="Je niečo čo by ste sa nás chceli spýtat?">
                            </div>
                             <div class="modal-btn">
                                <button type="submit">Kontaktujte ma</button>
                            </div>
                        </form>
                    </div>
                </teleport>
            </div>

            <div class="boxes container">
                <div class="dotte">
                    <div class="box1">
                        <p>Pravidelné UX audity a postupné vylepšovanie nášho internetového obchodu je už niekoľko rokov súčasťou našej dlhodobej stratégie v predaji. 
                            UX tím v Riešeniach odvádza skvelú prácu, ktorú sprevádzajú viditeľné výsledky a spokojnosť našich zákazníkov. 
                            Okrem ich prístupu k nášmu biznisu … <span class="red">čítať viac</span></p>
                        <img src="./../assets/images/dittos.svg" alt="">
                    </div>
                </div>
                <div class="dotte">
                    <div class="box2">
                        <p>S UX tímom Riešení úzko spolupracujeme už dlhé roky a sú dôležitým partnerom nášho biznisu. 
                            Vďaka ich know-how pre nás od samého začatku správne nastavili zdravý pomer prvotriedneho dizajnu a funkčnosti webu,
                            ktorý následne vylepšovali pomocou relevantných analýz a dát. 
                            Aj ich zásluhou … <span class="red">čítať viac</span></p>
                        <img src="./../assets/images/dittos.svg" alt="">
                    </div>
                </div>
            </div>
            <div class="users container">
                <div class="loga-firiem svet">
                    <img src="./../assets/images/svetnapojov.svg" alt="logo firmy SvetNápojov.sk">
                    <p> <b>Jozef Korman </b> <br> Konateľ  <span>SvetNápojov.sk</span> </p>
                </div>
                <div class="loga-firiem alain">
                    <img src="./../assets/images/alaindelon.png" alt="logo firmy  AlainDelon">
                    <p> <b>Richard Wohlstein </b> <br> Retail manager <span>AlainDelon.sk</span> </p>
                </div>            
            </div>
            <div class="results container">
                <div class="pink">
                     <h2>Rýchla <span>a jednoduchá cesta k výsledkom.</span></h2>
                     <img src="./../assets/images/pink.svg" alt="" class="pink2">                
                    </div>
            </div>
            <div class="numbers">
                <div class="one">
                    <img src="./../assets/images/1.svg" alt="čislo 1" class="img1">
                    <div class="text-box nmb-1">
                        <h3>Ciele auditu</h3>
                        <p>Určíme si spoločné ciele, nastavíme očakávania a definujeme <b>cieľovú skupinu a jej potreby.</b></p>
                    </div>
                    <img class="arrowR" src="./../assets/images/arrowR.svg" alt="prava šipka">
                </div>
                <div class="two">
                    <img src="./../assets/images/arrowL.svg" alt="ľava šipka" class="arrowL">
                    <img src="./../assets/images/2.svg" alt="čislo 2">
                    <div class="text-box nmb-2">
                        <h3>Zbieranie dát</h3>
                        <p>Zvolíme vhodné metodiky a nástroje na <b>sledovanie správania používateľov a zbieranie dát.</b></p>
                    </div>
                </div>
                <div class="one">
                    <img src="./../assets/images/3.svg" alt="čislo 3">
                    <div class="text-box nmb-3">
                        <h3>Vyhodnotenie</h3>
                        <p><b>Vyhodnotíme nazbierané dáta,</b> zosumarizujeme všetky naše zistenia a <b>navrhneme riešenia.</b></p>
                    </div>
                    <img class="smallarrowR" src="./../assets/images/smallerarrowR.svg" alt="prava šipka">
                </div>
                <div class="four">
                    <img src="./../assets/images/4.svg" alt="čislo 4">
                    <div class="text-box nmb-2">
                        <h3>Výsledky auditu</h3>
                        <p><b>Osobná prezentácia výsledkov a navrhnutých riešení </b> s podrobnou dokumentáciou.</p>
                    </div>
                </div>
            </div>
            <div class="important container">
                <div class="pink">
                    <h2>Zameriame sa na to najdôležitejšie.</h2>
                    <img src="./../assets/images/pink3.png" class="pink3" alt="">
                </div>
            </div>
            <div class="ul container">
                <p>Dosiahnite lepšie výsledky vašej webstránky alebo e-shopu <b>pomocou UX auditu.</b></p>
                <ul>
                    <li>Informačnú architektúru a štruktúru kategórií</li>
                    <li>Správanie návštevníkov na kľúčových stránkach</li>
                    <li>Rýchlosť a dostupnosť stránok, SEO nastavenia</li>
                    <li>Váš biznis a vašich zákazníkov</li>
                    <li>Ciele, ktoré chcete dosiahnuť</li>
                    <li>Webovú analytiku</li>
                </ul>
            </div>
            <div class="btn container">
                <button @click="openModal">Mám záujem o UX audit</button>
            </div>       
        </main>
    </div>
</template>

<script>
import { required, email, minLength} from '@vuelidate/validators';
import { reactive, computed } from 'vue';
import { useVuelidate } from '@vuelidate/core';

export default {
  data() {
    return {
      isOpen: false,
      formData: reactive({
        meno: '',
        email: ''
      }),
      v$: null
    };
  },
  methods: {
    openModal() {
      this.isOpen = true;
      console.log("Modální okno otvorené");
      this.$nextTick(() => {
        const modal = document.getElementById('modal');
        if (modal) {
          console.log("Modální okno nájdené, posúvanie...");
          modal.scrollIntoView({ behavior: 'smooth'});
        } else {
          console.log("Modální okno nenájdené");
        }
      });
    },
    async odoslatFormular() {
      if (this.v$) {
        const result = await this.v$.$validate();
        if (result) {
          alert('Formulár bol úspešne odoslaný!');
        } else { 
          alert('Prosím, vyplňte povinné polia.');
        }
      }
    }
  },
  watch: {
    isOpen(value) {
      if (value) {
        document.getElementById('app').classList.add('modal-open');
      } else {
        document.getElementById('app').classList.remove('modal-open');
      }
    }
  },
  computed: {
    rules() {
      return computed(() => ({
        meno: { required, minLength: minLength(5) },
        email: { required, email }
      }));
    }
  },
  validations() {
    return {
      formData: this.rules
    };
  },
  mounted() {
    this.v$ = useVuelidate(this.rules, this.formData);
  }
};
</script>

<style lang="scss" scoped>
.container{
    display: flex;
    justify-content: center;
}

.container h2 {
    width: 8.94em;
    height: 4.19em;
    font-size: 3em;
    font-weight: 700;
    padding-top: 1.56em;
    padding-right: 2.3em;
    margin: 0;
}

.images {
    padding-top: 4.8em;
    display: flex;
    padding-left: 1em;
}
.google {
    height: 5em;
    padding-top: 1em;
}

.adma {
    padding-left: 2em;
    height: 7em;
}

.list p {
    width: 19em;
    height: 8em;
    font-size: 1.5em;
    font-weight: 400;
    margin-right: 3.5em;
    line-height: 2em;
    margin-top: 2.5em;
    position: relative;
    left: -1em;
}

ul {
    display: flex;
    width: 24.63em;
    height: 15.625em;
    flex-direction: column;
    justify-content: center;
    list-style: none; 
    padding-left: 0; 
}
li {
    background-image: url('./../assets/images/greencircle.svg'); 
    background-repeat: no-repeat; 
    padding-left: 1.875em; 
    padding-bottom: 2.5em;
    font-size: 1.125em;
    font-weight: 600;
}

.UX {
    align-items: center;
    margin-top: 6.7em;
}

.UX p{
    width: 23em;
    height: 4.375em;
    font-size: 1.375em;
    font-weight: 400;
    line-height: 2.5em;
    position: relative;
    left: -1em;
    margin-right: 2em;
    margin-top: 0;
}

.UX Button {
    width: 19.7em;
    height: 3.5em;
    border-radius: 0.5em;
    background: #EE325C;
    border: none;
    color: #FFF;
    text-align: center;
    font-size: 1.25em;
    font-weight: 900;
    margin-top: 1em;
    transition-duration: 2s;
    cursor: pointer;
}

.UX Button:focus,
.UX Button:hover {
    background: #EE325C;
    animation: pulse-169a02ec 1s;
    box-shadow: inset 0 0 0 2em transparent, 0 0 0 1em transparent;
    color: #fff;
    transform: scale(1.1);
}

.boxes {
    margin-top: 8em;
}
.box1 {
    margin-right: 6em;
}
.box1 img,
.box2 img {
    position: relative;
    bottom: 19.4em;
    left: 2em;
}
.box1 p,
.box2 p {
    width: 22.56em;
    font-size: 1em;
    font-weight: 400;
    line-height: 2em;
    margin: 0;
    border: 1px solid #D6D8DD;
    padding: 2em 1.56em 1.75em 2.12em;
}
.red {
    color: #EE325C;
    font-weight: 700;
}
.users {
    margin-top: 2.06em;
}

.loga-firiem {
    display: flex;
}
.loga-firiem img {
    width: 4em;
    height: 4em;
}
.loga-firiem p {
    padding-left: 1.19em;
    width: 14.125em;
    height: 3.06em;
    line-height: 1.375em;
    font-size: 1em;
}
.loga-firiem b {
    font-weight: 900;
}
.loga-firiem span {
    color: #EE325C;
    font-weight: 700;
}

.svet {
    margin-right: 6em;
    position: relative;
    left: -7em;
}
.results h2{
    width: 10.94em;
    padding-right: 0em;
    text-align: center;
    padding-top: 3.5em;
}
.resualts h2 br {
    display: none;
}

.one{
    display: flex;
    justify-content: center;
    position: relative;
    left: -11.8em;
}
.text-box {
    display: flex;
    width: 22.75em;
    height: 6.25em;
    flex-direction: column;
    justify-content: center;
    padding-left: 3em;
    padding-top: 1.3em;
}
.text-box h3 {
    font-size: 1.5em;
    font-weight: 900;
    line-height: normal;
    margin: 0;
}
.text-box p {
    font-weight: 400;
    line-height: 1.75em;
    margin: 0;
    width: 22em;
}
.arrowR {
    position: relative;
    top: 5em;
    left: 3em;
    height: 4.375em;
    width: 4.64em;
}
.two {
    display: flex;
    justify-content: center;
    position: relative;
    left: 12em;
    padding-top: 3em;
}
.nmb-2 p {
    width: 24em;
    }
.arrowL{
    position: relative;
    top: 3em;
    right: 3em;
}
.nmb-3 p {
    width: 24em;
}
.smallarrowR {
    position: relative;
    top: 4.5em;
    left: 3em;
    width: 4.25em;
    height: 4.31em;
}
.four {
    display: flex;
    justify-content: center;
    position: relative;
    left: 14em;
    padding-top: 2em;
}

.important{
    padding-top: 5em;
}
.important h2 {
    width: 9.6em;
    padding-right: 10em;
}
.ul p {
    width: 16.69em;
    height: 4.25em;
    font-size: 1.625em;
    font-weight: 400;
    line-height: 1.5em;
    margin: 0;
    margin-right: 2.5em;
    margin-top: -0.1em;
}
.ul ul {
    width: 27.63em;
}

.btn{
    position: relative;
    top: -5em;
    left: -17em;
}
.pink1{
    position: relative;
    top: -9.8em;
    right: -10em;
    width: 12.88em;
}
.pink2{
    position: relative;
    top: -5.5em;
    left: 13.9em;
    width: 16.16em;
}
.pink3{
    position: relative;
    top: -5.5em;
}
@media screen and (max-width: 1085px ) {
    .container {
        flex-direction: column-reverse;
        align-items: center;
    }
    .container h2 {
        padding-right: 0em;
    }
    .list {
        flex-direction: column;
        align-items: center;
    }
    .list ul {
        padding-top: 6em;
    }
    .list p {
        width: 18em;
        margin: 0;
        left: 0;
    }
    .list p br {
        display: none;
    }
    .UX{
        flex-direction: column;
        margin-top: 3.7em;
    }
    .UX p {
        width: 18em;
        height: 7.38em;
        left: 0;
        margin-right: 1.5em;
    }
    .UX button {
        margin-right: 1.5em;
    }
    .boxes{
        flex-direction: column;
    }
    .box1{
        margin-right: 0em;
        margin-bottom: 10em;
    }
    .svet {
        left: -0.5em;
        top: -34em;
    }
    .alain{
        position: relative;
        left: -3.5em;
    }
    .results h2 {
        padding-top: 0em;
    }
    .arrowR{
        display: none;
    }
    .arrowL{
        display: none;
    }
    .smallarrowR{
        display: none;
    }
    .two {
        left: 10em;
    }
    .four {
        left:9em
    }
    .important {
        padding-top: 0em;
    }
    .ul p {
        margin-top: 2em;
        margin-bottom: 5em;
        margin-right: 0em;
    }
    .btn{
        left: -1.5em;
    }
}

@media screen and (max-width: 900px ) {
    .numbers{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .one {
        left: 0em;
    }
    .numbers img {
        padding-top: 2em;
    }
    .two {
        left: 0em;
        padding-top: 0em;
    }
    .four {
        left: 0em;
        padding-top: 0em;
    }
}
@media screen and (max-width: 560px ) {
    .images {
        padding-left: 2em;
    }
    .container h2 {
        font-size: 2em;
        width: 9.94em;
    }
    .pink1{
        top: -6.5em;
        right: -6.4em;
        width: 9em;
    }
    .list p {
        font-size: 1.25em;
        margin-left: 2em;  
        margin-bottom: 2em;
    }
    ul {
        padding-top: 9em;
        width: 17.63em;
        padding-right: 2em;  
    }
    .UX {
        margin-top: 4.7em;
    }
    .UX p {
        width: 12.5em;
        margin-left: -0.5em;
    }
    .UX button {
        margin-right: 0em;
        width: 16em;
        margin-top: 4em;   
    }
    .box1 p {
        width: 17.25em;
        padding: 2em 1.19em 1em 1.75em;
    }
    .box1 img {
        bottom: 22.6em;
        left: 1em;
    }
    .svet{
        left: 2.5em;
        top: -43em;
    }
    .box2 p {
        width: 16.44em;
        padding: 1.87em 1.94em 1.5em 1.81em;
    }
    .box2 img {
        bottom: 25em;
        left: 1em;
    }
    .alain {
        top: -2em;
        left: -0.5em;
    }
    .results {
        margin-bottom: 3em;
    }
    .results h2 {
        display: flex;
        flex-direction: column;
        text-align: left;    
    }
    .pink2 {
        top: -1.5em;
        left: 1.5em;
        width: 11.5em;
    }
    .text-box p {
        width: 13.5em;
    }
    .one{
        left: 4em;
    }
    .two {
        padding-top: 4em;  
        padding-bottom: 2em;
        left: 4em;
    }
    .nmb-2 p {
        width: 14em;    
    }
    .nmb-3 p {
        width: 14.5em;
    }
    .nmb-3{
        padding-top: 4em;
    }
    .four {
        padding-top: 4em;
        left: 4em;
    }
    .important{
        padding-top: 2em;
    }
    .important h2{
        width: 8.94em;    
    }
    .pink3 {
        top: -4em;
        width: 17em;
    }
    .ul ul {
        width: 15.63em;
    }
    .ul p {
        margin-top: 6em;
        width: 12.69em;
        font-size: 1.38em;
    }
    .btn {
        margin-top: 2em;
        left: -0.5em; 
    }
    .btn button {
        width: 13.7em;  
    }
}

@media screen and (max-width: 425px) {
    .numbers {
        align-items: stretch;
    }
    .numbers img {
        padding-left: 2em;
    }
    .text-box  {
        padding-left: 1em;
    }
    .nmb-1{
        padding-left: 2em    
    }
}

@media screen and (max-width: 360px) {
    .images {
        font-size: 0.7em;
    }
    .container h2 {
        margin-left: 0.5em;
    }
    .pink1 {
        left: -7.4em;
    }
    .list p {
        margin-left: 3em;    
    }
    .list ul {
        margin-left: 2em;
    }
    .UX p {
        margin-left: 0.5em;
    }
    .UX button {
        width: 14em;    
    }
    .boxes {
        font-size: 0.9em;
    }
    .box1 img {
    bottom: 21.4em;
    left: 2em;
    }    
    .box2 img {
    bottom: 24.5em;
    left: 2em;
    }
    .users {
        font-size: 0.9em;    
    }
    .svet {
        left: 2.9em;
    }
    .alain {
        left: -0em;
        top: -3em;
    }
    .results h2 {
        margin-left: 1em; 
    }
    .ul {
        margin-left: 1em;    
    } 
    .pink2 {
        left: 3.2em;
    }
    .pink3 {
        left: 1em;
    }
    .ul ul {
        margin-left: 1em;
    }
    .ul p {
        font-size: 1.35em;
        margin-left: -1em;
    }
    .btn {
        left: 0em;
    }
    .btn button {
        width: 14em;    
    }
}
</style>