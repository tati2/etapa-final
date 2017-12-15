<template>

<section>
  <section class="titulo">
    <h1>Você sabia?</h1>
    <p class="sub-titulo">Responda perguntas sobre:</p>

   </section> 
  <section class="menu">
    <router-link to="meioambiente">
    <div class="contenier1">
      <div class="meio-ambiente">
        <p>Meio Ambiente</p>           
      </div>
    </div>
    </router-link> 
   <router-link to="saude">
      <div class="contenier2">
        <div class="saude">
          <p>Saúde</p>   
        </div>
      </div>
    </router-link>
  <router-link to="consumoconsciente">
      <div class="contenier3">
        <div class="consumo-consciente">
          <p>Consumo Consciente</p>
        </div>
      </div>
  </router-link> 
  </section>
  <div class="comp">
    <!-- <quiz :quest="quest"></quiz> -->
  </div>
</section>

</template>

<script>

</script>
<style scoped>


h1{
  padding:1%;
  margin: 1%; 
  text-align: left;
  font-weight: normal;
  color:#FFF;
  font-size: 3em;
}
p {
  color:#fff;
  text-decoration:none;
}
 section {
  background-color: #ADFF2F;
  margin: 0;
  position: 0;
}
.titulo {
  text-align: center;
}
.sub-titulo{
  margin:2%;
  text-align: left;
  color: #006400;
  font-size: 1.5em;
}
.menu{ 
  text-align: center;
  justify-content: center;  
  font-size: 2em;
  background-size: cover;
  background-position: center;  
  background-repeat: no-repeat;
  height:100vh;
  

}
/*@media screen and(max-width:1024px){
  
}*/

.meio-ambiente{ 
background-color: rgba(230,120,88,0.5);  
height: 100%;
  
}

.contenier1{
   background-image:url(../assets/meioambiente.jpg);
   height: 40%;
  background-position: center;
 background-repeat: no-repeat;
 background-size: cover; 
 

}

.saude{
  background-color: rgba(230,120,88,0.5);  
  height:100%;
}
.contenier2{
  background-image: url(../assets/saude.jpg);
  height: 40%;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center; 
}
.consumo-consciente{
  background-color: rgba(230,120,88,0.5); 
   height: 100%;
}
.contenier3{
   background-image: url(../assets/consumoconsciente.jpg);
    height:40%;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}

.comp{
  display: none;
}

/*@media screen and (max-width: 320px)*/

</style>

 

