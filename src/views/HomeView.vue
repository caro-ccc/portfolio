<template>
  <v-app id="home">
    <NavBar />
    <vi-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Hola</h1>
              <h1 class="text-grey">Soy Carolina Cocom</h1>
              <span class="text-grey">Est.Turismo</span> <br />
              <v-btn tile darck class="text-red" variant="outlined"
                >contactame</v-btn
              >
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="
                position: absolute;
                z-index: 999;
                bottom: 0%;
                margin-left: auto;
                margin-right: auto;
                left: 0%;
                right: 0%;
                text-align: center;
              "
            ></div>
            <v-icon fas fa-angle-double-down></v-icon>
          </v-col>
          <v-col cols="5">
            <div style="position: absolute; z-index: 9999" class="mt-16"></div>
            <v-img src="../assets/caroli.png" contain max-height="300"></v-img>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="../assets/caroli.png" max-height="200"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h2 class="mt-16"> About Me</h2>
              <div style="width:120px">
                <v-slider v-model="slider2" color="black" label=""></v-slider>

              </div>
              <h4 class="mt-n4"> LLevo 1 año haciendo gomitas con chamoy</h4>
              <h4>Y azulitos</h4>
              <p class="text-grey">Ando en proceso de estudios por ahora. <br>
              Mi capacitación actual asignada es Turismo</p>
              <br>
              <p class="tex-gray">¡Conoceme Más!</p>
              <v-btn title dark color="green" class="mt-4">
                Descargar CV
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h1>Lo que hago.</h1>
        <div style="width: 120px; margin: 0% auto">
          <v-slide v-model="slider2" color="black" label=""> 
          </v-slide>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portafolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fa-regular fa-file-lines" color="orange" class="text-white" ></v-btn>
                <h3 class="ml-3 mt-4"> Gustos</h3>
                <p class="text-grey ,ml-3 mt-4 text-caption">
                  Me gustan varios generos de canciones,<br>tambien
                   me gusta el color rojo <br> y el clima lluvioso o nublado. <br>Algo que me encanta ver <br>antes de dormir es el <br> cielo estrellado y la luna</p>
              </div>
              <div class="child">
                <v-btn icon="fa-brands fa-linux" color="#000080" class="text-white" ></v-btn>
                <h3 class="ml-3 mt-4"> Metas</h3>
                <p class="text-grey ,ml-3 mt-4 text-caption">
                  Las metas que me propongo son <br>como tener un titulo,
                  <br>viajar y conocer el mundo <br>tener un buen de mascotas y poder ser alguien <br>de bien en la vida </p>
              </div>
              <div class="child">
                <v-btn icon=" fa-solid fa-leaf" color="green" class="text-white" ></v-btn>
                <h3 class="ml-3 mt-4"> Pasatiempo</h3>
                <p class="text-grey ,ml-3 mt-4 text-caption">
                  me gusta pasar tiempo haciando la tarea con musica,<br> ver videos de todo tipo <br>
                y salir con amigos de vez en cuando.</p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>

      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="Green" class="mr-2" >Todos</v-btn>
          <v-btn class="mr-2" variant="tonal" >Gustar</v-btn>
          <v-btn class="mr-2" variant="tonal" >Dormir</v-btn>
          <v-btn class="mr-2" variant="tonal" >Socializar</v-btn>
          <v-btn class="mr-2" variant="tonal" >Escuchar Musica</v-btn>
          
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
            <v-col cols="12" md="4" v-for="(item, i) in items" :key="i">
              <v-hover v-slot="{isHovering,props}">
                <v-card :elevation="isHovering ? 12: 2"
              :class="{'on-hover' : isHovering}" v-bind="props">
                <v-img :src="item.img" height="255px" cover></v-img>
            </v-card>
              </v-hover>
            </v-col>
          
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-5">
          <v-btn color="green" class="mt-4"> Conocer mas</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-card class="mw-auto" maz-with="344" height="">
            <v-img src="caroli.png" height="200px cover"></v-img>  
            <v-card-title>misha</v-card-title>
            <v-card-subtitle>misha fue una gato linda </v-card-subtitle>
            <v-card-text>Hay muchos gatitos actualmente por mi casa </v-card-text>
            </v-card>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="biog">
        <div class="hire"></div>
        <v-row>
          <v-col cols="12" sm="8">
            <h1>Contactame para tus proyectos</h1>
            <p> Puedes encontrarme en mis redes sociales o mediante mi numero de telefono puedes contactarte conmigo!<br>(datos encontrados en el Blog).</p>
          </v-col>
          <v-col cols="12" sm="4">
            <v-btn color="green" class="mt-15">Contactame!</v-btn>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="12" id="Blog">
        <div>
          <v-col class="mt-15">
            <h1>Blog</h1>
          </v-col>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
          <div class="child">      
            <h1>Informacion de contacto</h1>     
            <v-btn icon="fa-solid fa-map-location-dot"></v-btn>
            <p class="text-grey ,ml-3 mt-4 text-caption">
             Palmas Turquesa, <br>Calle Pavito Migratorio,<br> Mzn 34, Lt 8. </p>
          </div>
        </v-col>

          <v-col cols="12" sm="4">
          <div class="child">      
            <h1>Number</h1>     
            <v-btn icon="fa-solid fa-square-phone-flip"></v-btn>
            <p class="text-grey ,ml-3 mt-4 text-caption">
             +52 984 134 9458 </p>
             <v-col cols="12" sm="4">
          <div class="child">      
            <h1>Informacion de contacto  </h1>     
            <v-btn icon="fa-solid fa-envelope"></v-btn>
            <p class="text-grey ,ml-3 mt-4 text-caption">
             @caro19852725@gmail.com <br> caro2008cx@gmail.com</p>
          </div>
        </v-col>
        </div>
        </v-col>
        </v-row>
      </v-col>
      <v-col cols="12" sm="8">
          <h1 class="mt-18">Send tour message!!!</h1>
          <v-divider></v-divider>
      <span class="text-captio"></span>
      <v-row class="mt-10">
        <v-col cols="12" sm="6">
          <v-text-field label="Name" persistent-hint outlined></v-text-field>
        </v-col>
       <v-col cols="12" sm="6">
        <v-text-field label="Last name" persistent-hint outlined></v-text-field>
       </v-col>
       <v-col cols="12" sm="6">
        <v-text-field label="Phone number" persistent-hint outlined></v-text-field>
       </v-col>
       <v-col cols="12" sm="6">
        <v-text-field label="Email" persistent-hint outlined></v-text-field>
       </v-col>
       <v-textarea label="Message" persistent-hint outlined></v-textarea>
      </v-row> 
      <v-btn color="green" class="mt-2">Submit</v-btn>        
        </v-col>
    </vi-container>
  </v-app>
</template>

<script>
import { defineComponent } from "vue";

// Components
import NavBar from "../components/NavBar.vue";

export default defineComponent({
  name: "HomeView",
  setup() {
    return {
      slider2: 50,
      items : [
        {img: "caroo.png"},
        {img: "mapache.png"},
      ]
    }
  },

  components: {
    NavBar,
  },
});
</script>

<style scoped>
.v-container {
  padding-top: 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head:before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: rgb(0, 0, 0);
  transform: skew(0deg, 6deg);
}
.head:after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: rgb(0, 0, 0);
  transform: skew(0deg, -6deg);
}
.egg {
  display: block;
  margin-left: 100px;
  margin-top: 100px;
  width: 365px;
  height: 300px;
  background-color: rgba(107, 126, 113, 0.741);
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 0% ;
}
.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}

.imgHover{
  padding: 0 200px;
}
.pre{
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0% 200px;
  background-color: aliceblue;
}
.hire{
width: 100%;
height: 200%;
padding: 0 200%;
background-color: #e9e9e9;
margin-top: -24px;
}
</style>
