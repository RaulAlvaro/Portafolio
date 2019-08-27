<template>
  <div class="uk-flex uk-flex-column uk-flex-middle uk-flex-center uk-position-relative">
    <div
    class="uk-position-absolute uk-width-1-1 uk-height-1-1"
    :style="'background-image:url(' + imageUrl + ');'"
    style="background-size:cover; ">
    </div>
    <div class="uk-position-relative gradientContact uk-width-1-1 uk-height-1-1">
      <h2 class="contactTitleStyle uk-padding-large">Contáctanos</h2>
      <div class="contactFormSize">
        <div class="uk-margin-medium">
          <input class="uk-input" type="text" placeholder="Nombre">
        </div>
        <div class="uk-margin-medium">
          <input class="uk-input" type="text" placeholder="Correo">
        </div>
        <div class="uk-margin-medium">
          <select class="uk-select">
            <option>Desarrollo Web</option>
            <option>Desarrollo Web</option>
            <option>Desarrollo Web</option>            
          </select>
        </div>
        <div class="uk-margin-medium">
          <textarea class="uk-textarea" rows="5" placeholder="Mensaje"></textarea>
        </div>
        <div class="uk-width-1-1 uk-text-center">
          <button class="btn-contact-style btn-contact-size">Ver Proyecto</button>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  data(){
    return {
      imageUrl: 'https://miro.medium.com/max/1838/0*10YYCc2FdnWFT87s'
    }
  }
}
</script>

<style>
  ::placeholder {
    color: #fbdc00 !important;
    font-weight: bold !important;
  }

  .contactTitleStyle{
    font-weight:bold; 
    color:#fbdc00; 
    margin-bottom:0px; 
    text-align:center;
  }

  .gradientContact {
    /* Permalink - use to edit and share this gradient: https://colorzilla.com/gradient-editor/#000000+0,000000+100&0.65+0,0.65+100;Neutral+Density */
    background: -moz-linear-gradient(top,  rgba(0,0,0,0.80) 0%, rgba(0,0,0,0.80) 100%); /* FF3.6-15 */
    background: -webkit-linear-gradient(top,  rgba(0,0,0,0.80) 0%,rgba(0,0,0,0.80) 100%); /* Chrome10-25,Safari5.1-6 */
    background: linear-gradient(to bottom,  rgba(0,0,0,0.80) 0%,rgba(0,0,0,0.80) 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#a6000000', endColorstr='#a6000000',GradientType=0 ); /* IE6-9 */
  }

  .btn-contact-style{
    background-color:#fbdc00;
    font-weight: bold;
    cursor: pointer;
  }

  .uk-input {
    border-radius: 10px;
    background-color: rgba(204,170,99,0.2);
  }

  .uk-select:not([multiple]):not([size]) {
    border-radius: 10px;
    background-color: rgba(204,170,99,0.2);
    color: #fbdc00 !important;
    font-weight: bold !important;      
  }

  .uk-textarea{
    border-radius: 10px;
    background-color: rgba(204,170,99,0.2);
  }

  .btn-contact-size{
    border: none;
    text-decoration: none;
  }

  @keyframes pulsecContacto {
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

  @media (max-width: 640px) {
    .contactFormSize{
      margin-left: 8vw;
      margin-right: 8vw;
    }

    .uk-input {
      height: 50px;
    }

    .uk-select:not([multiple]):not([size]) {
      height: 50px;   
    }

    .uk-textarea{
      max-height: 80px;
    }

    .btn-contact-size{
      font-size: 15px;
      border-radius: 10px;
      padding: 1em 1em;
      margin-bottom: 2em;
      animation: pulsecContacto 1.5s infinite;
    }     
  }

  @media (min-width: 641px) {
    .contactFormSize{
      margin-left: 10vw;
      margin-right: 10vw;
    }

    .uk-input {
      height: 50px;
    }

    .uk-select:not([multiple]):not([size]) {
      height: 50px;   
    }

    .uk-textarea{
      max-height: 150px;
    }

    .btn-contact-size{
      font-size: 15px;
      border-radius: 10px;
      padding: 1em 1em;
      margin-bottom: 2em;
      animation: pulsecContacto 1.5s infinite;
    }
  }

  @media (min-width: 960px) {
    .contactFormSize{
      margin-left: 17vw;
      margin-right: 17vw;
    }

    .uk-input {
      height: 50px;
    }

    .uk-select:not([multiple]):not([size]) {
      height: 50px;   
    }

    .uk-textarea{
      max-height: 150px;
    }

    .btn-contact-size{
      font-size: 15px;
      border-radius: 10px;
      padding: 1.5em 2.5em;
      margin-bottom: 2em;
      animation: pulsecContacto 1.5s infinite;
    }
  }

  @media (min-width: 1200px) {
    .contactFormSize{
      margin-left: 30vw;
      margin-right: 30vw;
    }

    .uk-input {
      height: 50px;
    }

    .uk-select:not([multiple]):not([size]) {
      height: 50px;   
    }

    .uk-textarea{
      max-height: 150px;
    }

    .btn-contact-size{
      font-size: 15px;
      border-radius: 10px;
      padding: 1.5em 2.5em;
      margin-bottom: 2em;
      animation: pulsecContacto 1.5s infinite;
    }    
  }

  @media (min-width: 1600px) {
    .contactFormSize{
      margin-left: 35vw;
      margin-right: 35vw;
    }

    .uk-input {
      height: 70px;
    }

    .uk-select:not([multiple]):not([size]) {
      height: 70px;   
    }

    .uk-textarea{
      max-height: 200px;
    }

    .btn-contact-size{
      font-size: 20px;
      border-radius: 10px;
      padding: 1em 2em;
      margin-bottom: 2em;
      animation: pulsecContacto 1.5s infinite;
    }    
  }

</style>
