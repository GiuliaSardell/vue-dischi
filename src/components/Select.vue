<template>
  <select class="form-select my-5"
  v-model="type"
  @change="$emit('changeValue', type)"
  >
  <!-- <option selected>Open this select menu</option> -->
  <option value="Tutte le categorie">Tutte le categorie</option>
  <option value="Rock">Rock</option>
  <option value="Pop">Pop</option>
  <option value="Jazz">Jazz</option>
  <option value="Metal">Metal</option>
</select>
</template>

<script>
export default {
  name: 'Select',
  data(){
    return{
      type: 'Tutte le categorie'
    }
  }
  
  
}
</script>

<style lang="scss">

.form-select{
  width: 300px  !important;
  margin: 0 auto;
  display: block;

}

</style>