<template>
  <header>
    <!-- Home Navigation Menu (Header) -->
    <nav class="navbar navbar-expand-lg fixed-top navbar-dark bg-white">
      <div class="container">
        <!-- Get-in-EXP LOGO -->
        <a href="#" >
          <img class="img-startHeader" src="img/logos/logo_Startheader.png" alt="startHeaderLogo">
        </a>

        <ul class="navbar-nav ml-5">
          <li class="nav-item"><router-link to="/home" class="nav-link">JOB OFFERTS</router-link></li>
          <li class="nav-item"><router-link to="/login" class="nav-link">SIGN IN</router-link></li>
          <li class="nav-item"><router-link to="/register" class="nav-link">SIGN UP</router-link></li>
        </ul>
      </div>
    </nav>
  </header>
</template>
<script>
import BaseNav from "@/components/BaseNav";
import CloseButton from "@/components/CloseButton";

export default {
  name: 'StarterHeader',
  components: {
    BaseNav,
    CloseButton
  },

};
</script>
<style>
</style>
