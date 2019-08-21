<template>
  <div 
    class="uk-flex uk-flex-column uk-flex-middle uk-flex-center uk-padding-large"
    style="background-color:#eeeeee">
    <h2 style="font-weight:bold">Sobre Mi</h2>
    <div 
      class="uk-padding contentAboutMeSize"
      style="text-align:center">{{ aboutMe.content }}</div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      aboutMe:{
        content: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industrys standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.'
      }
    }
  }
}
</script>

<style>
@media (max-width: 640px) {
  .contentAboutMeSize{
    margin-left: 1em;
    margin-right: 1em;
    padding: 0em 0em;
    font-size: 14px;
  }  
}

@media (min-width: 641px) {
  .contentAboutMeSize{
    margin-left: 5em;
    margin-right: 5em;
    font-size: 16px;
  }
}

@media (min-width: 960px) {
  .contentAboutMeSize{
    margin-left: 12em;
    margin-right: 12em;
    font-size: 16px;
  }
}

@media (min-width: 1200px) {
  .contentAboutMeSize{
    margin-left: 12em;
    margin-right: 12em;
    font-size: 17px;
  }
}

@media (min-width: 1600px) {
  .contentAboutMeSize{
    margin-left: 20em;
    margin-right: 20em;
    font-size: 18px;
  }
}
</style>
