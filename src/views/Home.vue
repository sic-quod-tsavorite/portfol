<template>
  <v-card>
    <v-tabs vertical fixed-tabs background-color="indigo" dark>
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
            </div>
            <v-img
              id="meLogo"
              src="https://cdn.discordapp.com/attachments/294221981455220737/707523986795397172/mig-vhs-edit-smol-800-800.png"
            ></v-img>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat height="100vh" class="page two" id="page2">
          <v-card-text>
            <p>Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.</p>

            <p>Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.</p>

            <p>Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae tortor. Aliquam eu nunc.</p>

            <p>Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.</p>

            <p
              class="mb-0"
            >Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget, vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi.</p>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat height="100vh" class="page three" id="page3">
          <v-card-text>
            <p>Fusce a quam. Phasellus nec sem in justo pellentesque facilisis. Nam eget dui. Proin viverra, ligula sit amet ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In dui magna, posuere eget, vestibulum et, tempor auctor, justo.</p>

            <p
              class="mb-0"
            >Cras sagittis. Phasellus nec sem in justo pellentesque facilisis. Proin sapien ipsum, porta a, auctor quis, euismod ut, mi. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nam at tortor in tellus interdum sagittis.</p>
          </v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat height="100vh" class="page four" id="page4">
          <v-card-text>
            <v-lazy
              v-model="isActive"
              :options="{
              threshold: 0.5
            }"
              min-height="200"
              transition="fade-transition"
            ></v-lazy>
            <v-btn
              href="https://cdn.discordapp.com/attachments/294221981455220737/707554216964522024/martin_s_cv_v2.pdf"
              type="application/pdf"
              outlined
              rounded="30%"
            >Click Me</v-btn>
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
  //width: 20px;
  display: none;
} /*
::-webkit-scrollbar-track {
  border-radius: 5px;
  box-shadow: inset 0 0 10px grey;
}
::-webkit-scrollbar-track-piece {
  background-color: rgb(0, 1, 59);
}
::-webkit-scrollbar-thumb {
  border-radius: 5px;
  background-color: #170099;
}
::-webkit-scrollbar-thumb:hover {
  background-color: #5661ff;
}

.burger {
  opacity: 100%;
  width: 25px;
  height: 22px;
}

#line1,
#line2,
#line3 {
  width: 25px;
  height: 4px;
  background-color: black;
  transition-duration: 90ms;
  border-radius: 25%;
}

#line2 {
  margin: 5px 0 5px 0;
}

#burger-outer:hover #line1 {
  width: 20px;
  transition-duration: 90ms;
}

#burger-outer:hover #line3 {
  width: 15px;
  transition-duration: 90ms;
}*/

.one {
  background-image: url(https://cdn.discordapp.com/attachments/294221981455220737/707548895332401243/p1bg.svg);
  background-size: 95vw;
  animation: circleLoad 1s 1;
}
.two {
  background: darkgreen;
}
.three {
  background-image: url(https://cdn.discordapp.com/attachments/294221981455220737/693517665351762020/django.gif);
  background-size: 100vw;
}
.four {
  background: darkgreen;
}

.container {
  margin-top: 10%;
  span {
    display: block;
  }
}

.fName {
  z-index: 2;
  color: white;
  font-size: 60px;
  font-weight: 700;
  letter-spacing: 8px;
  margin-bottom: 20px;
  animation: fText 3s 1;
}
.sName {
  z-index: 2;
  font-size: 30px;
  color: black;
  animation: sText 3s 1;
}

@keyframes fText {
  0% {
    color: black;
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

#meLogo {
  position: fixed;
  top: 10%;
  right: 10%;
  height: 500px;
  width: 500px;
  transition: 0.5s;
  animation: meLoad 1s 1;
}
#meLogo:hover {
  transition: 0.5s;
  height: 550px;
  width: 550px;
  margin: -25px -25px auto auto;
}

@keyframes circleLoad {
  from {
    background-size: 0%;
  }
  to {
    background-size: 100%;
  }
}
@keyframes meLoad {
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
/*@media (prefers-color-scheme: light) {
  #page2 {
    background: #fefefe;
  }
}
@media (prefers-color-scheme: dark) {
  #page2 {
    background: rgba(34, 34, 34, 0.933);
  }
}*/
</style>
