<template>
  <header>
    <!-- Home Navigation Menu (Header) -->
    <nav class="navbar navbar-expand-lg fixed-top navbar-dark bg-default">
      <div class="container">
        <!-- Get-in-EXP LOGO -->
        <a href="#" >
          <img class="img-startHeader" src="img/logos/logo_AppHeader.png" alt="startHeaderLogo">
        </a>

        <ul class="navbar-nav ml-5">
          <li class="nav-item"><router-link to="/home" class="nav-link">JOB OFFERTS</router-link></li>
          <li class="nav-item"><router-link to="/profile" class="nav-link">PROFILE</router-link></li>
          <li class="nav-item"><router-link to="/login" class="nav-link">SIGN IN</router-link></li>
          <li class="nav-item"><router-link to="/register" class="nav-link">SIGN UP</router-link></li>
        </ul>
        <!-- TODO PARA EL REFACTOR
        <ul class="navbar-nav ml-5">
          <li class="nav-item"><router-link to="/home" class="nav-link">JOB OFFERTS</router-link></li>
          <li class="nav-item"><router-link class="nav-link">LOG OUT</router-link></li>
          <li class="nav-item"><router-link to="/profile" class="nav-link">PROFILE</router-link></li>
        </ul>
        -->

      </div>
    </nav>
  </header>
</template>
<script>
import BaseNav from "@/components/BaseNav";
import BaseDropdown from "@/components/BaseDropdown";
import CloseButton from "@/components/CloseButton";

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown
  }
};
</script>
<style>
</style>
