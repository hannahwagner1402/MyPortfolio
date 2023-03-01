<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="intro">Hi! I'm Hannah Wagner, </h1>
              <h1 class="skills">Web Designer & Developer!
              </h1>
              <h4 class ="facts"> Ambitious Creative Computing Student at the UAS St. Pölten based in Vienna Austria :)</h4>


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
            <div style="position: relative; z-index: 9999" class="mt-12 align-center">
             <div class="backgr">
               <div class="imgCircle">
              <v-img class="firstpic" src="slay.jpg" contain max-height="300"></v-img>
               </div>
             </div>
            </div>
          </v-col>
        </v-row>
      </div>


      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6" class="mt-10">
              <div class="egg">
                <v-img src="seggsy.png" max-height="300" class=""></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6" class="mt-3">
              <h2 class="mt-16 mb-6">About Me</h2>
              <div style="width: 120px">
              </div>
              <h4 class="mt-n4">I'm so slay pls hire me</h4>

              <p class="text-grey mt-3">
                My name is Hannah, and I am a student currently
                pursuing web design and development. During my time studying,
                I have acquired a diverse range of skills that enable me to excel
                in both the coding and design aspects of the field. My coding skills
                include proficiency in HTML, CSS, Javascript (with experience in Vue.js
                and Node.js), Kotlin, and basic SQL.
              </p>
              <br />
              <p class="text-grey">
                In terms of design, I am well-versed
                in Adobe Photoshop, After Effects, Illustrator, and InDesign,
                Procreate, and Figma. In addition, I have experience in
                user research and user testing, making me knowledgeable in the field of
                user experience. Outside of my studies, I enjoy drawing, illustrating, video editing
                and working on my own projects. I am passionate about expanding my
                knowledge and skills in coding, designing, and UI/UX, and am eager
                to learn new things. Thank you for taking the time to learn a little bit
                about me, and I look forward to the opportunity to work together in the future!
              </p>
            </v-col>
          </v-row>
        </div>
      </v-col>

      <v-col cols="12" class="padd" id="skillsset">

        <div class="text-center mt-16">
        <h2 class="mySkills">MY SKILLZ 😎</h2>
        <div style="width: 120px; margin: 0 auto">
        </div>
      </div>

      <div class = "iconContainer">
        <v-img class="skillIcons" src="js.svg" contain max-height="300"></v-img>
        <v-img class="skillIcons" src="css3-alt.svg" contain max-height="300"></v-img>
        <v-img class="skillIcons" src="vuejs.svg" contain max-height="300"></v-img>
        <v-img class="skillIcons" src="figma.svg" contain max-height="300"></v-img>
        <v-img class="skillIcons" src="html5.svg" contain max-height="300"></v-img>
        <v-img class="skillIcons" src="android.svg" contain max-height="300"></v-img>
        <v-img class="skillIcons" src="node-js.svg" contain max-height="300"></v-img>
      </div>

        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn
                  icon="fa-solid fa-laptop"
                  color="#97CF8A"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Web Development</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  As a web developer, I design and develop <br>
                  websites using various programming languages <br>
                  such as HTML, CSS, and JavaScript.
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fas fa-mobile-alt"
                  color="#97CF8A"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">App Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  As an app designer, I specialize <br>
                  in creating visually appealing and <br>
                  user-friendly mobile applications. <br />
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fas fa-camera"
                  color="#97CF8A"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">UI/UX Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I prioritize creating enjoyable user experiences <br>
                  and conduct user research and testing to ensure that<br>
                  the product meets the needs of the target audience. <br>
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>



      <v-col cols="12" sm="12" id="projects">

        <div class="text-center mt-6">
          <h2 class="mySkills">MY PROJECTS 🤭</h2>
          <div style="width: 120px; margin: 0 auto">
          </div>
        </div>

        <div class="d-flex justify-center mb-8 mt-2">
          <v-btn color="#97CF8A" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web and App Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Web and App Development</v-btn>
          <v-btn class="mr-2" variant="tonal">UI/UX Design</v-btn>
          <v-btn variant="tonal">Illustration/Animation</v-btn>
        </div>
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
                >
                  <v-img :src="item.img" height="225px" cover> </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12" >
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
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from "vue";
import NavBar from "../components/NavBar.vue";
import FooterView from "../components/FooterView.vue";

// Components
//import HelloWorld from '../components/HelloWorld.vue';

export default defineComponent({
  name: "HomeView",
  setup() {
    return {


      items: [
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
      ],
    };
  },
  components: {
    NavBar,
    FooterView
},
});
</script>
<style scoped>
.v-container {
  padding: 16px 0 16px 0;
}

.mySkills{
  margin-bottom: 30px;
  font-family: "Baby Doll";
  font-size: 50px;
}

.iconContainer{
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 66%;
  height: 5%;
}
.skillIcons{
  display: flex;
  width: 100px;
  height: 100px;
}

.intro{
  margin-left: 11%;
  display: flex;
  justify-content: flex-start;
  font-size: 2rem;
}

.skills{
  margin-left: 11%;
  margin-right: 0px;
  display: flex;
  justify-content: flex-start;
  font-size: 4rem;
}

.facts{
  margin-left: 11%;
  margin-right: 0px;
  display: flex;
  justify-content: flex-start;
  color:darkgrey;

}

.backgr{
  background-color: #315A39;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 400px;
  height: 400px;
  overflow: hidden;
  border-radius: 50%;
}

.firstpic {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 300px;
  height: 300px;
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


.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #B1DD9E;
  border-radius: 50% 50% 50% 50% / 60% 60% 50% 50%;
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

.child2 {
  display: flex;
  width: 100%;
  flex-direction: row;
  padding: 2rem 1rem;
  margin-right: 8px;
}
.contact{
width: 100%;
}
.linc{
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
