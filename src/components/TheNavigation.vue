<template>
     <nav id="nav">
   <ul class="nav-links"></ul>
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