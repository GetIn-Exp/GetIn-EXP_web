<template>
  <header>
    <!-- Home Navigation Menu (Header) -->
    <nav class="navbar navbar-expand-lg fixed-top navbar-dark bg-white">
      <div class="container">
        <!-- Get-in-EXP LOGO -->

        <a href="#" class="navbar-brand text-default">
          <h3>GETIN-EXP
          </h3>
        </a>

        <button
            type="button"
            data-toggle="collapse"
            data-target="navbar-danger"
            aria-controls="navbar-danger"
            aria-label="Toggle navigation"
            class="navbar-toggler"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div id="navbar-danger" class="collapse navbar-collapse">
          <div class="navbar-collapse-header">
            <div class="row">
              <div class="col-6 collapse-brand">
                <a href="./index.html">
                  <img src="img/brand/blue.png" />
                </a>
              </div>
              <div class="col-6 collapse-close">
                <button
                    type="button"
                    data-toggle="collapse"
                    data-target="#navbar-danger"
                    aria-controls="navbar-danger"
                    aria-label="Toggle navigation"
                    class="navbar-toggler"
                >
                  <span></span>
                  <span></span>
                </button>
              </div>
            </div>
          </div>

          <a href="#" class="navbar-brand"> Offerts </a>

          <ul class="navbar-nav ml-auto">
            <li class="nav-item">
              <a href="#" class="nav-link nav-link-icon"
              ><i class="fa fa-facebook-square"></i
              ><span class="nav-link-inner--text d-lg-none"
              >Facebook</span
              ></a
              >
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link nav-link-icon">
                <i class="fa fa-twitter"></i>
                <span class="nav-link-inner--text d-lg-none">Twitter</span>
              </a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link nav-link-icon">
                <i class="fa fa-google-plus"></i>
                <span class="nav-link-inner--text d-lg-none">Google +</span>
              </a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link nav-link-icon">
                <i class="fa fa-instagram"></i>
                <span class="nav-link-inner--text d-lg-none">
                    Instagram
                  </span>
              </a>
            </li>

            <li class="nav-item"><a href="#" class="nav-link">PROFILE</a></li>
            <li class="nav-item dropdown">
              <a
                  href="#"
                  id="nav-inner-primary_dropdown_1"
                  role="button"
                  data-toggle="dropdown"
                  aria-haspopup="true"
                  aria-expanded="false"
                  class="nav-link"
              >LOG IN</a
              >

              <div
                  aria-labelledby="nav-inner-primary_dropdown_1"
                  class="dropdown-menu dropdown-menu-right"
              >
                <a href="#" class="dropdown-item">Action</a
                ><a href="#" class="dropdown-item">Another action</a>
                <div class="dropdown-divider"></div>
                <a href="#" class="dropdown-item">Something else here</a>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>
<script>
import BaseNav from "@/components/BaseNav";
import CloseButton from "@/components/CloseButton";

export default {
  components: {
    BaseNav,
    CloseButton
  }
};
</script>
<style>
</style>
