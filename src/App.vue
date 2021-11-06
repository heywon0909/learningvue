<template>
  <div>
  

  <Modal v-bind:원룸들="원룸들" :모달창열렸니="모달창열렸니" :누른거="누른거"></Modal>

  <div class="menu">
      <a v-for="(a,i) in 메뉴들" :key="i">{{a}}</a>
    </div>  

  <Discount></Discount>

  


  <Card :원룸들="원룸들"></Card>

  </div> 
</template>

<script>
import apple from './assets/data.js'
import Discount from './Discount.vue'
import Modal from './Modal.vue'
import Card from './Card.vue'
export default {
  name: 'App',
  data(){
    return {
      원룸들:apple,
      누름:0,
      products:['역삼동원룸','천호동원룸','마포구원룸'],
      메뉴들: ['Home','Products','About'],
      모달창: false,
    }
  },
  methods:{
    increase(i){
      this.신고수[i] += 1;
    }
  },
  components: {
    Discount,
    Modal,
    Card
  }
}
</script>

<style>
body{
  margin:0
}
div{
  box-sizing: border-box;
}
.black-bg{
  width: 100%; 
  height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed;
  padding: 20px;
}
.white-bg{
  width:100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}
.menu{
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color: white;
  padding: 10px;
}
.room-img{
  width:100%;
  margin-top:40px;
}
.discount{
  background: #eee;
  padding: 10px;
  margin: 10px;
  border-radius: 5px;
}
</style>
