<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
    <div >
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/post">Post</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
header{
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: white;
}
a{
  margin-left: 10px;
  font-size: 30px;
  font-weight: 300;
}
</style>
