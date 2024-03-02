<template>
    <header>
        <section class="logo-btn"> 
            <img src="./../assets/logoR.png" alt="logo" class="logo">
            <button>Mám záujem o UX audit</button>
        </section>
        <section class="title">
            <h1>Zvýšte svoje zisky optimalizáciou vášho eshopu.</h1>    
        </section>
    </header>
</template>

<script>
</script>

<style scoped>
header {
    width: 100%;
    height: 554px;
    background: linear-gradient(159deg, #3D2E80 51.38%, #DC1969 125.72%);
    flex-shrink: 0;
}
.logo-btn {
    display: flex;
    justify-content: space-around;
    padding-top: 57px;
}
.logo {
    width: 145px;
    height: 48.066px;
    flex-shrink: 0;
}
button{
    width: 200px;
    height: 42px;
    flex-shrink: 0;
    border-radius: 8px;
    background: #EE325C;
    border: none;
    color: #FFF;
    text-align: center;
    font-family: Mulish;
    font-size: 14px;
    font-style: normal;
    font-weight: 900;
    padding: 4px 10px;
}
.title {
    display: flex;
    height: 325px;
    justify-content: center;
    flex-shrink: 0;
    padding-top: 92px;
}
h1 {
    color: #FFF;
    text-align: center;
    font-family: Mulish;
    font-size: 50px;
    font-style: normal;
    font-weight: 900;
     width: 694px;
}
</style>