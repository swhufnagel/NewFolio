<template>
  <v-content class="ma-0 pa-0">
    <div id="landing">
      <v-parallax
        id="parralax"
        src="https://scontent.fapa1-1.fna.fbcdn.net/v/t1.0-9/13438952_10157027950280335_1023770913506391617_n.jpg?_nc_cat=108&_nc_oc=AQkvq7F2nFEH9MyJhSqjfjwnOKgVfQ8Oh1jKpch29B9e3TtlojyAXuiG8JSIXAu_gUPvJxRDiNQWkO5bLNyxyVh2&_nc_ht=scontent.fapa1-1.fna&oh=8d8d8178e7f921e8e2511c7304f65439&oe=5DBF5CA4"
        style="height: 100%; opacity:0.7;"
      >
        <div>
          <h1 id="welcome">Welcome to my Portfolio</h1>
          <div id="my-div">Sean Hufnagel</div>
          <h2 id="uxui">User Experience / User Interface</h2>
          <h3 id="design">Designer / Developer</h3>
          <p id="learn">Learn about me!</p>
        </div>
      </v-parallax>
    </div>
    <div id="about">
      <h1>About</h1>
      <div></div>
      <div>
        <p id="aboutP">
          User-focused full stack web-developer that specializes in Javascript.
          Spent the last 5 years honing my technical skills to become a confident
          programmer, completing my Associates Degree in Computer Programming as
          well as earning my certificate at DU’s intensive web-development
          bootcamp program. I keep my head down and don’t stop until the job is
          and task is complete. I have 10 years experience in customer service
          so I am driven to provide an ideal User Experience in my products. I
          have advanced experience with web development languages including but
          not limited to HTML, CSS, Javascript, React & MySQL. Being a quick
          learner made it possible for me to grasp the context of programming
          language and move on to apply it. My optimistic spirit drives the whole
          team to excel and perform without hesitation, I strive to succeed with
          no alternative.
        </p>
      </div>
    </div>
    <div id="skills">
      <div id="skillBox">
        <v-parallax
          id="skillsBack"
          src="https://www.chainimage.com/images/apple-mac-os-x-lion-wallpapers-hd-desktop-wallpapers-pink-forest.jpg"
          style="height: 700px; opacity:0.8;"
        >
          <v-flex></v-flex>
          <v-container>
            <v-card>
              <v-card-title class="green lighten-2">
                <span class="headline white--text">Skills</span>

                <v-spacer></v-spacer>
              </v-card-title>

              <v-list>
                <v-list-tile class="skillArea">
                  <v-list-tile-content id="tryThis">
                    <v-list-tile-title class="skillTitle">HTML/CSS</v-list-tile-title>
                    <v-flex class="iconList" md12 s6>
                      <i class="devicon-bootstrap-plain-wordmark colored"></i>
                      <i class="devicon-html5-plain-wordmark colored"></i>
                      <i class="devicon-css3-plain-wordmark colored"></i>
                      <i class="devicon-react-original"></i>
                      <i class="devicon-sass-original colored"></i>
                      <i class="devicon-foundation-plain colored"></i>
                    </v-flex>
                  </v-list-tile-content>
                </v-list-tile>
                <v-divider></v-divider>
                <v-list-tile class="skillArea">
                  <v-list-tile-content id="tryThis">
                    <v-list-tile-title class="skillTitle">Javascript</v-list-tile-title>
                    <v-flex class="iconList" md12 s6>
                      <i class="devicon-javascript-plain colored"></i>
                      <i class="devicon-react-original colored"></i>
                      <i class="devicon-vuejs-plain"></i>
                      <i class="devicon-jquery-plain-wordmark"></i>
                      <i class="devicon-nodejs-plain-wordmark colored"></i>
                    </v-flex>
                  </v-list-tile-content>
                </v-list-tile>
                <v-divider></v-divider>
                <v-list-tile class="skillArea">
                  <v-list-tile-content id="tryThis">
                    <v-list-tile-title class="skillTitle">Back-End</v-list-tile-title>
                    <v-flex class="iconList" md12 s6>
                      <i class="devicon-express-original-wordmark colored"></i>
                      <i class="devicon-mysql-plain-wordmark colored"></i>
                      <i class="devicon-mongodb-plain-wordmark colored"></i>
                      <i class="devicon-nodejs-plain colored"></i>
                      <i class="devicon-sequelize-plain-wordmark colored"></i>
                      <i class="devicon-heroku-original-wordmark colored"></i>
                      <i class="devicon-amazonwebservices-plain-wordmark colored"></i>
                    </v-flex>
                  </v-list-tile-content>
                </v-list-tile>
                <v-divider></v-divider>
                <v-list-tile class="skillArea">
                  <v-list-tile-content id="tryThis">
                    <v-list-tile-title class="skillTitle">Design</v-list-tile-title>
                    <v-flex class="iconList" md12 s6>
                      <i class="devicon-photoshop-plain"></i>
                      <i class="devicon-gimp-plain colored"></i>
                      <i class="devicon-illustrator-plain colored"></i>
                    </v-flex>
                  </v-list-tile-content>
                </v-list-tile>
                <v-divider></v-divider>
                <v-list-tile class="skillArea">
                  <v-list-tile-content id="tryThis">
                    <v-list-tile-title class="skillTitle">Other</v-list-tile-title>
                    <v-flex class="iconList" md12 s6>
                      <i class="devicon-babel-plain colored"></i>
                      <i class="devicon-github-plain colored"></i>
                      <i class="devicon-gitlab-plain colored"></i>
                      <i class="devicon-mocha-plain colored"></i>
                      <i class="devicon-slack-plain colored"></i>
                      <i class="devicon-visualstudio-plain colored"></i>
                      <i class="devicon-webpack-plain colored"></i>
                    </v-flex>
                  </v-list-tile-content>
                </v-list-tile>
              </v-list>
            </v-card>
          </v-container>
        </v-parallax>
      </div>
    </div>
    <div id="portfolio">
      <h1>Portfolio</h1>
      <div id="projectBox">
        <v-container grid-list-md text-xs-center>
          <v-layout row wrap>
            <template v-for="(item,index) in items">
              <v-flex :key="index">
                <v-card id="projCards">
                  <v-img id="icons" :src="item.image"></v-img>
                  <v-list-tile-content id="projTitle">
                    <v-card-title id="cardTitle" v-bind="item.title">{{item.title}}</v-card-title>
                    <v-list-tile-sub-title>{{ item.text }}</v-list-tile-sub-title>
                  </v-list-tile-content>
                  <v-card-actions>
                    <v-btn @click="openApp(index)" flat color="orange">App</v-btn>
                    <v-btn @click="openCode(index)" flat color="orange">Github</v-btn>
                  </v-card-actions>
                </v-card>
              </v-flex>
            </template>
          </v-layout>
        </v-container>
      </div>
    </div>

    <div id="contact">
      <v-container fluid fill-height>
        <v-layout align-center justify-center>
          <v-flex xs12 sm8 md4>
            <v-card class="elevation-12">
              <v-toolbar dark color="gray">
                <v-toolbar-title>Contact Me!</v-toolbar-title>
                <v-spacer></v-spacer>
              </v-toolbar>
              <v-card-text>
                <v-form>
                  <v-text-field prepend-icon="person" name="login" label="Login" type="text"></v-text-field>
                  <v-text-field
                    id="password"
                    prepend-icon="email"
                    name="password"
                    label="Password"
                    type="password"
                  ></v-text-field>
                  <v-textarea name="input-7-1" box label="How Can I help you?" auto-grow value></v-textarea>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn dark color="black">Send</v-btn>
              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </div>
  </v-content>
