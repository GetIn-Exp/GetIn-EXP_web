<template>
  <div>
    <header>
      <!-- Home Navigation Menu (Header) -->
      <nav class="navbar navbar-expand-lg navbar-dark bg-danger">
        <div class="container">
          <!-- Get-in-EXP LOGO -->

          <a href="#" class="navbar-brand"> GETIN-EXP </a>

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

    <body>
      <div class="container pt-lg-md">
        <div class="row justify-content-center">


          <!-- First Column: search parameters and filters -->
          <div class="col-lg-4">
            <card
              id="home-card-search"
              shadow
              header-classes="bg-pb-5"
              body-classes="px-lg-1 py-lg-1"
              class="border-0 myred roundered mb-5"
            >
              <div class="card-body pb-0">
                <div id="home-form-search" class="form-group">
                  <!---->
                  <div id="home-form-search-what" class="input-group mb-2">
                    <!----><!---->
                    <input
                      aria-describedby="addon-right addon-left"
                      placeholder="QUÉ"
                      class="form-control"
                    />
                    <div class="input-group-append">
                      <span class="input-group-text"
                        ><i class="ni ni-zoom-split-in"></i
                      ></span>
                    </div>
                    <!---->
                  </div>

                  <div id="home-form-search-where" class="input-group mb-2">
                    <!----><!---->
                    <input
                      aria-describedby="addon-right addon-left"
                      placeholder="DÓNDE"
                      class="form-control"
                    />
                    <div class="input-group-append">
                      <span class="input-group-text"
                        ><i class="ni ni-pin-3"></i
                      ></span>
                    </div>
                    <!---->
                  </div>
                </div>

                <div id="home-form-filter" class="form-group">
                  <button
                    id="home-form-btn"
                    type="button"
                    class="btn btn-icon btn-style"
                  >
                    <!----><!----><!---->
                    <span class="btn-inner--icon"
                      ><i class="ni ni-settings-gear-65"></i
                    ></span>
                    Advanced filters
                  </button>
                  
                  <div
                    id="home-form-datepicker"
                    class="input-group input-daterange datepicker"
                  >
                    <base-input
                      name="calendar"
                      addon-left-icon="ni ni-calendar-grid-58"
                      label="Antes de"
                      labelClasses="input-group-text label-style text-uppercase"
                    >
                      <flat-picker
                        slot-scope="{ focus, blur }"
                        @on-open="focus"
                        @on-close="blur"
                        :config="{ allowInput: true }"
                        class="form-control datepicker"
                        v-model="dates.simple"
                      >
                      </flat-picker>
                    </base-input>

                    <div id="home-form-dropdown" class="input-group">
                      <text-dropdown/>
                    </div>
                  </div>
                </div>
              </div>
            
            </card>
          </div>
          

          <!--_Second Column: offerts list -->
          <div class="col-lg-8">
            <div id="offerts-panel" class="text-center text-muted mb-4">
              PANEL DE OFERTAS
            </div>
          </div>
        </div>
      </div>
    </body>
  </div>
</template>

<script>
import flatPicker from "vue-flatpickr-component"
import TextDropdown from "./components/TextDropdown";

import Hero from "./components/Hero";
import AppHeader from "../layout/AppHeader";
import AppFooter from "../layout/AppFooter";

import BasicElements from "./components/BasicElements";
import Inputs from "./components/Inputs";
import CustomControls from "./components/CustomControls";
import Navigation from "./components/Navigation";
import JavascriptComponents from "./components/JavascriptComponents";
import Carousel from "./components/Carousel";
import Icons from "./components/Icons";
import Examples from "./components/Examples";
import DownloadSection from "./components/DownloadSection";
import DatePickers from "./components/JavascriptComponents/DatePickers.vue";

export default {
  name: "home",
  components: {
    flatPicker,
    TextDropdown
  },

  data() {
    return {
      dates: {
        simple: "2018-07-17",
      },
    };
  },
};
</script>

<!-- Can't be scoped if we pretend to export label-style outside -->
<style>
.roundered {
  border-radius: 1.5rem;
}

.myred {
  background-color: #f5365c !important;
}

.btn-style {
  width: 100%;
  border: 2px solid black;
  color: white;
  background-color: #f5365c;
}

.label-style {
  font-size: 0.9rem;
  font-weight: 500;
  line-height: 1.5;
  color: #adb5bd;
  background-color: #fff;
  border: 1px solid #cad1d7;
  border-radius: 0.25rem;
}

.dropdown-categories{
    position: absolute;
    top: 100%;
    right: 100% !important;
    float: left;
    background-color: inherit;
    background-clip: padding-box;
}

/* Not used */
.form-btn-container {
  position: relative;
  margin-top: 30px;
  margin-bottom: 30px;
  margin-left: 20px;
  margin-right: 20px;
}

.form-btn-container .form-btn {
  position: absolute; /* The position also affects the behaviour of the transparency */
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 1;
  color: white;
  background-color: #f5365c;
  border-color: black;
}

/* Same pattern as A) to move the child .bg-text relatively to its father */
.main-title h2 {
  position: relative;
  text-transform: uppercase; /* Initialy, Text to uppercase */
  font-size: 4rem;
  font-weight: 700;
}

.main-title h2 span {
  color: var(--color-secondary);
}

.main-title h2 .bg-text {
  position: absolute; /* The position also affects the behaviour of the transparency */
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: var(--color-grey-5); /* Color superposition! As transparent */
  transition: all 0.4s ease-in-out;
  z-index: -11;
  font-weight: 800;
  font-size: 6.3rem;
}

.form-hr {
  display: block;
  position: relative;
  padding: 0;
  margin: 8px auto;
  height: 0;
  width: 100%;
  max-height: 0;
  font-size: 1px;
  line-height: 0;
  clear: both;
  border: none;
  border-top: 1px solid #adb5bd;
  border-bottom: 1px solid #adb5bd;
}
</style>