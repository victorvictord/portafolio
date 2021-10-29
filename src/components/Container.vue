<template>
    <div id="container" class="container">
         <h2>Proyectos</h2>
         <img
          src="https://avatars.githubusercontent.com/u/5412050?v=4"
          alt="Victor Victor"
          width="58"
          loading="Lazy"
          class="image"
         />
        <hr />
        <loading v-if="load" />
        <div id="cards" v-for="proyect in proyects" :key="proyect.id" >
       
        <Card 
            :name="proyect.name" 
            :description="proyect.description" 
            :author="proyect.owner.login" 
            :url="proyect.html_url"
            :homepage="proyect.homepage"
             />
        </div>
    </div>
</template>
<script>
import Card from "./Card.vue";
import Loading from "./Loading.vue"

export default {
    data(){
        return {
            proyects: null,
            load: false,
        }
    },
    components: {
        Card,
        Loading,
    },
    mounted(){
        this.getProjects();
    },
    methods:{
        async getProjects(){
            this.load = true;
            const res = await fetch("https://api.github.com/users/victorvictord/repos");
            const data = await res.json();
            this.proyects = data;
            this.load = false;
            console.log(this.proyects);
        }
    }
}
</script>
<style scoped>
.image{
    border-radius: 50%;
}
#cards {
    display: flex;
    flex-wrap: wrap;

}
/*
.container {
    margin: 1rem;
    border: solid 1px #eee; 
    padding: 7px;
    box-shadow: 1px 1px 4px #333;
    text-align: center;
}
*/

</style>