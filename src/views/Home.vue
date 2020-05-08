<template>
  <v-card>
    <v-tabs vertical fixed-tabs background-color="$cDark" dark height="100vh">
      <v-tab>Home</v-tab>
      <v-tab>Videos</v-tab>
      <v-tab>Projects</v-tab>
      <v-tab>About Me</v-tab>
      <v-tab-item>
        <v-card flat min-height="100vh" height="100%" id="page1">
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
              src="https://storage.googleapis.com/martinportfolio/items/mig-vhs-edit-smol-800-800.png"
            ></v-img>
            <h1 class="welcometxt" data-text="Welcome to my portfolio">Welcome to my portfolio</h1>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat min-height="100vh" height="100%" id="page2">
          <v-card-text>
            <v-container id="p2cont">
              <h1>Video Projects</h1>
              <v-row justify="space-around">
                <div id="videos">
                  <h2>Animation project</h2>
                  <iframe
                    width="600"
                    height="315"
                    src="https://www.youtube.com/embed/rCxzlAfkGBI"
                    frameborder="0"
                    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen
                  ></iframe>
                </div>
                <div id="videos">
                  <h2>Video project made with short time limit</h2>
                  <iframe
                    width="600"
                    height="315"
                    src="https://www.youtube.com/embed/VaDvrAkslCk"
                    frameborder="0"
                    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen
                  ></iframe>
                </div>
                <div id="videos">
                  <h2>Promotion project for Fanø CMS</h2>
                  <iframe
                    width="600"
                    height="315"
                    src="https://www.youtube.com/embed/zuGXpow5d6A"
                    frameborder="0"
                    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen
                  ></iframe>
                </div>
                <div id="videos">
                  <h2>Made up internet commercial project</h2>
                  <iframe
                    width="600"
                    height="315"
                    src="https://www.youtube.com/embed/aMF6Mrzyy04"
                    frameborder="0"
                    allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen
                  ></iframe>
                </div>
              </v-row>
            </v-container>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat min-height="100vh" height="100%" id="page3">
          <v-card-text>
            <v-container id="p3cont">
              <h1>
                Other Projects
                <br />Click to open in new tab
              </h1>
              <v-row justify="space-around">
                <div id="projects">
                  <a href="http://www.simplehistory.top/" target="_blank">
                    <h2>Website exam project, Subject: Space</h2>
                    <v-img
                      id="projectimg"
                      src="https://storage.googleapis.com/martinportfolio/items/simplehistory.png"
                    ></v-img>
                  </a>
                </div>
                <div id="projects">
                  <a
                    href="https://storage.googleapis.com/martinportfolio/items/GERALT%20-%20SHEPARD%20FAIREY.png"
                    target="_blank"
                  >
                    <h2>Image in the style of Shepard Fairey</h2>
                    <v-img
                      id="projectimg"
                      src="https://storage.googleapis.com/martinportfolio/items/GERALT%20-%20SHEPARD%20FAIREY.png"
                    ></v-img>
                  </a>
                </div>
              </v-row>
            </v-container>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat min-height="100vh" height="100%" id="page4">
          <v-card-text>
            <v-containor>
              <v-row>
                <v-col>
                  <h1>Contact Info</h1>
                  <v-card id="p4card" max-width="70%">
                    <br />Email: mart412f@easv365.dk
                    <br />LinkedIn:
                    <a
                      href="https://www.linkedin.com/in/martin--s%C3%B8rensen/"
                    >@martin--sørensen</a>
                    <br />
                    <br />
                  </v-card>
                </v-col>
                <v-col class="text-center" id="p4col2">
                  <h1>My CV</h1>
                  <v-btn
                    href="https://storage.googleapis.com/martinportfolio/items/martin%20s%20cv%20only.pdf"
                    large
                    target="_blank"
                    id="p4btn"
                  >Click to open</v-btn>
                  <h1>My bussiness card</h1>
                  <v-btn
                    href="https://storage.googleapis.com/martinportfolio/items/martin%20s%20card%20only.pdf"
                    large
                    target="_blank"
                    id="p4btn"
                  >Click to open</v-btn>
                  <h1>My Video CV</h1>
                  <div>
                    <iframe
                      width="560"
                      height="315"
                      src="https://www.youtube.com/embed/qSQsz0ykWZI"
                      frameborder="0"
                      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                      allowfullscreen
                    ></iframe>
                  </div>
                </v-col>
              </v-row>
            </v-containor>
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
// not sure why, men keyframe animations virker ikke med opacity efter jeg builder i vue.

