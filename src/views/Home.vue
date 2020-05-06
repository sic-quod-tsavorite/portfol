<template>
  <v-card>
    <v-tabs vertical fixed-tabs background-color="$cDark" dark>
      <v-tab>Home</v-tab>
      <v-tab>Videos</v-tab>
      <v-tab>Projects</v-tab>
      <v-tab>About Me</v-tab>
      <v-tab-item>
        <v-card flat height="100vh" class="page one" id="page1">
          <v-card-text>
            <div class="container">
              <span class="fName">Martin</span>
              <span class="sName">Sørensen</span>
              <v-card
                raised
                color="$almostWhite"
                max-width="400px"
                id="boutMe"
              >Multimedia design student at EASV in Esbjerg</v-card>
            </div>
            <v-img
              id="meLogo"
              src="https://cdn.discordapp.com/attachments/294221981455220737/707523986795397172/mig-vhs-edit-smol-800-800.png"
            ></v-img>
            <h1 class="welcometxt" data-text="Welcome to my portfolio">Welcome to my portfolio</h1>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat height="100vh" class="page two" id="page2">
          <v-card-text>
            <v-container>
              <h1>Video Projects</h1>
              <v-row justify="space-between">
                <v-lazy
                  v-model="isActive"
                  :options="{threshold: 0.5}"
                  min-height="200"
                  transition="fade-transition"
                >
                  <div id="videos">
                    <h2>Animation project</h2>
                    <iframe
                      width="560"
                      height="315"
                      src="https://www.youtube.com/embed/rCxzlAfkGBI"
                      frameborder="0"
                      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                      allowfullscreen
                    ></iframe>
                  </div>
                </v-lazy>
                <v-lazy
                  v-model="isActive"
                  :options="{threshold: 0.5}"
                  min-height="200"
                  transition="fade-transition"
                >
                  <div id="videos">
                    <h2>Video project made with short time limit</h2>
                    <iframe
                      width="560"
                      height="315"
                      src="https://www.youtube.com/embed/VaDvrAkslCk"
                      frameborder="0"
                      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                      allowfullscreen
                    ></iframe>
                  </div>
                </v-lazy>
                <v-lazy
                  v-model="isActive"
                  :options="{threshold: 0.5}"
                  min-height="200"
                  transition="fade-transition"
                >
                  <div id="videos">
                    <h2>Promotion project for Fanø CMS</h2>
                    <iframe
                      width="560"
                      height="315"
                      src="https://www.youtube.com/embed/zuGXpow5d6A"
                      frameborder="0"
                      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                      allowfullscreen
                    ></iframe>
                  </div>
                </v-lazy>
                <v-lazy
                  v-model="isActive"
                  :options="{threshold: 0.5}"
                  min-height="200"
                  transition="fade-transition"
                >
                  <div id="videos">
                    <h2>Made up internet commercial project</h2>
                    <iframe
                      width="560"
                      height="315"
                      src="https://www.youtube.com/embed/aMF6Mrzyy04"
                      frameborder="0"
                      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                      allowfullscreen
                    ></iframe>
                  </div>
                </v-lazy>
              </v-row>
            </v-container>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat height="100vh" class="page three" id="page3">
          <v-card-text>
            <v-container>
              <h1>
                Other Projects
                <br />Click to open in new tab
              </h1>
              <v-row justify="space-between">
                <div id="projects">
                  <a href="http://www.simplehistory.top/" target="_blank">
                    <h2>Website exam project, Subject: Space</h2>
                    <v-img
                      id="projectimg"
                      src="https://cdn.discordapp.com/attachments/294221981455220737/707665938614583326/1UVua5uZ5CE-c_PzBYtn76KlZQYyxz9qPr871oJw.png"
                    ></v-img>
                  </a>
                </div>
                <div id="projects">
                  <a
                    href="https://cdn.discordapp.com/attachments/294221981455220737/707685567126569010/GERALT_-_SHEPARD_FAIREY.png"
                    target="_blank"
                  >
                    <h2>Image in the style of Shepard Fairey</h2>
                    <v-img
                      id="projectimg"
                      src="https://cdn.discordapp.com/attachments/294221981455220737/707685567126569010/GERALT_-_SHEPARD_FAIREY.png"
                    ></v-img>
                  </a>
                </div>
              </v-row>
            </v-container>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat height="100vh" class="page four" id="page4">
          <v-card-text>
            <v-tabs>
              <v-tab>CV</v-tab>
              <v-tab>Card</v-tab>
              <v-tab-item>
                <iframe
                  src="https://docs.google.com/gview?url=https://cdn.discordapp.com/attachments/294221981455220737/707560387150610502/martin_s_cv_only.pdf&embedded=true"
                  style="width:40%; height:90vh;"
                  frameborder="1"
                >CV</iframe>
                <a
                  href="https://docs.google.com/gview?url=https://cdn.discordapp.com/attachments/294221981455220737/707560387150610502/martin_s_cv_only.pdf&embedded=true"
                  target="_blank"
                >cv</a>
              </v-tab-item>
              <v-tab-item>
                <iframe
                  src="https://docs.google.com/gview?url=https://cdn.discordapp.com/attachments/294221981455220737/707560381991747644/martin_s_card_only.pdf&embedded=true"
                  style="width:40%; height:90vh;"
                  frameborder="1"
                >Card</iframe>
              </v-tab-item>
            </v-tabs>
          </v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    isActive: false
  })
};
</script>

