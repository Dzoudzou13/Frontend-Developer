<template>
   <footer>
        <div class="text">
            <h1>Máte otázky? Jednoducho sa spýtajte.</h1>
        </div>
        <div class="contact">
            <a href="tel:+421 (02) 555 65 726" class="tel">+421 (02) 555 65 726 </a>
            <a href="mailto:uxdesign@riesenia.com" class="email">uxdesign@riesenia.com</a>
        </div>
        <div class="company">
            <img src="./../assets/images/company.png" alt="RIESENIA">            
        </div>
    </footer>
</template>

<script>
</script>


<style>
footer {
    width: 100%;
    background: linear-gradient(161deg, #3D2E80 38.81%, #DC1969 112.05%);
    display: flex;
    flex-direction: column;
    align-items: center;
}

.text h1 {
    width: 18em;
    font-size: 3em;
    font-weight: 900;
    line-height: 1.69em;
    text-align: center;
    margin-top: 3em;
}
.contact {
    font-size: 1.875em;
    font-weight: 700;
    line-height: 2.5em;
    margin-top: 4em;
}
.tel {
    color: #fff;
    text-decoration: none;
    padding-right: 2em;
}
.email{
   color: #EE325C;
   text-decoration: none;
}
.company {
    margin-top: 8em;
    margin-bottom: 7em;
}

@media screen and (max-width: 800px ) {
    .text h1{
        width: 11em;
        font-size: 1.5em;
        margin-top: 3em    
    }
    .contact {
        display: flex; 
        flex-direction: column;
        align-items: center;
        margin-top: 2em;
        font-size: 1.375em; 
    }
    .tel {
        padding-right: 0em;
    }
    .company{
        margin-top: 5em;
    }
    .company img {
        width: 12em;   
    }
}
</style>