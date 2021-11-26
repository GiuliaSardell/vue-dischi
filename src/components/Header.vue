<template>
  <header>
    <div class="container-logo">
      <img src="https://www.ore25.it/wp-content/uploads/2020/01/file-spotify-logo-png-4.png" alt="">
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss">
@import '../assets/style/generals.scss';
@import '../assets/style/vars.scss';

header{
  // height: 80px;
  background-color: lighten($primary-color, 10%);
  padding: 10px;
  margin-bottom: 40px;

  .container-logo{
    width: 50px;
    height: 50px;


    img{
      height: 100%;
      width: 100%;
      
    }
  }
}

</style>