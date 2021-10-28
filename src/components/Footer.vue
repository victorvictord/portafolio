<template>
 <div id="footer">
    <footer>
        <h3>
        &copy; Victor Victor Dasilva Lopez - {{year }}
        </h3>
    </footer>
  </div>
</template>

<script>
export default {
    computed:{
        year(){
            return new Date().getFullYear()
        }
    }
}
</script>

<style scoped>
h3{
  background-color: #333;
  padding: 1rem;
  color: snow;
  text-align: center;
}
</style>