* {
  scrollbar-width: none;
  -ms-overflow-style: none;
}
::-webkit-scrollbar {
  display: none;
}

#page1 {
  background-color: $almostWhite;
  background-image: url(https://storage.googleapis.com/martinportfolio/items/p1bg.svg);
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
  top: 10%;
  right: 10%;
  position: absolute;
  height: 500px;
  width: 500px;
  transition: 0.5s;
  animation: meImgLoad 1s 1;
}
#meLogo:hover {
  transition: 0.5s;
  transform: scale(1.1);
}

#boutMe {
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
  right: -20vw;
  line-break: none;
  transform: translate(-50%, -50%);
  font-size: 600%;
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
  }
  to {
    height: 500px;
    width: 500px;
  }
}
@keyframes meTextLoad {
  0% {
    transform: scale(0);
  }
  80% {
    transform: scale(0.01);
  }
  100% {
    transform: scale(1);
  }
}
@keyframes welLoad {
  from {
    font-size: 0;
    right: 0;
  }
  to {
    font-size: 600%;
    right: -20vw;
  }
}

@media (max-width: 1300px) {
  .welcometxt {
    right: -30vw;
  }
  @keyframes welLoad {
    from {
      font-size: 0;
      right: 0;
    }
    to {
      font-size: 600%;
      right: -30vw;
    }
  }
}

@media (max-width: 1200px) {
  #meLogo {
    top: 10%;
    right: 10%;
    position: absolute;
    height: 200px;
    width: 200px;
  }
  .welcometxt {
    font-size: 500%;
  }
  @keyframes meImgLoad {
    from {
      height: 0px;
      width: 0px;
    }
    to {
      height: 200px;
      width: 200px;
    }
  }
  @keyframes welLoad {
    from {
      font-size: 0;
      right: 0;
    }
    to {
      font-size: 500%;
    }
  }
}

@media (max-width: 770px) {
  #meLogo {
    top: 40%;
    right: 10%;
    position: absolute;
    height: 300px;
    width: 300px;
  }
  .welcometxt {
    font-size: 300%;
  }
  @keyframes meImgLoad {
    from {
      height: 0px;
      width: 0px;
    }
    to {
      height: 300px;
      width: 300px;
    }
  }
  @keyframes welLoad {
    from {
      font-size: 0;
      right: 0;
    }
    to {
      font-size: 300%;
    }
  }
}

#page2 {
  background: $cRed;
  h1 {
    text-align: center;
    margin-bottom: 100px;
    color: $cTextdark;
    font-family: "Open Sans", sans-serif;
  }
}

#p2cont {
  margin-top: 3%;
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
    transform: scale(0);
    margin-top: -50px;
  }
  100% {
    transform: scale(1);
    margin-top: 0;
  }
}
@keyframes vidtxtLoad {
  0% {
    transform: scale(0);
    margin-left: -50px;
  }
  40% {
    transform: scale(0);
    margin-left: -50px;
  }
  100% {
    transform: scale(1);
    margin-left: 0;
  }
}

#page3 {
  background: $cDark;
  background-image: url(https://storage.googleapis.com/martinportfolio/items/bcircle1.svg);
  background-size: 105vh;
  background-position: center;
  background-position-y: -80vh;
  background-repeat: no-repeat;
  animation: bcirani 3s 1;
  h1 {
    text-align: center;
    margin: -100px auto 100px auto;
    color: $cTextdark;
    line-height: 25px;
    font-family: "Open Sans", sans-serif;
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
    background-size: 70vh;
  }
  to {
    background-size: 105vh;
  }
}

@media (max-width: 870px) {
  #p3cont {
    padding-top: 10vh;
  }
}

#page4 {
  background: $almostWhite;
  background-image: url(https://storage.googleapis.com/martinportfolio/items/bcircle1.svg);
  background-size: 70%;
  background-repeat: no-repeat;
  background-position-x: 45vw;
  background-position-y: -10vh;
  animation: p4cirbg 3s 1;
  h1 {
    text-align: center;
    margin: 10px auto;
  }
}

#p4card {
  padding: 10px;
  font-size: 250%;
  line-height: 125%;
  margin: 10% 15% auto auto;
}

#p4col2 {
  padding-top: 10%;
}

#p4btn {
  margin-bottom: 15px;
}

@keyframes p4cirbg {
  0% {
    background-size: 0;
    background-position-x: 100vw;
    background-position-y: 100vh;
  }
  100% {
    background-size: 70%;
    background-position-x: 45vw;
    background-position-y: -10vh;
  }
}
</style>
