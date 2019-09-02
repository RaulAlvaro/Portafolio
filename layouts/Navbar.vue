<template>
  <div>
    <div 
      class="uk-position-relative uk-visible@m"
      style="z-index:1">
      <div uk-sticky="animation: uk-animation-slide-top; sel-target: .uk-navbar-container; cls-active: uk-navbar-sticky container-navbar; cls-inactive: uk-position-absolute uk-navbar-transparent uk-light; top: 800">
        <nav class="uk-navbar-container uk-width-1-1" uk-navbar>
          <div 
            class="uk-navbar-right"
            style="padding-top:0.5em;">
            <ul
              class="uk-navbar-nav"
              v-for="(item, key) in sections"
              :key="key">
              <li 
                class="menu-item"
                style="padding-left:2vw; padding-right:2vw">
                <a
                  class="font-size-titlenavbar"
                  style="font-weight:bold"
                  @click="goToSection(item.title)">{{ item.title }}</a>
              </li>
            </ul>
          </div>
          <div
            class="uk-navbar-right uk-hidden@m">
            <a
              class="uk-navbar-toggle"
              uk-navbar-toggle-icon
              uk-toggle="target: #offcanvas-nav-primary"
              href="#offcanvas-nav-primary"/>
          </div>
        </nav>
      </div>
    </div>
  </div>


</template>

<script>
var UIkit

if (process.browser) {
  UIkit = require('uikit')
}

export default {
  data(){
    return {
      sections:[
        { title: 'HOME' },
        { title: 'SERVICIOS' },
        { title: 'PORTAFOLIO' },
        { title: 'SOBRE MI' },
        { title: 'CONTACTO' },
      ]
    }
  },
  methods:{
    async goToSection(url){
      // await wait(2000)
      // UIkit.offcanvas('#offcanvas-nav-primary').hide().then(() => {
        //Validate screeen size
        UIkit.scroll({offset: 120})
        // this.$router.push('#'+ slugify(url))
        console.log(url);
        this.$router.push('#'+url)
      // })
    },    
  }
}

function wait (n) {
 return new Promise(function (resolve, reject) {
   setTimeout(() => {
     resolve()
   }, n)
 })
}


</script>

<style>
  .menu-item:hover a{
    color: #fbdc00 !important;
  }

  .container-navbar {
    background-color: rgba(0, 0, 0, 0.9) !important;
  }

  @media (max-width: 640px){
    
  }

  @media (min-width: 641px){
    
  }

  @media (min-width: 960px){
    .font-size-titlenavbar{
      font-size: 14px !important;
    }
  }

  @media (min-width: 1200px){
    .font-size-titlenavbar{
      font-size: 16px !important;
    }    
  }

  @media (min-width: 1600px){
    .font-size-titlenavbar{
      font-size: 17px !important;
    }    
  }

</style>
