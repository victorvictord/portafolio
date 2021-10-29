<template>
  
      <div class="card">
        <div class="card-body">
      <h4 class="card-title">{{name}}</h4>
      <br />
      <p class="card-text">
        {{description}}
      </p>
      <br />
      <p><strong>{{author}}</strong></p>
      <br>
      <button-url :url ="url" name="Github" />
      <br>
       <button-url color="red" :url="homepage" name="Deploy" v-if="homepage  != null" />
        </div>
    </div>
  
</template>

<script>
import ButtonUrl from "./ButtonUrl.vue"

export default {
  props:{
    name: String,
    description: String,
    author: String,
    url: String,
    homepage: String,
  },
  components:{
    ButtonUrl
  }
}
</script>

<style scoped>
.card {
    border: solid 1px #eee; 
    box-shadow: 1px 1px 4px #333;
    text-align: center;
    width: 250px;
    margin: 7px;
}
</style>