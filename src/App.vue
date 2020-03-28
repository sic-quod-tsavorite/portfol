<template>
  <v-app>
    <v-card>
      <v-tabs vertical fixed-tabs background-color="indigo" dark>
        <v-tab>Home</v-tab>
        <v-tab>Video</v-tab>
        <v-tab>Projects</v-tab>
        <v-tab>Contact</v-tab>
        <v-tab-item>
          <v-card flat height="100vh" class="page one">
            <v-card-text>
              <p>Sed aliquam ultrices mauris. Donec posuere vulputate arcu. Morbi ac felis. Etiam feugiat lorem non metus. Sed a libero.</p>

              <p>Nam ipsum risus, rutrum vitae, vestibulum eu, molestie vel, lacus. Aenean tellus metus, bibendum sed, posuere ac, mattis non, nunc. Aliquam lobortis. Aliquam lobortis. Suspendisse non nisl sit amet velit hendrerit rutrum.</p>

              <p
                class="mb-0"
              >Phasellus dolor. Fusce neque. Fusce fermentum odio nec arcu. Pellentesque libero tortor, tincidunt et, tincidunt eget, semper nec, quam. Phasellus blandit leo ut odio.</p>
            </v-card-text>
          </v-card>
        </v-tab-item>
        <v-tab-item>
          <v-card flat height="100vh" class="page two" color="green darken-1">
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
          <v-card flat height="100vh" class="page three">
            <v-card-text>
              <p>Fusce a quam. Phasellus nec sem in justo pellentesque facilisis. Nam eget dui. Proin viverra, ligula sit amet ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In dui magna, posuere eget, vestibulum et, tempor auctor, justo.</p>

              <p
                class="mb-0"
              >Cras sagittis. Phasellus nec sem in justo pellentesque facilisis. Proin sapien ipsum, porta a, auctor quis, euismod ut, mi. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nam at tortor in tellus interdum sagittis.</p>
            </v-card-text>
          </v-card>
        </v-tab-item>
        <v-tab-item>
          <v-card flat height="100vh" class="page four">
            <v-card-text>
              <v-lazy
                v-model="isActive"
                :options="{
              threshold: 0.5
            }"
                min-height="200"
                transition="fade-transition"
              >
                <p>zxcvxzcvzxcvFusce a quam. Phasellus nec sem in justo pellentesque facilisis. Nam eget dui. Proin viverra, ligula sit amet ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In dui magna, posuere eget, vestibulum et, tempor auctor, justo.</p>

                <p
                  class="mb-0"
                >Cras sagittis. Phasellus nec sem in justo pellentesque facilisis. Proin sapien ipsum, porta a, auctor quis, euismod ut, mi. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nam at tortor in tellus interdum sagittis.</p>
              </v-lazy>
            </v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs>
    </v-card>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    isActive: false
  })
};
</script>

<style>
* {
  scrollbar-width: none;
  -ms-overflow-style: none;
}
::-webkit-scrollbar {
  display: none;
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
}

.one {
  background-image: url(https://cdn.discordapp.com/attachments/266630767671508992/664565449182281738/gene-raz-von-edler-winter-nebulas-by-ellysiumn-as-version.png);
  background-size: 100vw;
}
.two {
  background: darkblue;
}
.three {
  background-image: url(https://cdn.discordapp.com/attachments/294221981455220737/693517665351762020/django.gif);
  background-size: 100vw;
}
.four {
  background: darkgreen;
}
</style>
