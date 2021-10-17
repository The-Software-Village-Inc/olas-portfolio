<template>
  <div class="p-0 navb">
    <div class="d-flex justify-content-between">
      <div class="">
        <span>
          <img
            src="https://res.cloudinary.com/sam-kay/image/upload/v1634481142/ola/1_2_vox9xw.png"
            alt=""
        /></span>
      </div>
<!-- 
      <div class="d-flex align-items-center topnav">
        <div class="nav-items"><a href="">Work</a></div>
        <div class="nav-items"><a href="">About</a></div>
        <div class="nav-items"><a href="">Resume</a></div>
        <div class="nav-items mr-0"><a href="">Contact</a></div>
      </div> -->
       <ul class="d-flex align-items-center topnav m-0">
          <li  class="nav-items" @click="toggle">
            <router-link to="/">Work</router-link>
          </li>
         
          <li  class="nav-items" @click="toggle">
            <router-link to="/about">About</router-link>
          </li>
 <li  class="nav-items" @click="toggle">
            <router-link to="/Gallery/all">Resume</router-link>
          </li>
          <li  class="nav-items mr-0" @click="toggle">
            <router-link to="/contact">Contact</router-link>
          </li>
          <!--  <li class="side-link" @click="toggle">
            <router-link to="/pricing">Pricing</router-link>
          </li> -->
        </ul>
      <div class="d-block d-flex d-md-none  align-items-center justify-content-center ">
        <button
          class=" harmburger"
          :class="[{ opened: toggled }]"
          @click="toggle"
          aria-label="Main Menu"
        >
          <svg width="100" height="100" viewBox="0 0 100 100">
            <path
              class="line line1"
              d="M 20,29.000046 H 80.000231 C 80.000231,29.000046 94.498839,28.817352 94.532987,66.711331 94.543142,77.980673 90.966081,81.670246 85.259173,81.668997 79.552261,81.667751 75.000211,74.999942 75.000211,74.999942 L 25.000021,25.000058"
            />
            <path class="line line2" d="M 20,50 H 80" />
            <path
              class="line line3"
              d="M 20,70.999954 H 80.000231 C 80.000231,70.999954 94.498839,71.182648 94.532987,33.288669 94.543142,22.019327 90.966081,18.329754 85.259173,18.331003 79.552261,18.332249 75.000211,25.000058 75.000211,25.000058 L 25.000021,74.999942"
            />
          </svg>
        </button>
      </div>
    </div>
    <transition name="fade">
      <div class="side-nav text-center" v-if="toggled">
        <!-- <div class="paatern">  <img src="../assets/Taieri.png" alt=""></div> -->

        <ul>
          <li class="side-link" @click="toggle">
            <router-link to="/">Work</router-link>
          </li>
         
          <li class="side-link" @click="toggle">
            <router-link to="/about">About</router-link>
          </li>
 <li class="side-link" @click="toggle">
            <router-link to="/Gallery/all">Resume</router-link>
          </li>
          <li class="side-link" @click="toggle">
            <router-link to="/contact">Contact</router-link>
          </li>
          <!--  <li class="side-link" @click="toggle">
            <router-link to="/pricing">Pricing</router-link>
          </li> -->
        </ul>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return { toggled: false };
  },
  methods: {
    toggle() {
      this.toggled = !this.toggled;
    },
  },
};
</script>

<style lang="scss">
.navb {
  position: sticky !important;
  top: 0;
  position: -webkit-sticky;
  z-index:40000;
  background-color: white;
}

.nav-items {
     margin-left:4vw;
    list-style: none;
}

.nav-items a {
  font-family: Open Sans, Arial, Helvetica, sans-serif;
  font-size: 18px;
  font-style: normal;
  font-weight: 600;
  line-height: 25px;
  letter-spacing: 0em;
  color: rgba(171, 175, 193, 1);
  text-decoration: none;
  transition: 0.2s ease-in;

  &:hover {
    color: #000000;
    text-decoration: none;
    transition: 0.4s ease-out;
  }
}
.harmburger {
  background-color: #ffffff;
  border: none;
  cursor: pointer;
  padding: 0;
  left: 0;
  position:relative;
}

.line {
  fill: none;
  stroke: black;
  stroke-width: 6;
  transition: stroke-dasharray 250ms cubic-bezier(0.4, 0, 0.2, 1),
    stroke-dashoffset 250ms cubic-bezier(0.4, 0, 0.2, 1);
}
.line1 {
  stroke-dasharray: 60 207;
  stroke-width: 8;
}
.line2 {
  stroke-dasharray: 60 60;
  stroke-width: 8;
}
.line3 {
  stroke-dasharray: 60 207;
  stroke-width: 8;
}
.opened .line1 {
  stroke-dasharray: 90 207;
  stroke-dashoffset: -134;
  stroke-width: 8;
}
.opened .line2 {
  stroke-dasharray: 1 90;
  stroke-dashoffset: -90;
  stroke-width: 8;
}
.opened .line3 {
  stroke-dasharray: 90 207;
  stroke-dashoffset: -134;
  stroke-width: 8;
}
button {
  outline: none !important;
}

svg {
  height: 40px;
  width: 40px;
}

.side-nav {
  width: 100vw;
  height:100vh;
  margin-left: -40px;
  position: absolute;
  z-index: 40000;
background: rgba(238, 242, 245, 1);
  display: flex;
  justify-content: center;
  align-items: center;
  transition: 0.3s ease-in-out;
  font-family: Open sans, sans-serif;
}
.side-nav ul {
  margin: 0;
  padding: 0;
}
.side-nav li {
  list-style: none;
  text-decoration: none;
  padding: 20px 0px !important;
  transition: 0.3s ease-out;
  margin: auto;
}

.side-nav a {
  text-decoration: none !important;
  color: rgb(0, 0, 0);
  z-index: 50;
  font-size: 26px;
}

.side-nav li:hover {
  transform: scale(1.2);
  transition: 0.3s ease-out;
    text-decoration: none;

}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}  
@media (min-width: 993px) {

}

@media (max-width: 768px) {
   .nav-items {
    display: none;
  }
 
}


</style>
