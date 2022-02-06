# 1.-Data-dan-Methods-Vue.js-

Vue.js memberikan kemudahan dalam menampilkan data secara dinamis.

Untuk lebih jelasnya silahkan ketikan kode berikut pada file “App.vue”:

<template>
  
  <h2>Name: {{ name }}</h2>
  
</template>
 
<script>
  
export default {
  
  name: "App",
  
  data() {
  
    return {
  
      name: "M Fikri",
  
    };
  
  },
  
};
  
</script>
 
<style>
  
</style>
