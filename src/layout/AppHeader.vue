<template>
  <header>
    <!-- Home Navigation Menu (Header) -->
    <nav class="navbar navbar-expand-lg fixed-top navbar-dark bg-default">
      <div class="container">
        <!-- Get-in-EXP LOGO -->
        <router-link to="/home">
          <img class="img-startHeader" src="img/logos/logo_AppHeader.png" alt="startHeaderLogo">
        </router-link>

        <ul v-if="logged" class="navbar-nav ml-5">
          <li class="nav-item"><router-link to="/home" class="nav-link">JOB OFFERTS</router-link></li>
          <li class="nav-item"><router-link to="/profile" class="nav-link">PROFILE</router-link></li>
          <li class="nav-item"><router-link to="/" class="nav-link" @click="logOut()">LOG OUT</router-link></li>
        </ul>
        <ul v-else class="navbar-nav ml-5">
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
import BaseDropdown from "@/components/BaseDropdown";
import CloseButton from "@/components/CloseButton";

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown
  },
  data () {
    return {
      logged: false,
      token: 0,
    }
  },
  beforeMount() {
    if (localStorage.getItem('logged')) {
      try {
        this.logged = (localStorage.logged === 'true');
        this.token = parseInt(JSON.parse(localStorage.getItem('token')));
      } catch(error) {
        this.logged = false;
        this.token = 0;
      }
    }
  },
  methods: {
    logOut () {
      localStorage.logged = false;
      localStorage.token = 0;
    }
  }
};
</script>
<style>
</style>
