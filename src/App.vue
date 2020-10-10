<template>
  <v-app>
   <body>
    <header>
        <div id="logo">
            <router-link to="/"><img src="./assets/logoo.svg" alt=""></router-link>
        </div>
        <div id="menu">
            <router-link to="/produkter">Produkter</router-link> 
            <a href="">Priser</a>
            <button><a target="_blank" href="https://mette-pahuus.planway.com">Bestil tid</a></button>
        </div>
        <div id="some">
            <a target="_blank" href="https://www.facebook.com/mettepahuus.frisor/"><img src="./assets/facebook.svg" alt=""></a>
            <a target="_blank" href="https://www.instagram.com/mettepahuus.frisor/?hl=da"><img src="./assets/insta_1.svg" alt=""></a>
        </div>
    </header>
    <div id="caro">
      <v-carousel hide-delimiters cycle>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
    </div>
    <footer>
        <div id="bestil">
            <div id="bestil_tekst">
                <h3>Bestil tid</h3>
                <p>Du kan nemt og hurtigt bestille en tid online. 
                Du skal bare følge linket herunder og derefter følge vejledningen på siden du bliver viderestillet til.</p>
                <button><a target="_blank" href="https://mette-pahuus.planway.com">Bestil tid</a></button>
            </div>
        </div>
        <div id="tider">
            <div id="tider_tekst">
                <h3>Telefontider</h3>
                <div id="dage">
                    <p>Mandag:</p>
                    <p>Tirsdag:</p>
                    <p>Onsdag:</p>
                    <p>Torsdag:</p>
                    <p>Fredag:</p>
                    <p>Lørdag:</p>
                    <p>Søndag:</p>
                </div>
                <div id="tidsp">
                    <p>Lukket</p>
                    <p>9:00 - 17:30</p>
                    <p>9:00 - 17:30</p>
                    <p>9:00 - 17:30</p>
                    <p>9:00 - 17:30</p>
                    <p>Efter aftale</p>
                    <p>Lukket</p>
                </div>
            </div>
        </div>
        <div id="kontakt">
            <div id="kontakt_tekst">
                <h3>Kontakt</h3>
                <div id="txt1">
                    <p>Telefon:</p>
                    <p>E-mail:</p>
                    <p>Adresse:</p>
                </div>
                <div id="txt2">
                    <p>+45 27 63 25 09</p>
                    <p>Mettepahuus@live.dk</p>
                    <p>Torvet 10, st</p>
                    <p>6760 Ribe</p>
                </div>
                <div id="some2">
                    <a target="_blank" href="https://www.facebook.com/mettepahuus.frisor/"><img src="./assets/facebook.svg" alt=""></a>
                    <a target="_blank" href="https://www.instagram.com/mettepahuus.frisor/?hl=da"><img src="./assets/insta_1.svg" alt=""></a>
                </div>
            </div>
        </div>
    </footer>
</body>
  </v-app>
</template>

<script>
export default {
    data () {
      return {
        items: [
          {
            src: 'https://www.2trendy.dk/images/topbillede-vans-08-02-19.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      }
    },
  }
</script>

<style>
body {
    margin: 0;
}

header {
    background-color: white;
    height: 85px;
    display: flex;
    justify-content: center;
    font-size: 19px;
    font-family: 'Open Sans', sans-serif;
}

#logo {
    width: 33%;
    height: 80px;
    display: flex;
    padding-left: 30px;
}

#logo img {
    height: 75px;
    margin: 5px 0 0 10px;
}

#menu {
    width: 33%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

#menu button {
    background-color: #e8e8e8 !important;
    font-size: 18px;
    font-family: 'Open Sans', sans-serif;
    width: 100px;
    height: 35px;
    border: none;
}

#menu button:hover {
    background-color: #d3d3d3 !important;
    transition: 0.5s;
}

a {
    text-decoration: none;
    color: #181818;
}

#some {
    width: 33%;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding-right: 30px;
}

#some img {
    height: 25px;
    margin: 5px 18px 0 0;
}

#caro {
    height: 700px;
    width: 100%;
}

footer {
    height: 270px;
    background-color: #e8e8e8;
    display: flex;
    justify-content: center;
    padding-left: 50px;
}

#bestil, #tider, #kontakt {
    width: 29%;
    display: flex;
    justify-content: center;
    padding-top: 20px;
}


#bestil_tekst, #tider_tekst, #kontakt_tekst {
    width: 60%;
}

#bestil_tekst button {
    background-color: #d3d3d3 !important;
    font-size: 14px;
    font-family: 'Open Sans', sans-serif;
    width: 80px;
    height: 30px;
    border: none;
    margin-top: 30px;
}

#bestil_tekst button:hover {
    background-color: #b8b8b8 !important;
    transition: 0.5s;
}

#tider_tekst, #kontakt_tekst {
    display: flex;
    flex-wrap: wrap;
}

#tider_tekst h3, #kontakt_tekst h3 {
    width: 100%;
}

#dage {
    width: 40%;
    height: 210px;
}

#dage p, #tidsp p {
    margin-bottom: 3px;
}

#tidsp {
    width: 60%;
    height: 210px;
}

#txt1 {
    width: 40%;
    height: 90px;
}

#txt1 p, #txt2 p {
    margin-bottom: 3px;
}

#txt2 {
    width: 60%;
    height: 90px;
}

#some2 {
    width: 100%;
    display: flex;
    justify-content: center;
    height: 110px;
    padding: 20px 0 0 40px;
}

#some2 img {
    height: 25px;
    margin: 5px 18px 0 0;
}

h3 {
    font-size: 19px;
    font-family: 'Open Sans', sans-serif;
    font-weight: lighter;
    margin-bottom: 13px;
}

p {
    font-size: 14px;
    font-family: 'Open Sans', sans-serif;
}

</style>