<template>
    <nav>
      <ul>
        <li><router-link to="/" class="nav-link">Beranda</router-link></li>
        <li><router-link to="/rental" class="nav-link">Rental Mobil</router-link></li>
        
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navbar'
  }
  </script>
  
  <style scoped>
  nav {
    background-color: #007bff;
    padding: 10px 0; 
    border-bottom: 2px solid #0056b3; 
  }
  
  ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex; 
    justify-content: center; 
  }
  
  .nav-link {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
    border-radius: 5px;
  }
  
  .nav-link:hover {
    background-color: #0056b3; 
  }
  </style>
  