<template>
    <div>
  <div v-for="(count,i) in 원룸들" :key="i">
    <img :src="count.image" class="room-img">
    <h4>{{count.title}}</h4>
    <p>{{count.price}}</p>
  </div>
  </div>
</template>

<script>
export default {
    name: 'Card',
    props:{
        원룸들: Array,
    }
}
</script>

<style>

</style>