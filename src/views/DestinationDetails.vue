<template>
   <sectiom class="destination">
       <h1>{{destination.name}}</h1>
       <div class="destination-details">
           <img 
           :src="require(`@/assets/${destination.image}`)" 
           :alt="destination.name"
           :title="destination.name">
           <p>{{destination.description}}</p>
       </div>
   </sectiom>
</template>

<script>
import store from "@/store.js";
export default {
    data(){
        return{
            destinationId: this.$route.params.id,
            destinations: store.destinations
        }
    },
    computed:{
        destination(){

            return this.destinations.find(
                destination => destination.id === this.destinationId
            )
        }
    }
}
</script>

<style scoped>

img{
    max-width: 600px;
    height: auto;
    width: 100%;
    max-height: 400px;
}

.destination-details{
    display: flex;
    justify-content: space-between;
}

p{
    margin: 0 40px;
    font-size: 20px;
    text-align: left;
}

</style>