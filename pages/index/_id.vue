<template lang="pug">
  div.right-side-container 
    div 
      h1 Selected user id is {{$route.params.id}}
</template>

<style scoped>
  .right-side-container{
    height: 100%; 
    display: flex; 
    flex-direction: row;
    align-items: center;
    justify-content: center;
  }
</style>