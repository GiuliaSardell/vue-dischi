<template>
  <div class="col-2">
    <div class="container-img">
      <img :src="character.poster" :alt="character.title">
    </div>
    
    <h6>{{character.title}}</h6>
    <span>{{character.author}}</span>
    <span>{{character.year}}</span>
  </div>
</template>

<script>

export default {
  name: 'Characters',
  props:{
    character: Object
  }
  }
  

</script>

<style lang="scss">

@import '../assets/style/generals.scss';
@import '../assets/style/vars.scss';

.col-2{
  width: 15% !important;
  cursor: pointer;
  margin: 10px 20px 40px 20px;
  padding: 10px 0;
  background-color: lighten($primary-color, 5%);
  &:hover{
    background-color: lighten($primary-color, 15%);
    transition: all 0.3s;
  }
  .container-img{
    // height: 100%;
    width: 100%;
  }
  img{
    width: 100%;
    height: 100%;
    // &:hover{
    //   filter: brightness(1);
    // }
  }
  h6{
    margin: 10px 0;
    text-transform: uppercase;
    color: white;
    font-weight: bold;
    font-size: 14px;
    text-align: center;
  }
  span{
    display: block;
    text-align: center;
    color: lighten($primary-color, 30%);
  }
}

</style>