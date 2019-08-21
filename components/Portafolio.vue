<template>
  <div 
    class="uk-flex uk-flex-column uk-flex-middle uk-flex-center uk-padding-large"
    style="background-color:black">
    <h2 style="font-weight:bold; color:#fbdc00; margin-bottom:0px;">Portafolio</h2>
    <div
      class="uk-padding-small subtitlePortafolioStyle"
      style="color:white; text-align:center;">{{ description }}</div>
    <div >
      <div class="uk-child-width-1-1 uk-child-width-1-2@s uk-child-width-1-3@m uk-grid uk-margin-remove">
        <!-- <div
          v-for="(item, key) in projects"
          :key="key"
          :style="'background-image:url(' + item.imageUrl + ')'"
          style="height:300px; width:300px"
          class="uk-padding-remove">
          <img src="" alt="">
        </div> -->
        <div
          v-for="(item, key) in projects"
          :key="key"
          class="uk-padding-remove"
          style="cursor:pointer; border: 1px solid black;">
          <img :src="item.imageUrl">
        </div>        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took',
      projects: [
        {
          title: 'Proyecto 1',
          description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.',
          imageUrl: 'https://static.vix.com/es/sites/default/files/styles/large/public/btg/formas_en_que_las_personas_positivas_se_alejan_de_la_mala_energia.jpg'
        },
        {
          title: 'Proyecto 2',
          description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.',
          imageUrl: 'https://www.freejpg.com.ar/asset/900/57/57fe/F100006678.jpg'
        },
        {
          title: 'Proyecto 3',
          description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.',
          imageUrl: 'https://st2.depositphotos.com/1017228/12008/i/950/depositphotos_120084806-stock-photo-happy-business-people-using-laptop.jpg'
        },
        {
          title: 'Proyecto 4',
          description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.',
          imageUrl: 'https://emeduc.org/wordpressSite/wp-content/uploads/2017/05/art%C3%ADculo-25-05.jpg'
        },
        {
          title: 'Proyecto 5',
          description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.',
          imageUrl: 'https://image.freepik.com/foto-gratis/personas-manos-trabajando-usando-laptop-mesa-blanca_53876-50327.jpg'
        },
        {
          title: 'Proyecto 6',
          description: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.',
          imageUrl: 'https://laopinionla.files.wordpress.com/2019/02/shutterstock_349413722.jpg?quality=80&strip=all&w=940'
        }                                        
      ]
    }
  }
}
</script>

<style>
@media (max-width: 640px) {
  .subtitlePortafolioStyle{
    margin-left: 2vw;
    margin-right: 2vw;
    font-size: 14px;
  }  
}

@media (min-width: 641px) {
  .subtitlePortafolioStyle{
    margin-left: 10vw;
    margin-right: 10vw;
    font-size: 16px;
  }
}

@media (min-width: 960px) {
  .subtitlePortafolioStyle{
    margin-left: 15vw;
    margin-right: 15vw;
    font-size: 16px;
  }
}

@media (min-width: 1200px) {
  .subtitlePortafolioStyle{
    margin-left: 20vw;
    margin-right: 20vw;
    font-size: 17px;
  }
}

@media (min-width: 1600px) {
  .subtitlePortafolioStyle{
    margin-left: 25vw;
    margin-right: 25vw;
    font-size: 17px;
  }
}
</style>
