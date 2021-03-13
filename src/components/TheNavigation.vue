<template>
     <nav id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/Brazil">Brazil</router-link> |
      <router-link to="/Panama">Panama</router-link> |
      <router-link to="/Jamaica">Jamaica</router-link> |
      <router-link to="/Hawaii">Hawaii</router-link>
    </nav>
</template>
<style scoped>

#nav{
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 0 10px;
}

#nav a.active-class {
  color: #42b983;
}
</style>