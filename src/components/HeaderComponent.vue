<template>
   <header>
            <div class="logo-btn"> 
                <img src="./../assets/logoR.png" alt="logo" class="logo">
                <button @click="openModal">Mám záujem o UX audit</button>
                <teleport to="#app">
                    <div id="modal"  class="bg-modal" v-if="isOpen">
                        <div class="modal-header">
                            <h1>Jednoducho nám napíšte a my sa vám ozveme.</h1>
                            <img src="./../assets/exit.png" alt="" @click="isOpen = false">
                        </div>
                        <form @submit.prevent="odoslatFormular">
                            <div class="name">
                                <p>Meno <span>*</span></p>
                                <input type="text" name="meno" id="meno" v-model="meno" required>
                            </div>
                            <div class="mail-tel">
                                <div class="modal-mail">
                                    <p>E-mail: <span>*</span> </p>
                                    <input type="email" name="email" id="email" v-model="email" required>
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
                        </form>
                        <div class="modal-btn">
                            <button @click="odoslatFormular" type="submit">Kontaktujte ma</button>
                        </div>
                    </div>
                </teleport>
            </div>
            <div class="title">
                <h1>Zvýšte svoje <span>zisky optimalizáciou</span>vášho eshopu.</h1>    
            </div>
            <div class="btn">
                 <button @click="openModal">Mám záujem o UX audit</button>
            </div>
        </header>
</template>

<script>
export default {
    data() {
  return {
    isOpen: false,
    meno: '',
    email: ''
  };
},
methods: {
  openModal() {
    this.isOpen = true;
    console.log("Modal opened");
    this.$nextTick(() => {
      const modal = document.getElementById('modal');
      if (modal) {
        console.log("Modal found, scrolling...");
        modal.scrollIntoView({ behavior: 'smooth'});
      } else {
        console.log("Modal not found");
      }
    });
  },
   odoslatFormular() {
     if (this.meno.trim() === '' || this.email.trim() === '') {
      alert('Prosím vyplňte povinné polia: Meno a Email.');
      document.getElementById('meno').classList.add('error'); 
      document.getElementById('email').classList.add('error'); 
      return false;
    }
    const emailFormat = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    if (!this.email.match(emailFormat)) {
      alert('Prosím zadajte platnú e-mailovú adresu.');
      document.getElementById('email').classList.add('error'); 
      return false;
    }
    alert('Formulár je úspešne odoslaný.');
    return true;
  }
},
  watch: {
    isOpen(value) {
      if (value) {
        document.getElementById('app').classList.add('modal-open')
      } else {
        document.getElementById('app').classList.remove('modal-open')
      }
    }
  }
}
</script>

<style>
header {
    width: 100vw;
    height: 34.625em;
    background: linear-gradient(171deg, #3D2E80 51.38%, #DC1969 125.72%);
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
.btn {
    display: none;
}

/* Modalný formulár */
#app.modal-open {
  opacity: 0.5;
  background-color: rgba(255 , 255, 255, 0.90);
}

.bg-modal {
    position: absolute;
    width: 34.19em;
    border: 1px solid #E7E8EB;
    background: #fff;
    box-shadow: 0px 32px 45px 0px rgba(0, 0, 0, 0.15);
    z-index: 2;
    display: flex;
    flex-direction: column;
    top: 7em;
}

.modal-header {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.bg-modal h1{
    font-size: 1.875em;
    color: #000;
    width: 12.75em;
    height: 6.625em;
    font-weight: 900;
    line-height: 2em;
    margin-top: 3em;
}
.bg-modal img {
    position: relative;
    top: -17em;
    left: 14em;
    cursor: pointer;
}

.bg-modal form {
    margin-top: -7em;
    padding-left: 5em;
}

.bg-modal input {
    width: 32em;
    height: 3.44em;
    border-radius: 0.25em;
    background-color: #EFEFEF;
    border: #EFEFEF;
    padding-left: 2em;
}
.bg-modal p {
    font-weight: 900;
}
.bg-modal span {
    color: #EE325C;
}
.mail-tel {
    display: flex;
}
.mail-tel input {
    width: 13em;
}

.modal-mail {
    margin-right: 3em;
}

.note input{
    padding-bottom: 10em;
}
.note input::placeholder {
    color: #000;
    font-weight: 400;
    font-size: 1em;
}
.modal-btn {
    display: flex;
    justify-content: center;
    margin-bottom: 1em;
}
Button {
    width: 18.7em;
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
.error {
    border-color: #EE325C;
}


@media screen and (max-width: 560px ) {
     .title{
        height: 12.31em;
        margin-top: 3em;
    }
    .title h1 {
        font-size: 1.875em;
        height: 3em;
    }
    .logo-btn button {
        display: none;    
    }
    .bg-modal {
        font-size: 0.7em;
    }
    .bg-modal input {
        width: 22em;
    }
    .mail-tel input {
        width: 8.5em;
    }
    .btn {
        display: flex;
        justify-content: center;    
        margin-top: 4em;
    }
    Button {
        width: 14em;
        font-size: 0.88em;
    }
}

@media screen and (max-width: 360px) {
    .logo-btn {
        justify-content: start;
    }
    .logo-btn button {
        right: 8em;
        min-width: 15.5em;    
    }
    .title h1 {
        display: flex; 
        flex-direction: column;   
    }
}
</style>