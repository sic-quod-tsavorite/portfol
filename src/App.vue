<template>
  <v-app>
    <v-speed-dial
      v-model="fab"
      :top="top"
      :bottom="bottom"
      :right="right"
      :left="left"
      :direction="direction"
      :open-on-hover="hover"
      :transition="transition"
    >
      <template v-slot:activator>
        <v-btn v-model="fab" color="blue darken-2" dark fab id="burger-outer">
          <div class="burger">
            <div id="line1"></div>
            <div id="line2"></div>
            <div id="line3"></div>
          </div>
        </v-btn>
      </template>
      <a href="#home" v-smooth-scroll>
        <v-btn fab dark small color="yellow">
          <v-icon>mdi-pencil</v-icon>
        </v-btn>
      </a>
      <a href="#video" v-smooth-scroll>
        <v-btn fab dark small color="green">
          <v-icon>mdi-pencil</v-icon>
        </v-btn>
      </a>
      <a href="#projects" v-smooth-scroll>
        <v-btn fab dark small color="indigo">
          <v-icon>mdi-plus</v-icon>
        </v-btn>
      </a>
      <a href="#contact" v-smooth-scroll>
        <v-btn fab dark small color="red">
          <v-icon>mdi-delete</v-icon>
        </v-btn>
      </a>
    </v-speed-dial>
    <div class="outer-wrapper">
      <div class="wrapper">
        <div class="slide one" id="home"></div>
        <div class="slide two" id="video">
          <v-lazy
            v-model="isActive"
            :options="{
              threshold: 0.5
            }"
            min-height="200"
            transition="fade-transition"
          >
            <v-card class="mx-auto" max-width="336">
              <v-card-title>Card title</v-card-title>

              <v-card-text>
                Phasellus magna. Quisque rutrum. Nunc egestas, augue at
                pellentesque laoreet, felis eros vehicula leo, at malesuada
                velit leo quis pede. Aliquam lobortis. Quisque libero metus,
                condimentum nec, tempor a, commodo mollis, magna. In turpis. In
                dui magna, posuere eget, vestibulum et, tempor auctor, justo. In
                turpis. Pellentesque dapibus hendrerit tortor. Ut varius
                tincidunt libero.
              </v-card-text>
            </v-card>
          </v-lazy>
        </div>
        <div class="slide three" id="projects"></div>
        <div class="slide four" id="contact"></div>
      </div>
    </div>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    direction: 'bottom',
    fab: false,
    fling: false,
    hover: false,
    tabs: null,
    top: true,
    right: false,
    bottom: false,
    left: true,
    transition: 'slide-x-transition',
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

a {
  text-decoration: none;
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

.slide {
  width: 100vw;
  height: 100vh;
}

.outer-wrapper {
  width: 100vh;
  height: 100vw;
  transform: rotate(-90deg) translateX(-100vh);
  transform-origin: top left;
  overflow-y: scroll;
  overflow-x: hidden;
  position: absolute;
  z-index: 0;
}

.wrapper {
  display: flex;
  flex-direction: row;
  width: 400vw;
  transform: rotate(90deg) translateY(-100vh);
  transform-origin: top left;
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
