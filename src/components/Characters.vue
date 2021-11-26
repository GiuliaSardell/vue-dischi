<template>
  <div class="col-2">
    <div class="container-img">
      <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
    </div>
    
    <h6>New Jersey</h6>
    <span>Bon Jovi</span>
    <span>anno</span>
  </div>
</template>

<script>

export default {
name: 'Characters'
}
</script>

<style lang="scss">

@import '../assets/style/generals.scss';
@import '../assets/style/vars.scss';

.col-2{
  cursor: pointer;
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