</template>

<script type="application/javascript" src="../../public/assets/js/animation.js"></script>
<script>
import pokemonIcon from "../../public/assets/photos/pokeomonicon.jpg";
import rpsIcon from "../../public/assets/photos/rpsicon.png";
import giphyIcon from "../../public/assets/photos/giphyicon.png";
import nflIcon from "../../public/assets/photos/nflicon.png";
import tunedeaIcon from "../../public/assets/photos/tunedeaicon.png";
import friendIcon from "../../public/assets/photos/friendIcon.png";
import burgerIcon from "../../public/assets/photos/burgerIcon.png";
import mongoIcon from "../../public/assets/photos/mongoIcon.jpeg";
import PostivismIcon from "../../public/assets/photos/postivismIcon.png";
import SayHayIcon from "../../public/assets/photos/SayHayIcon.png";
import amazonIcon from "../../public/assets/photos/amazonIcon.png";
import xmenIcon from "../../public/assets/photos/xmenIcon.png";

export default {
  data: () => ({
    drawer: null,
    isActive: true,
    items: [
      {
        image: pokemonIcon,
        title: "Pokemon Battle",
        appUrl: "https://swhufnagel.github.io/RPG-Game/",
        codeUrl: "https://github.com/swhufnagel/RPG-Game"
      },
      {
        image: tunedeaIcon,
        title: "Tunedea",
        appUrl: "https://swhufnagel.github.io/Project-1/",
        codeUrl: "https://github.com/swhufnagel/Project-1"
      },
      {
        image: rpsIcon,
        title: `Rock Paper Scissor`,
        appUrl: "https://swhufnagel.github.io/RPS-Multiplayer/",
        codeUrl: "https://github.com/swhufnagel/RPS-Multiplayer"
      },
      {
        image: giphyIcon,
        title: "Gif Showcase",
        appUrl: "https://swhufnagel.github.io/GifTastic/",
        codeUrl: "https://github.com/swhufnagel/GifTastic"
      },
      {
        image: nflIcon,
        title: "NFL Trivia",
        appUrl: "https://swhufnagel.github.io/TriviaGame/",
        codeUrl: "https://github.com/swhufnagel/TriviaGame"
      },
      {
        image: xmenIcon,
        title: "Memory Game",
        appUrl: "https://swhufnagel.github.io/Clicky-Game/",
        codeUrl: "https://github.com/swhufnagel/clicky-game"
      },
      {
        image: PostivismIcon,
        title: "Postivism",
        appUrl: "https://www.postivism.herokuapp.com",
        codeUrl: "https://github.com/swhufnagel/Project2"
      },
      {
        image: SayHayIcon,
        title: "Say Hay",
        appUrl: "https://testflight.apple.com/join/tO1A4iRa",
        codeUrl: "https://github.com/swhufnagel/Project-3"
      },
      {
        image: mongoIcon,
        title: "Mongo Scraper",
        appUrl: "https://swh-mongoscraper.herokuapp.com/",
        codeUrl: "https://github.com/swhufnagel/MongoScraper"
      },
      {
        image: burgerIcon,
        title: "Burger Time",
        appUrl: "https://burger-menu-swh.herokuapp.com/",
        codeUrl: "https://github.com/swhufnagel/burger"
      }
    ]
  }),
  props: {
    source: String
  },
  methods: {
    addActiveClass: function() {
      return (this.isActive = !this.isActive);
    },
    openApp: function(index) {
      window.open(this.items[index].appUrl, "_blank");
    },
    openCode: function(index) {
      window.open(this.items[index].codeUrl, "_blank");
    }
  },
  mounted() {
    if (window.innerWidth < 700) {
      // this.$router.push("HelloWorld");
      console.log("Mobile");
    }
  }
};
</script>

