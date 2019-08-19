<template>
  <div class="container">
    <div class="card">
      <h3 class="title">HTML</h3>
      <div class="bar">
        <div class="emptybar"></div>
        <div class="filledbar"></div>
      </div>
      <div class="circle">
        <img
          src="https://www.w3.org/html/logo/downloads/HTML5_Badge_512.png"
          alt
          style="width: 80px;"
        />
      </div>
    </div>
    <div class="card">
      <h3 class="title">CSS</h3>
      <div class="bar">
        <div class="emptybar"></div>
        <div class="filledbar"></div>
      </div>
      <div class="circle">
        <img
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/1200px-CSS3_logo_and_wordmark.svg.png"
          alt
          style="width: 80px;"
        />
      </div>
    </div>
    <div class="card">
      <h3 class="title">JS</h3>
      <div class="bar">
        <div class="emptybar"></div>
        <div class="filledbar"></div>
      </div>
      <div class="circle">
        <img src="https://tchol.org/images/javascript-logo-png-3.png" alt style="width: 100px;" />
      </div>
    </div>
    <div class="card">
      <h3 class="title">VueJS</h3>
      <div class="bar">
        <div class="emptybar"></div>
        <div class="filledbar"></div>
      </div>
      <div class="circle">
        <img src="https://vuejs.org/images/logo.png" alt style="width: 80px;" />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>

<style scoped>
body {
  background-color: #031846;
  font-family: "Open Sans", sans-serif;
}

.container {
  position: absolute;
  height: 300px;
  width: 600px;
  top: 60px;
  left: calc(50% - 300px);
  display: flex;
}

.card {
  display: flex;
  height: 280px;
  width: 200px;
  background-color: #031846;
  border-radius: 10px;
  box-shadow: -1rem 0 3rem #031846;
  /*   margin-left: -50px; */
  transition: 0.4s ease-out;
  position: relative;
  left: 0px;
}

.card:not(:first-child) {
  margin-left: -50px;
}

.card:hover {
  transform: translateY(-20px);
  transition: 0.4s ease-out;
}

.card:hover ~ .card {
  position: relative;
  left: 50px;
  transition: 0.4s ease-out;
}

.title {
  color: white;
  font-weight: 300;
  position: absolute;
  left: 20px;
  top: 15px;
}

.bar {
  position: absolute;
  top: 100px;
  left: 20px;
  height: 5px;
  width: 150px;
}

.emptybar {
  background-color: #2e3033;
  width: 100%;
  height: 100%;
}

.filledbar {
  position: absolute;
  top: 0px;
  z-index: 3;
  width: 0px;
  height: 100%;
  background: rgb(0, 154, 217);
  background: linear-gradient(
    90deg,
    rgb(217, 25, 0) 0%,
    rgba(217, 147, 0, 1) 40%,
    rgb(5, 131, 21) 100%
  );
  transition: 0.6s ease-out;
}

.card:hover .filledbar {
  width: 100%;
  transition: 0.4s ease-out;
}

.circle {
  color: white;
  position: absolute;
  top: 150px;
  left: calc(50% - 60px);
}

.stroke {
  stroke: white;
  stroke-dasharray: 360;
  stroke-dashoffset: 360;
  transition: 0.6s ease-out;
}

svg {
  fill: #17141d;
  stroke-width: 2px;
}

.card:hover .stroke {
  stroke-dashoffset: 100;
  transition: 0.6s ease-out;
}
</style>