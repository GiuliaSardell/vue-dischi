<template>
  <div class="row">
    <Character 
      v-for="character in characters"
      :key ="character.id"
      :character="character"
    />
 

    <!-- <div class="col-2">lista caratteri</div>
    <div class="col-2">lista caratteri</div>
    <div class="col-2">lista caratteri</div>
    <div class="col-2">lista caratteri</div>
    <div class="col-2">lista caratteri</div> -->
  </div>
</template>

<script>

import Character from './Characters.vue';
import axios from 'axios' //vue lo riconosce 

export default {
  name: 'CharactersList',
  components:{
    Character,
  },
  data(){
    return{
      characters: []
    }
  },
  methods:{
    getApi(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then( r => {
        // console.log('r',r);
        this.characters = r.data.response;
        console.log('r',r)
        console.log('characters',this.characters)
      })
      .catch( e => {
        console.log('e',e);
      })
    }
  },
  mounted(){
    console.log(axios)
    this.getApi();
  }

}
</script>

<style lang="scss">
.row{
  justify-content: center;
}

</style>