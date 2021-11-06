<template>
  <div v-if="모달창 == true" class="black-bg">
    <div class="white-bg">
    <Discount/>
    <img :src="원룸들[누름].image" style="width:100%;">
    <h4>{{원룸들[누름].title}}</h4>
    <p>{{원룸들[누름].price}}</p>
    <p>{{원룸들[누름].content}}</p>
    <button @click="모달창=false">닫기</button>
    </div>
  </div>  
</template>

<script>
export default {
    name:'Modal',
    props:{
        원룸들: Array,
        누른거:Number,
        모달창열렸니:Boolean,
    }
}
</script>

<style>

</style>

