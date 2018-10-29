<template>
<div>
  <div class="home">
      <!-- <img src="img/consultations8.jpeg" alt=""> -->
      <h1 id="logo">Build&Brand <span id="sublogo"><br> Group</span></h1>     
  <div class="services">
        <ul class="service-items">
            <li id="service-item">Consultation</li>
            <li id="service-item">Investments</li>
            <li id="service-item">Insuarance</li>
            <li id="service-item">Swot analysis</li>

        </ul>
    </div>

    <div class="request-service">
        <div id="consultation">THE swot analysis</div>
        <div class="service-categories">
            <ul class="category-items">
                <li id="category-item">Seek Service</li>
                <li id="category-item">learn more</li>
                <li id="category-item">previous clients</li>
            </ul>
        </div>
    </div>
  </div>
      <div class="menu-btn" v-on:click="toggleMenu">
        <div class="btn-line"></div>
        <div class="btn-line"></div>
        <div class="btn-line"></div>
      </div>
      <div class="side-wrapper">
          <ul id="side-wrapper-item">
              <div class="btn-close" v-on:click="toggleMenu">
                  <div class="btn-line-close"></div>
                  <div class="btn-line-close"></div>
                  <div class="btn-line-close"></div>
              </div>
              <li><a>Home</a></li>
              <hr>
              <li><a>About</a></li>
              <hr>
              <li><a>News</a></li>
              <hr>
              <li><a>Our Services</a></li>
              <hr>
              <li><a>Clients</a></li>
              <hr>
              <li><a>Support</a></li>
              <hr>
              <li><a>Our Team</a></li>
              <hr>
              <li><a>Contact Us</a></li>
              <hr>
              <li><a>Promotions</a></li>
              <hr>
          </ul>
      </div>
      </div>
</template>

<script>
export default {
  name: "home",
  data(){
    const menuBtn = document.querySelector('.menu-btn');
    const closeBtn = document.querySelector('.btn-close');
    const sideWrapper = document.querySelector('.side-wrapper');
    return{
      showMenu: false
    }
  },
  methods: {
      toggleMenu(){
        if(!showMenu){
          sideWrapper.classList.add('open');
          menuBtn.classList.add('activate');
          closeBtn.classList.add('show-cross');
          closeBtn.classList.add('activate');

          //set Menu state
          showMenu = true;
        } else {
          sideWrapper.classList.remove('open');
          menuBtn.classList.remove('activate');
          closeBtn.classList.remove('show-cross');
          closeBtn.classList.remove('activate');

          //set Menu state
          showMenu = false;
        }
}

  }
};
</script>

<style src="../assets/css/style.css">

</style>
