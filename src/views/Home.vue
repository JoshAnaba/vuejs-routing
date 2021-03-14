<template>
  <div class="home">
    <h1>Destinations</h1>
   <div class="destination">
      <div v-for="destination in destinations"
      :key="destination.id">
      <router-link 
      :to="{name: 'DestinationDetails', params: {id: destination.id}}">
      <h2>{{destination.name}}</h2>
      </router-link>
      <figure>
      <router-link 
      :to="{name: 'DestinationDetails', params: {id: destination.id}}">
          <img :src="require(`@/assets/${destination.image}`)" :alt="destination.name"
          :title="destination.name">
      </router-link>
      <div>
        {{destination.description}}
      </div>
    </figure>
    </div>
   </div>
  </div>
</template>

<script>
// @ is an alias to /src
import store from "@/store.js"

export default {
  name: "Home",
  components: {
  },
  data(){
    return {
      destinations: store.destinations
    }
  }
};
</script>

<style scoped>

.destination{
  display: flex;
}

img{
  max-width: 150px;
}
</style>
