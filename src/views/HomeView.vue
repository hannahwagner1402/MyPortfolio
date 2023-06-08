<template>
  <v-app id="home">
    <NavBar/>
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="intro">Hi! I'm Hannah Wagner, </h1>
              <h1 class="skills">Web Designer & Developer!
              </h1>
              <h4 class="facts"> Ambitious Creative Computing Student at the UAS St. Pölten based in Vienna Austria
                :)</h4>


            </div>
          </v-col>
          <v-col cols="2">
            <div
                style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
                class="mt-16"
            >
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16 align-center">
              <div class="backgr">
                <div class="imgCircle">
                  <v-img class="firstpic" src="intropic.JPG" contain max-height="400"></v-img>
                </div>
              </div>
            </div>
          </v-col>
        </v-row>
      </div>

      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="4" class="mt-13">
              <v-img src="AboutMe.JPG" max-height="400" class="mt-10"></v-img>
            </v-col>
            <v-col cols="12" sm="4" class="mt-5">
              <h2 class="mt-16 mb-3">About Me</h2>
              <div style="width: 120px"></div>

              <p class="text-grey">
                My name is Hannah, and I am a student currently pursuing web design and development. During my time studying, I have acquired a diverse range of skills that enable me to excel in both the coding and design aspects of the field. My coding skills include proficiency in HTML, CSS, Javascript (with experience in Vue.js and Node.js), Kotlin, and basic SQL.
                <br>
                In terms of design, I am well-versed in Adobe Photoshop, After Effects, Illustrator, and InDesign, Procreate, and Figma. In addition, I have experience in user research and user testing, making me knowledgeable in the field of user experience. Outside of my studies, I enjoy drawing, illustrating, video editing, and working on my own projects. I am passionate about expanding my knowledge and skills in coding, designing, and UI/UX, and am eager to learn new things. Thank you for taking the time to learn a little bit about me, and I look forward to the opportunity to work together in the future!
              </p>
            </v-col>
            <v-col cols="12" sm="4" class="mt-13">
              <v-img src="AboutMe2.png" max-height="400" class="mt-10"></v-img>
            </v-col>
          </v-row>
        </div>
      </v-col>

      <div class="dividerMargin">
      <v-divider></v-divider>
      </div>

      <v-col cols="12" class="padd" id="skillsset">

        <div class="text-center mt-12">
          <h2 class="mySkills">My Skillset</h2>
          <div style="width: 120px; margin: 0 auto">
          </div>
        </div>

        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <img class="threeIcons" src="laptop.svg" alt="">

                <h3 class="ml-3 mt-4">Web Development</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  As a web developer, I design and <br>
                  develop websites using various programming<br>
                   languages such as HTML, CSS, and JavaScript.
                </p>
              </div>
              <div class="child">
                <img class="threeIcons" src="mobile.svg" alt="">
                <h3 class="ml-3 mt-4">App Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  As an app designer, I specialize <br>
                  in creating visually appealing and <br>
                  user-friendly mobile applications. <br/>
                </p>
              </div>
              <div class="child">
                <img class="threeIcons" src="uiux.svg" alt="">
                <h3 class="ml-3 mt-4">UI/UX Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I prioritize creating enjoyable user  <br>
                  experiences and conduct user research and<br>
                  testing to help meet the needs of the users <br>
                </p>
              </div>
            </v-col>
          </v-row>

        </div>

<h2 class="skillSeperator">Technologies used:</h2>
        <div class="iconContainer">
          <div class="skillIconWrapper">
            <img class="skillIcons" src="js.svg" alt="JavaScript">
            <h3 class="skillDescription">Javascript</h3>
          </div>
          <div class="skillIconWrapper">
            <img class="skillIcons" src="css3-alt.svg" alt="CSS3">
            <h3 class="skillDescription">CSS</h3>
          </div>
          <div class="skillIconWrapper">
            <img class="skillIcons" src="vuejs.svg" alt="CSS3">
            <h3 class="skillDescription">Vue.js</h3>
          </div>
          <div class="skillIconWrapper">
            <img class="skillIcons" src="figma.svg" alt="CSS3">
            <h3 class="skillDescription">Figma</h3>
          </div>
          <div class="skillIconWrapper">
            <img class="skillIcons" src="html5.svg" alt="CSS3">
            <h3 class="skillDescription">HTML</h3>
          </div>
          <div class="skillIconWrapper">
            <img class="skillIcons" src="android.svg" alt="CSS3">
            <h3 class="skillDescription">Kotlin</h3>
          </div>
          <div class="skillIconWrapper">
            <img class="skillIcons" src="node-js.svg" alt="CSS3">
            <h3 class="skillDescription">Node-js</h3>
          </div>
          <div class="skillIconWrapper">
            <img class="skillIcons" src="unity.svg" alt="CSS3">
            <h3 class="skillDescription">Unity</h3>
          </div>

        </div>

        <v-divider></v-divider>
      </v-col>


      <v-col cols="12" class="imgHover mb-12">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card
                    :elevation="isHovering ? 12 : 2"
                    :class="{ 'on-hover': isHovering }"
                    v-bind="props"
                    @click="openNewPage(item.img)"
                    style="cursor: pointer"
                >
                  <v-img :src="item.img" height="225px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>

      <v-col cols="12" sm="12">
        <hr class="v-divider">
      </v-col>

      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>


          <div class="child2">

            <h1 class="contact">Contact info</h1>
            <h2 class="linc">Github</h2>
            <h2 class="linc">LinkedIn</h2>
            <h2 class="linc">Email</h2>
            <h2 class="linc">Instagram</h2>
          </div>

        </v-row>
      </v-col>
    </v-container>
    <FooterView/>
  </v-app>

