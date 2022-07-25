<script>
 export default {
  data(){
     return {
        selected: '',
        options : [
        { text: 'Напитки', value: 'Напитки' },
        { text: 'Первое', value: 'Первое ' },
        { text: 'Второе', value: 'Второе' },
        {text:'Закуски',value:'Закуски'},
        {text:'Десерт',value:' Десерт'}
        
        ]
      }
    }
 }

</script>

<template>
  <div id="cat">Выберите категорию: </div>
    
<div id="form">
 <select v-model="selected">
  <option v-for="option in options" :value="option.value">
    {{ option.text }}
  </option>
</select>
</div>

<div>

</div>

<div id="addForm"> 
  <input v-model="message" placeholder="Добавить позицию">

</div>

<div id="button">
    <button @click="next">Дальше</button>
    </div>

</template>

<style></style>