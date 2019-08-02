<template>
  <div class="">
    <div uk-slideshow="animation: slide">
      <div class="uk-position-relative uk-visible-toggle"> 
        <ul 
          class="uk-slideshow-items"
          uk-height-viewport="offset-top: true">
          <li 
            v-for="(item, key) in portrait"
            :key="key">
              <div :style="'background-image:url(' + item.img + ')'"
                class="uk-height-viewport uk-width-1-1 uk-position-absolute"
                style="background-repeat:no-repeat; background-size:cover;"/>
              <div 
                class="gradientPortrait uk-height-1-1 uk-width-1-1 uk-position-relative uk-flex uk-flex-column uk-flex-middle uk-flex-center">
                <span class="text-portrait-size text-portrait-style" v-html="item.title"/>
                <!-- <div style="background-color:#fbdc00">PROYECTOS</div> -->
                <button class="btn-portrait-style btn-portrait-size">PROYECTOS</button>
              </div>
          </li>
        </ul>
        <a class="uk-position-center-left uk-position-small uk-hidden-hover" href="#" uk-slidenav-previous uk-slideshow-item="previous"></a>
        <a class="uk-position-center-right uk-position-small uk-hidden-hover" href="#" uk-slidenav-next uk-slideshow-item="next"></a>
      </div>
      <div 
        class="uk-position-bottom-center uk-position-small"
        style="transform:translate(-5em, -5em)">
        <ul class="uk-slideshow-nav uk-dotnav uk-flex-center uk-margin dotnavPortrait"/>
      </div>
    </div>
  
  </div>
</template>

<script>
export default {
  data(){
    return {
      portrait: [
        { 
          title: 'El <b>arte</b> desafia a la <b>tecnología</b> y la <b>tecnología</b> inspira al <b>arte</b>',
          img:'https://static.videezy.com/system/resources/thumbnails/000/005/654/original/4k-stock-video-of-typing-on-laptop.jpg'
        },
        { 
          title: 'El arte desafia a la tecnología y la tecnología inspira al arte',
          img:'http://k43.kn3.net/5CDB0798E.jpg'
        },
        { 
          title: 'El arte desafia a la tecnología y la tecnología inspira al arte',
          img:'http://www.imagenesparafondo.com/wp-content/uploads/2013/08/Fondo-Super-Mario.jpg'
        }                
      ],
      button: 'PROYECTOS',
      rip: ''
    }
  }
}
</script>

<style>
.backcolor {
    background-color: cadetblue;
}

.backtest {
  background-color: red;
}

.dotnavPortrait > * > *{
  background-color: transparent;
  transform: scale(1.8);
  border: 1px solid #fbdc00;
  margin: 0em 1em
}

.dotnavPortrait > .uk-active > *{
  background-color: #fbdc00;
  -webkit-transform: scale(1.8);
}

.gradientPortrait {
  /* Permalink - use to edit and share this gradient: https://colorzilla.com/gradient-editor/#000000+0,000000+100&0.65+0,0.65+100;Neutral+Density */
  background: -moz-linear-gradient(top,  rgba(0,0,0,0.75) 0%, rgba(0,0,0,0.75) 100%); /* FF3.6-15 */
  background: -webkit-linear-gradient(top,  rgba(0,0,0,0.75) 0%,rgba(0,0,0,0.75) 100%); /* Chrome10-25,Safari5.1-6 */
  background: linear-gradient(to bottom,  rgba(0,0,0,0.75) 0%,rgba(0,0,0,0.75) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#a6000000', endColorstr='#a6000000',GradientType=0 ); /* IE6-9 */
}

.text-portrait-style{
  text-align: center;
  color:white;
  text-transform: uppercase;  
}

.btn-portrait-style{
  background-color:#fbdc00;
  font-weight: bold;
  cursor: pointer;
}

@media (max-width: 640px) {
  .text-portrait-size {
    font-size: 20px;
  }

  .text-portrait-style{
    margin-left: 3em;
    margin-right: 3em;
  }

  .btn-portrait-size{
    font-size: 14px;
    border: none;
    text-decoration: none;
    border-radius: 10px;
    padding: 1.5em 2em;
    margin-top: 5em;
  }  
}

@media (min-width: 641px) {
  .text-portrait-size {
    font-size: 25px;
  }

  .text-portrait-style{
    margin-left: 4.5em;
    margin-right: 4.5em;
  }

  .btn-portrait-size{
    font-size: 14px;
    border: none;
    text-decoration: none;
    border-radius: 10px;
    padding: 1em 2em;
    margin-top: 2em;
  }  
}

@media (min-width: 960px) {
  .text-portrait-size {
    font-size: 35px;
  }

  .text-portrait-style{
    margin-left: 4.5em;
    margin-right: 4.5em;
  }

  .btn-portrait-size{
    font-size: 18px;
    border: none;
    text-decoration: none;
    border-radius: 10px;
    padding: 1em 2em;
    margin-top: 2em;
  }
}

@media (min-width: 1200px) {
  .text-portrait-size {
    font-size: 40px;
  }

  .text-portrait-style{
    margin-left: 5.5em;
    margin-right: 5.5em;
  }

  .btn-portrait-size{
    font-size: 20px;
    border: none;
    text-decoration: none;
    border-radius: 10px;
    padding: 1em 2em;
    margin-top: 2em;
  }  
}

@media (min-width: 1600px) {
  .text-portrait-size {
    font-size: 50px;
  }

  .text-portrait-style{
    margin-left: 5.5em;
    margin-right: 5.5em;
  }

  .btn-portrait-size{
    font-size: 20px;
    border: none;
    text-decoration: none;
    border-radius: 10px;
    padding: 1em 2em;
    margin-top: 2em;
  }
}
</style>
