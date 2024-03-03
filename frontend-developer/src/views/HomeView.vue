<template>
    <div>
        <header>
            <section class="logo-btn"> 
                <img src="./../assets/logoR.png" alt="logo" class="logo">
                <button>Mám záujem o UX audit</button>
            </section>
            <section class="title">
                <h1>Zvýšte svoje zisky optimalizáciou vášho eshopu.</h1>    
            </section>
        </header>
        <main>
            <article>
                <h2>Rýchle výsledky pomocou UX auditu.</h2>
                <section class="images">
                    <img src="./../assets/premier-google-partner-RGB-search-mobile-vid-disp-shop.jpg" alt="google partner" class="google">
                    <img src="./../assets/memberofadma.png" alt="member of adma" class="adma">
                </section>
            </article>
            <article class="list">
                <p>UX auditom vášho riešenia lepšie pochopíte, ako vaši zákazníci používajú váš produkt, <b> zvýšite ich spokojnosť <br> a hlavne vaše zisky.</b></p>
                <ul>
                    <li>Odhalíme nedostatky na vašej stránke</li>
                    <li>Zvýšime konverzný pomer vašich stránok</li>
                    <li>Zvýšime výkon marketingových kampaní</li>
                    <li>Znížime vaše náklady na vývoj</li>
                    <li>Zvýšime návštevnosť vašich stránok</li>
                </ul>
            </article>
            <article class="UX">
                <p>Dosiahnite lepšie výsledky vašej webstránky alebo e-shopu <b>pomocou UX auditu.</b></p>
                <button>Mám záujem o UX audit</button>
            </article>

            <article class="boxes">
                <section class="box1">
                    <p>Pravidelné UX audity a postupné vylepšovanie nášho internetového obchodu je už niekoľko rokov súčasťou našej dlhodobej stratégie v predaji. 
                        UX tím v Riešeniach odvádza skvelú prácu, ktorú sprevádzajú viditeľné výsledky a spokojnosť našich zákazníkov. 
                        Okrem ich prístupu k nášmu biznisu … <span>čítať viac</span></p>
                </section>
                <section class="box2">
                    <p>S UX tímom Riešení úzko spolupracujeme už dlhé roky a sú dôležitým partnerom nášho biznisu. 
                        Vďaka ich know-how pre nás od samého začatku správne nastavili zdravý pomer prvotriedneho dizajnu a funkčnosti webu,
                        ktorý následne vylepšovali pomocou relevantných analýz a dát. 
                        Aj ich zásluhou … <span>čítať viac</span></p>
                </section>
            </article>
        </main>
    </div>
</template>

<script>
</script>

<style scoped>
header {
    width: 100%;
    height: 34.625em;
    background: linear-gradient(159deg, #3D2E80 51.38%, #DC1969 125.72%);
}
.logo-btn {
    display: flex;
    justify-content: space-around;
    padding-top: 3.56em;
}
.logo {
    width: 9em;
    height: 3em;
}
.logo-btn button{
    width: 13.5em;
    height: 3em;
    border-radius: 0.5em;
    background: #EE325C;
    border: none;
    color: #FFF;
    text-align: center;
    font-size: 0.875em;
    font-weight: 900;
}
.title {
    display: flex;
    height: 20.3125em;
    justify-content: center;
    padding-top: 0.31em;
}
h1 {
    color: #FFF;
    text-align: center;
    font-size: 3.125em;
    font-style: normal;
    font-weight: 900;
    line-height: 2em;
    width: 14.375em;
}

article {
    display: flex;
    justify-content: center;
}

article h2 {
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
    background-image: url('./../assets/greencircle.svg'); 
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

button {
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
}

.boxes {
    margin-top: 8em;
}

.box1,
.box2 {
    width: 26.25em;
    height: 17.7em;
    border: 1px solid #D6D8DD;
}
.box1 {
    margin-right: 9em;
}

.box1 p,
.box2 p {
    width: 22.56em;
    height: 14em;
    font-size: 1em;
    font-weight: 400;
    line-height: 2em;
    padding: 2em 1.56em 1.75em 2.12em;
}
.box1 span,
.box2 span {
    color: #EE325C;
    font-weight: 700;
}
</style>