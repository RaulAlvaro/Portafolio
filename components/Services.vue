<template>
    <div 
      class="uk-flex uk-flex-column uk-flex-middle uk-flex-center uk-padding-large"
      style="background-color:#eeeeee">
      <h2 style="font-weight:bold">Servicios</h2>

      <!-- Slider mobile -->
      <div 
        class="uk-hidden@s"
        uk-slider="center:true">
        <div class="uk-position-relative uk-visible-toggle uk-padding" tabindex="-1" style="width:15em;">
          <ul class="uk-slider-items uk-child-width-1-1 uk-grid" style="width:15em;">
            <li
              style="width:20em;"
              v-for="(service, i) in servicios"
              :key="i">
              <div 
                class="uk-card uk-card-default"
                style="border-radius:10px;">
                <div 
                  class="uk-card-media-top uk-text-center uk-padding"
                  style="padding-bottom:0em;">
                  <img :src="service.img" alt="">
                </div>
                <div class="uk-card-body uk-text-center">
                  <h3 
                    class="uk-card-title uk-text-center service-title-size"
                    style="font-weight:bold">{{service.title}}</h3>
                  <hr>
                  <p class="uk-text-center service-description-size">{{ service.description }}</p>
                  <button class="btn-services-style btn-services-size">SOLICITAR</button>
                </div>
              </div>
            </li>
          </ul>
          <a class="uk-position-center-left uk-position-small uk-hidden-hover" href="#" uk-slidenav-previous uk-slider-item="previous"></a>
          <a class="uk-position-center-right uk-position-small uk-hidden-hover" href="#" uk-slidenav-next uk-slider-item="next"></a>          
        </div>
        <ul class="uk-slider-nav uk-dotnav uk-flex-center uk-margin"></ul>
      </div>

      <!-- Vista Desktop -->
      <div 
        class="uk-child-width-1-3@m uk-flex uk-flex-wrap uk-padding@s uk-visible@s"
        style="padding-top:0em;">
        <div
          class="uk-padding-small"
          v-for="(service, i) in servicios"
          :key="i">
          <div 
            class="uk-card uk-card-default uk-position-relative background-card uk-animation-toggle"
            style="border-radius:10px; cursor:pointer;">
            <div 
              class="uk-card-media-top uk-text-center uk-padding"
              style="padding-bottom:0em;">
              <img 
                class="uk-animation-stroke uk-preserve svg-color"  width="200" height="200" :src="service.img" alt="" uk-svg="stroke-animation: true">
            </div>          
            <div class="uk-card-body uk-text-center container-text">
              <h3 
                class="uk-card-title uk-text-center service-title-size"
                style="font-weight:bold;">{{service.title}}</h3>
              <hr class="line-color">
              <p class="uk-text-center service-description-size service-description-style">{{ service.description }}</p>
              <!-- <div class="uk-position-relative">
                <div class="uk-position-absolute btn-services-style btn-services-size"/>
                <div class="uk-position-absolute">SOLICITAR</div>
              </div> -->
              <button class="btn-services-style btn-services-size">SOLICITAR</button>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  data(){
    return {
      servicios: [
        { 
          title: 'Desarrollo Web',
          description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry',
          img:'/iconos/laptop.svg'
        },
        { 
          title: 'Creción de Apps',
          description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry',
          img:'/iconos/ui.svg'
        },
        { 
          title: 'Asesoria Digital',
          description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry',
          img:'/iconos/system.svg'
        }                        
      ],
      button: 'PROYECTOS',
      rip: ''
    }
  }
}
</script>

<style>
.background-card:hover{
  background-color: #fbdc00;
}

.background-card:hover .btn-services-style{
  background-color: black;
  color:white;
}


.background-card:hover .btn-services-size{
  animation: pulsecServiceB 1.5s infinite;
}

.background-card:hover .container-text .line-color{
  border: 0.5px solid black;
}

.background-card:hover .container-text .service-description-style{
  color:black;
}

.svg-color{
  fill: #fbdc00;
}

.btn-services-style{
  background-color:#fbdc00;
  font-weight: bold;
  cursor: pointer;
  border: none;
  text-decoration: none;  
}

@keyframes pulsecServiceY {
  0% {
    transform:scale(.9);
  }
  70% {
    transform:scale(1);
    box-shadow: 0 0 10px 10px rgba(251,220,0, 0.4);
  }
  100% {
    transform:scale(.9);
    box-shadow: 0 0 0 10px 10px rgba(251,220,0, 0.5);
  }
}  

@keyframes pulsecServiceB {
  0% {
    transform:scale(.9);
  }
  70% {
    transform:scale(1);
    box-shadow: 0 0 10px 10px rgba(0,0,0, 0.4);
  }
  100% {
    transform:scale(.9);
    box-shadow: 0 0 0 10px 10px rgba(0,0,0, 0.5);
  }
}  

@media (max-width: 640px) {
  .btn-services-size{
    font-size: 12px;
    border-radius: 10px;
    padding: 1em 2em;
    margin-top: 1em;
    animation: pulsecServiceY 1.5s infinite;
  }

  .service-title-size{
    font-size: 20px;
  }

  .service-description-size{
    font-size: 15px;
  }
}

@media (min-width: 641px) {
  .btn-services-size{
    font-size: 13px;
    border-radius: 10px;
    padding: 1em 2em;
    margin-top: 1em;
    animation: pulsecServiceY 1.5s infinite;
  }

  .service-title-size{
    font-size: 18px;
  }

  .service-description-size{
    font-size: 15px;
  }
}

@media (min-width: 960px) {
  .btn-services-size{
    font-size: 15px;
    border-radius: 10px;
    padding: 1em 2em;
    margin-top: 1em;
    animation: pulsecServiceY 1.5s infinite;
  }

  .service-title-size{
    font-size: 18px;
  }

  .service-description-size{
    font-size: 15px;
  } 
}

@media (min-width: 1200px) {
  .btn-services-size{
    font-size: 15px;
    border-radius: 10px;
    padding: 1em 2.5em;
    margin-top: 1em;
    animation: pulsecServiceY 1.5s infinite;
  }

  .service-title-size{
    font-size: 20px;
  }

  .service-description-size{
    font-size: 15px;
  }
}

@media (min-width: 1600px) {
  .btn-services-size{
    font-size: 18px;
    border-radius: 10px;
    padding: 1em 3em;
    margin-top: 1em;
    animation: pulsecServiceY 1.5s infinite;
  }

  .service-title-size{
    font-size: 23px;
  }

  .service-description-size{
    font-size: 16px;
  }
}
</style>