<style lang="scss">
* {
  scrollbar-width: none;
  -ms-overflow-style: none;
}
::-webkit-scrollbar {
  display: none;
}

#page1 {
  background-color: $almostWhite;
  background-image: url(https://cdn.discordapp.com/attachments/294221981455220737/707548895332401243/p1bg.svg);
  background-size: 95vw;
  animation: circleLoad 1s 1;
}

.container {
  margin-top: 10%;
  span {
    display: block;
  }
}

.fName {
  color: $almostWhite;
  font-size: 60px;
  font-weight: 700;
  letter-spacing: 8px;
  margin-bottom: 20px;
  animation: fText 2s 1;
}
.sName {
  font-size: 30px;
  color: $cTextdark;
  animation: sText 2s 1;
}

#meLogo {
  position: fixed;
  top: 10%;
  right: 10%;
  height: 500px;
  width: 500px;
  transition: 0.5s;
  animation: meImgLoad 1s 1;
}
#meLogo:hover {
  transition: 0.5s;
  height: 550px;
  width: 550px;
  margin: -25px -25px auto auto;
}

#boutMe {
  opacity: 100%;
  animation: meTextLoad 2s 1;
  font-size: 30px;
  padding: 10px;
  margin-top: 15px;
  line-height: 35px;
}

.welcometxt {
  position: absolute;
  font-family: "Open Sans", sans-serif;
  bottom: 10%;
  right: -22%;
  transform: translate(-50%, -50%);
  font-size: 6em;
  color: $cTextdark;
  text-shadow: 0 0 20px $cRed;
  z-index: 4;
  animation: welLoad 1s 1;
}
.welcometxt::after {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  z-index: 3;
  color: $cRed;
  filter: blur(12px);
}
.welcometxt::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: $cLred;
  z-index: 2;
  opacity: 0.5;
  filter: blur(40px);
}

@keyframes circleLoad {
  from {
    background-size: 0%;
  }
  to {
    background-size: 100%;
  }
}
@keyframes fText {
  0% {
    color: $cTextdark;
    margin-bottom: -40px;
    opacity: 0%;
  }
  30% {
    letter-spacing: 25px;
    margin-bottom: -40px;
    opacity: 100%;
  }
  85% {
    letter-spacing: 8px;
    margin-bottom: -40;
  }
}
@keyframes sText {
  0% {
    opacity: 0%;
  }
  50% {
    opacity: 0%;
  }
  100% {
    opacity: 100%;
  }
}
@keyframes meImgLoad {
  from {
    height: 0px;
    width: 0px;
    margin: 250px 250px auto auto;
  }
  to {
    height: 500px;
    width: 500px;
    margin: 0;
  }
}
@keyframes meTextLoad {
  0% {
    opacity: 0%;
  }
  50% {
    margin-left: -200px;
  }
  80% {
    opacity: 0%;
  }
  100% {
    opacity: 100%;
    margin-left: 0px;
  }
}
@keyframes welLoad {
  from {
    font-size: 0;
    right: 0;
  }
  to {
    font-size: 6em;
    right: -22%;
  }
}

#page2 {
  background: $cRed;
  h1 {
    text-align: center;
    margin: -100px auto 100px auto;
    color: $cTextdark;
  }
}

#videos {
  margin-bottom: 30px;
  animation: vidLoad 2s 1;
  h2 {
    margin: -15px auto 2px 2px;
    color: $cTextdark;
    animation: vidtxtLoad 3s 1;
  }
}

@keyframes vidLoad {
  0% {
    opacity: 0%;
    margin-top: -50px;
  }
  100% {
    opacity: 100%;
    margin-top: 0;
  }
}
@keyframes vidtxtLoad {
  0% {
    opacity: 0%;
    margin-left: -50px;
  }
  40% {
    opacity: 0%;
    margin-left: -50px;
  }
  100% {
    opacity: 100%;
    margin-left: 0;
  }
}

#page3 {
  background: $cDark;
  background-image: url(https://cdn.discordapp.com/attachments/294221981455220737/707714623285100574/bcircle1.svg);
  background-size: 60%;
  background-position: center;
  background-position-y: -80vh;
  background-repeat: no-repeat;
  animation: bcirani 3s 1;
  h1 {
    text-align: center;
    margin: -100px auto 100px auto;
    color: $cTextdark;
    line-height: 25px;
  }
}

#projects {
  a {
    text-decoration: none;
  }
  h2 {
    color: $almostWhite;
    text-align: center;
    transition: 0.5s;
  }
  :hover {
    h2 {
      text-shadow: 0 0 20px $cRed;
      transition: 0.5s;
    }
    #projectimg {
      filter: grayscale(0%);
      transform: scale(0.98);
      transition: 0.5s;
    }
  }
}

#projectimg {
  width: 500px;
  height: 500px;
  filter: grayscale(100%);
  transition: 0.5s;
  transform: scale(0.9);
}

@keyframes bcirani {
  from {
    background-size: 40%;
  }
  to {
    background-size: 60%;
  }
}

#page4 {
  //background: darkgreen;
}
</style>
