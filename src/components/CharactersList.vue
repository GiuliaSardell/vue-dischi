<template>
  <div class="row">
    <Character />
    <Character />
    <Character />
    <Character />
    <Character />

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
      character: []
    }
  },
  methods:{
    getApi(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then( r => {
        // console.log('r',r);
        this.character = r.data;
        console.log('characters',this.character)
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