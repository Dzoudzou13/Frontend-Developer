<template>
   <header>
            <div class="logo-btn"> 
                <img src="./../assets/images/logoR.png" alt="logo" class="logo">
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
                                <div class="meno">
                                     <input type="text" name="meno" id="meno" v-model="formData.meno">
                                </div>                               
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
            <div class="title">
                <h1>Zvýšte svoje <span>zisky optimalizáciou</span>vášho eshopu.</h1>    
            </div>
            <div class="mobile-btn">
                 <button @click="openModal">Mám záujem o UX audit</button>
            </div>
        </header>
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

<style lang="scss">
header {
    width: 100%;
    height: 34.625em;
    background: linear-gradient(171deg, #3D2E80 51.38%, #DC1969 125.72%);
}
.logo-btn {
    display: flex;
    justify-content: space-around;
    padding-top: 3.56em;
}
button {
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
.logo {
    width: 9em;
    height: 3em;
}
.title {
    display: flex;
    height: 20.3125em;
    justify-content: center;
    padding-top: 0.31em;
    
    h1 {
        color: #FFF;
        text-align: center;
        font-size: 3.125em;
        font-style: normal;
        font-weight: 900;
        line-height: 2em;
        width: 14.375em;
    }
}

.mobile-btn {
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
    
    .modal-header {
        display: flex;
        flex-direction: column;
        align-items: center;
        
        h1 {
            font-size: 1.875em;
            color: #000;
            width: 12.75em;
            height: 6.625em;
            font-weight: 900;
            line-height: 2em;
            margin-top: 3em;
        }
    }

    img {
        position: relative;
        top: -17em;
        left: 14em;
        cursor: pointer;
    }

    form {
        margin-top: -7em;
        margin-left: 3em;
        
        input {
            width: 27rem;
            height: 3.44em;
            border-radius: 0.25em;
            background-color: #EFEFEF;
            border: #EFEFEF;
            padding-left: 2em;
        }
        
        p {
            font-weight: 900;
        }
        
        span {
            color: #EE325C;
        }
    }

    .name {
        display: flex;
        flex-direction: column;
    }
    
    .mail-tel {
        display: flex;
        
        input {
            width: 11.2rem;
        }
    }

    .modal-mail {
        margin-right: 3em;
        display: flex;
        flex-direction: column;
        
        span {
            width: 11em;
        }
    }

    .note input {
        padding-bottom: 10em;
        
        &::placeholder {
            color: #000;
            font-weight: 400;
            font-size: 1em;
        }
    }

    .modal-btn {
        display: flex;
        margin-bottom: 1em;
        
        Button {
            width: 23em;
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
    }

    .error {
        color: #EE325C;
        font-weight: bold;
    }
}

@media screen and (max-width: 560px) {
    .title {
        height: 12.31em;
        margin-top: 3em;
        
        h1 {
            font-size: 1.875em;
            height: 3em;
        }
    }
    
    .logo-btn button {
        display: none;
    }
    
    .bg-modal {
        font-size: 0.6em;
        
        form input {
            width: 16rem;
        }

        .mail-tel input {
        width: 6.3rem;
        }
    }
    
    
    .mobile-btn {
        display: flex;
        justify-content: center;
        margin-top: 4em;
        
        Button {
            width: 15em;
            font-size: 0.88em;
            justify-content: center;
            height: 3em;
            border-radius: 0.5em;
            background: #EE325C;
            border: none;
            color: #FFF;
            text-align: center;
            font-weight: 900;
        }
    }
    
    .modal-btn Button {
        width: 23.5em;
    }
    
    form {
        margin-left: 2.5em;
    }
}

@media screen and (max-width: 360px) {
    .logo-btn {
        justify-content: start;
        margin-left: 1em;
        
        button {
            right: 8em;
            min-width: 15.5em;
        }
    }
    
    .title h1 {
        display: flex;
        flex-direction: column;
    }
}

</style>