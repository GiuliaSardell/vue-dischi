<template>
<div>

  <Select @changeValue="getChangeValue"/>

   <div class="row">


    <Character 
      v-for="character in filterCharacters"
      :key ="character.id"
      :character="character"
    />

    

    <!-- <div class="col-2">lista caratteri</div>
    <div class="col-2">lista caratteri</div>
    <div class="col-2">lista caratteri</div>
    <div class="col-2">lista caratteri</div>
    <div class="col-2">lista caratteri</div> -->
  </div>
</div>
 
</template>

<script>

import Character from './Characters.vue';
import Select from './Select.vue';
import axios from 'axios' //vue lo riconosce 

export default {
  name: 'CharactersList',
  components:{
    Character,
    Select
  },

  data(){
    return{
      characters: [],
      type: ''
    }
  },
  computed:{
    filterCharacters(){
      if(this.type === "Tutte le categorie"){
        return this.characters
      }
      return this.characters.filter(single => {
        return single.genre.includes(this.type)
      })
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
    },
    
    getChangeValue(value){
      console.log('value', value)
      
      this.type = value
      console.log('type', this.type)
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