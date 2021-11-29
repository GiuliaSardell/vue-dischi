<template>
  <div class="main-wrapper">
    <Header />
    <!-- <Select @changeValue="getChangeValue()"
    /> -->
    <div class="container">

      <CharactersList />
    </div>
    
  </div>
</template>

<script>
import Header from './components/Header.vue';
// import Select from './components/Select.vue';
import CharactersList from './components/CharactersList.vue';


export default {
  name: 'App',
  components: {
    Header,
    CharactersList
  },
  
    
  
}
</script>

<style lang="scss">

@import './assets/style/generals.scss';
@import './assets/style/vars.scss';

.main-wrapper{
  min-height: 100vh;
  background-color: $primary-color; 
}

</style>