</template>

<script>
import {defineComponent} from "vue";
import NavBar from "../components/NavBar.vue";
import FooterView from "../components/FooterView.vue";

// Components
//import HelloWorld from '../components/HelloWorld.vue';

export default defineComponent({
  name: "HomeView",
  setup() {
    const items = [
      {
        img: "kindcosmetics.png",
      },
      {
        img: "clearmind.png",
      },
      {
        img: "easy.png",
      },
      {
        img: "2dga.png",
      },
      {
        img: "omme2.png",
      },
      {
        img: "todo2.png",
      },
      {
        img: "gdds.png",
      },
      {
        img: "frostbite.png",
      },
      {
        img: "snake.png",
      },
    ];

    const openNewPage = (imageSrc) => {
      const newWindow = window.open("", "_blank");
      newWindow.document.write(`
    <!DOCTYPE html>
    <html>
      <head>
        <title>Detail Page</title>
        <style>
          html, body {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden;
          }
          img {
            width: 100%;
            height: 100%;
            object-fit: contain;
          }
        </style>
      </head>
      <body>
        <img src="${imageSrc}" alt="Full Screen Image">
      </body>
    </html>
  `);
      newWindow.document.close();
    };

    return {
      items,
      openNewPage,
    };
  },
  components: {
    NavBar,
    FooterView,
  },
});
</script>

<style scoped>
.v-container {
  padding: 16px 0 16px 0;
}


.skillSeperator {
  text-align: center;
}
.threeIcons{
  height: 80px;
  width: 80px;
  background-color: #B1DD9E;
  padding: 15px;
  border-radius: 30%;
}

.dividerMargin{
  margin-top: 35px;
}
.mySkills {
  font-size: 45px;
  margin-bottom: 20px;
}

.iconContainer {
  margin-left: auto;
  margin-right: auto;
  display: flex;
  flex-wrap: wrap;
  width:45%;
  justify-content: center;
  align-items: center;
  margin-bottom: 50px;
  margin-top: 60px;
}

.skillIconWrapper {
  display: inline-block;
  background-color: #E8E8E8;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
  margin-right: 25px;
  margin-bottom: 25px;
  transition: transform 0.4s ease-in-out, background-color 0.4s ease-out;
  transform-origin: bottom;
}

.skillIconWrapper:hover {
  transform: scale(1.1, 1.1);
  transition: background-color 0.4s ease-in-out;
}

.skillDescription {
 font-size: 15px;
  text-align: center;
  color: #5F5F5F;
  border-radius: 0px 0px 10px 10px;
  transition: opacity 0.4s ease-in-out, background-color 0.4s ease-in-out;
}

.skillIcons {
  max-height: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  width:100px;
  height:80px;
  border-radius: 15px;
}


.intro {
  margin-left: 11%;
  display: flex;
  justify-content: flex-start;
  font-size: 2rem;
}

.skills {
  margin-left: 11%;
  margin-right: 0px;
  display: flex;
  justify-content: flex-start;
  font-size: 4rem;
  line-height: 1.2;
  padding-bottom: 16px;
  padding-top: 10px;
}

.facts {
  margin-left: 11%;
  margin-right: 0px;
  display: flex;
  justify-content: flex-start;
  color: darkgrey;
}

.backgr {
  background-color: #315A39;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 400px;
  height: 400px;
  overflow: hidden;
  border-radius: 50%;
  margin-top: 70px;
}

.firstpic {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 350px;
  height: 350px;
  overflow: hidden;
  border-radius: 50%;
}

.head {
  position: relative;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}

.head:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 130%;
  width: 50%;
  background: black;

}

.head:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 130%;
  width: 50%;
  background: #B1DD9E;
}


.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 1rem 1rem;
  margin-bottom: 20px;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}

.child2 {
  display: flex;
  width: 100%;
  flex-direction: row;
  padding: 2rem 1rem;
  margin-right: 8px;
}

.contact {
  width: 100%;
}

.linc {
  display: flex;
  justify-content: flex-end;
  margin-right: 10px;
  margin-left: 10px;
}

.imgHover {
  padding: 0 200px;
}

.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}

</style>