<style scoped>
#about,
#skills,
#portfolio {
  width: 110%;
  position: relative;
  right: 3%;
  height: 700px;
}
#contact {
  width: 110%;
  position: relative;
  right: 3%;
  height: 700px;
}
#tryThis {
  height: 200px;
  overflow: none !important;
  margin: auto;
}
#about {
  background-color: rgba(211, 211, 211, 0.411) !important;
}
#aboutP {
  width: 70%;
  text-align: center;
  margin: auto;
}
#cardTitle {
  text-align: center;
  margin: auto;
}
#skills {
  /* background-color: rgba(255, 186, 58, 0.692); */
}
#contact {
  background-color: rgba(11, 11, 88, 0.479);
}
h1,
p {
  text-align: center;
}
#icons {
  height: 200px;
  width: 200px;
}
#projTitle {
  height: 30px;
  margin-bottom: 0px;
}
#my-div {
  text-align: center;
  font-size: 60px;
  font-family: cursive;
}
.skillArea {
  height: 115px;
  background-color: blue(255, 255, 255, 0) !important;
  overflow: none;
}
.iconList {
  margin: auto;
  overflow: none;
}
[class*=" devicon-"],
[class^="devicon-"] {
  font-size: 3rem;
}
.skillTitle {
  margin-top: 3%;
  text-align: center;
  overflow: none;
  text-decoration: underline;
}

#uxui {
  text-align: center;
  color: black;
}
#design {
  text-align: center;
  color: black;
}
#learn {
  color: black;
  text-align: center;
}
#skillsBack {
  margin-top: -90px;
  z-index: 0;
}
#skillsText {
  z-index: 9999;
  color: black;
  opacity: 0.9;
  text-align: center;
  font-size: 36px;
}
#projCards {
  margin-top: 10px;
  width: 200px;
}
#welcome {
  text-align: center;
  position: relative;
  font-family: sans-serif;
  text-transform: uppercase;
  font-size: 2em;
  letter-spacing: 4px;
  overflow: hidden;
  background: linear-gradient(90deg, #000, #fff, #000);
  background-repeat: no-repeat;
  background-size: 80%;
  animation: animate 3s linear infinite;
  -webkit-background-clip: text;
  -webkit-text-fill-color: rgba(255, 255, 255, 0);
}
@keyframes animate {
  0% {
    background-position: -500%;
  }
  100% {
    background-position: 500%;
  }
}
#parralax {
  width: 110%;
  right: 3.5%;
}
#landing {
  height: 800px;
}
</style>
