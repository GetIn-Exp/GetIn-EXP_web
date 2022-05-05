<template>
  <div>
    <header>
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
          <div class="col-lg-4">
            <!-- primary refers to the color! secondary also available -->
            <card
              id="home-card-search"
              type="primary"
              shadow
              header-classes="bg-pb-5"
              body-classes="px-lg-1 py-lg-1"
              class="border-0 myred roundered"
            >
              <div class="card-body">
                <div id="home-form-search" class="input-group">
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

                  <div id="home-form-search-where" class="input-group">
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
              </div>
            </card>

            <br /><br />

            <card
              id="offerts-search-pannel"
              type="primary"
              shadow
              header-classes="pb-5"
              body-classes="px-lg-1 py-lg-1"
              class="border-0 myred roundered"
            >
              <div class="card-body row justify-content-center">
                <div class="h5 card-title text-white font-weight-bold mb-4">
                  Advanced Options
                </div>


                


                <div id="home-form-filter" class="input-group">
                  <!---->
                  
                  <div id="home-form-datepicker" class="input-group input-daterange datepicker row align-items-center">
                    <div class="col">
                        <base-input addon-left-icon="ni ni-calendar-grid-58">
                            <flat-picker slot-scope="{focus, blur}"
                                        @on-open="focus"
                                        @on-close="blur"
                                        :config="{allowInput: true, mode: 'range',}"
                                        class="form-control datepicker"
                                        v-model="dates.range">
                            </flat-picker>
                        </base-input>
                      </div>
                  </div>

                  <div id="home-form-filter-1" class="input-group mb-2">
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


                  <div id="home-form-filter-2" class="input-group">
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
              </div>
            </card>
          </div>

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
import flatPicker from "vue-flatpickr-component";

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
import DatePickers from './components/JavascriptComponents/DatePickers.vue';

export default {
  name: "home",
  components: {
    flatPicker
  },

  data() {
    return {
      dates: {
        simple: "2018-07-17",
        range: "2018-07-17 to 2018-07-19"
      }
    };
  }

};
</script>

<style scoped>
.roundered {
  border-radius: 1.5rem;
}

.myred {
  background-color: #f5365c !important;
}
</style>