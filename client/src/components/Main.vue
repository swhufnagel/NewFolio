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
          <div id="my-div">
            <span v-bind:class="{active: isActive}" v-on:click="addActiveClass">A</span>
            Sean Hufnagel
          </div>
          <h2 id="uxui">User Experience / User Interface</h2>
          <h3 id="design">Designer / Developer</h3>
          <p id="learn">Learn about me!</p>
          <font-awesome-icon icon="coffee"></font-awesome-icon>
        </div>
      </v-parallax>
    </div>
    <div id="about">
      <h1>About</h1>
      <div></div>
      <div>
        <p>
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
                <v-list-tile>
                  <v-list-tile-content>
                    <v-list-tile-title class="skillTitle">HTML/CSS</v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
                <v-divider></v-divider>
                <v-list-tile>
                  <v-list-tile-content>
                    <v-list-tile-title class="skillTitle">Javascript</v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
                <v-divider></v-divider>
                <v-list-tile>
                  <v-list-tile-content>
                    <v-list-tile-title class="skillTitle">Back-End</v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
                <v-divider></v-divider>
                <v-list-tile>
                  <v-list-tile-content>
                    <v-list-tile-title class="skillTitle">Design</v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
                <v-divider></v-divider>
                <v-list-tile>
                  <v-list-tile-content>
                    <v-list-tile-title class="skillTitle">Other</v-list-tile-title>
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
            <template v-for="(item, index) in items">
              <v-list-tile :key="index" xs3>
                <v-flex>
                  <v-card>
                    <v-img :src="item.image" aspect-ratio="2.75"></v-img>

                    <v-card-title v-bind="item.title"></v-card-title>
                    <div>
                      <div>{{ item.text }}</div>
                    </div>

                    <v-card-actions>
                      <v-btn flat color="orange">Code</v-btn>
                      <v-btn flat color="orange">Github</v-btn>
                    </v-card-actions>
                  </v-card>
                </v-flex>
              </v-list-tile>
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
export default {
  data: () => ({
    drawer: null,
    isActive: true,
    items: [
      {
        image: "Brunch this weekend?",
        title: "Pokemon Battle",
        subtitle:
          "I'll be in your neighborhood doing errands this weekend. Do you want to hang out?"
      },
      {
        image: "Summer BBQ",
        title: "Tunedea Music Finder",
        subtitle: "Wish I could come, but I'm out of town this weekend."
      },
      {
        image: "Rock Paper Scissor (Mutli-Player)",
        title: "Sandra Adams",
        subtitle: "Do you have Paris recommendations? Have you ever been?"
      },
      {
        image: "Birthday gift",
        title: "Gif Showcase",
        subtitle:
          "Have any ideas about what we should get Heidi for her birthday?"
      },
      {
        image: "Recipe to try",
        title: "NFL Trivia",
        subtitle:
          "We should eat this: Grate, Squash, Corn, and tomatillo Tacos."
      }
    ]
  }),
  props: {
    source: String
  },
  methods: {
    addActiveClass: function() {
      return (this.isActive = !this.isActive);
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
  height: 550px;
}
#about {
  background-color: rgba(211, 211, 211, 0.411) !important;
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
.skillTitle {
  text-align: center;
}
.skillTitle:before {
  content: "";
  position: absolute;
  text-align: center;
  left: 45%;
  bottom: 0;
  height: 1px;
  width: 10%; /* or 100px */
  border-bottom: 1px solid gray;
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