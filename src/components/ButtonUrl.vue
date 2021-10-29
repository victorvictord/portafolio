<template>
    <a :href="url" :class="setColor" target="_blank">{{name}}</a>
</template>
<script>
export default {
   props:{
       color: String,
       url: String,
       name: String
   },
   computed: {
       setColor(){
           return this.color ==='red' ? 'btn btn-danger' : 'btn btn-primary'

       }
   }
}
</script>