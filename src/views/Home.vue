<template>
  <div>
    <header>
      <!-- Home Navigation Menu (Header) -->
      <nav class="navbar navbar-expand-lg navbar-dark bg-default">
        <div class="container">
          <!-- Get-in-EXP LOGO -->

          <a href="#/landing" class="navbar-brand"> GETIN-EXP </a>

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

            <a href="#/home" class="navbar-brand"> Offerts </a>

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

              <li class="nav-item"><a href="#/profile" class="nav-link">PROFILE</a></li>
              <li class="nav-item dropdown">
                <a
                  href="#/login"
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
          <div class="col-lg-4 mt-5 mt-lg-0">
              <div>
                <h1 class="h1-large text-center">
                  Buscar Ofertas
                </h1>
              </div>

              <div class="card shadow mb-3">

                <div class="container pl-0 pr-0">
                  <div class="row">
                    <div class="col pr-0 nav-pills nav-fill nav-item">
                      <a
                        data-toggle="tab"
                        role="tab"
                        aria-selected="true"
                        style="cursor: pointer"
                        class="p-2 rounded-0 border-bottom shadow-none nav-item nav-link"
                        :class="{'active': !advanced }"
                        @click="advanced = false"
                        ><div>DEFAULT OPTIONS</div>
                      </a>
                    </div>
                    <div class="col pl-0 nav-pills nav-fill nav-item">
                      <a
                        data-toggle="tab"
                        role="tab"
                        aria-selected="true"
                        style="cursor: pointer"
                        class="p-2 rounded-0 border-bottom shadow-none nav-item nav-link"
                        :class="{'active': advanced }"
                        @click="advanced = true"
                        ><div>ADVANCED OPTIONS</div>
                      </a>
                    </div>
                  </div>
                </div>
                <!---->
                

                <div class="card-body">
                  <div
                    class="tab-pane fade active show"
                    style="height: 100px;"
                    aria-expanded="true"
                  >
                    <div id="home-form-search" v-if="!advanced" class="input-group">
                      <!---->
                      <div id="home-form-search-what" class="input-group mb-2 border-2">

                        <base-dropdown tag="div" style="width:100% !important" menuClasses="my-dropdown">
                            <template v-slot:title>
                              <div class="input-group">
                                <input
                                  aria-describedby="addon-right addon-left"
                                  placeholder="QUÉ"
                                  class="form-control dropdown-input border-right-0"
                                  v-model="what"
                                  :class="[
                                    { 'border-primary': whatIsValid },
                                    { 'border-danger': whatIsInvalid },
                                  ]"
                                />
                                <div class="input-group-append">
                                  <span
                                    class="input-group-text border-left-0"
                                    :class="[
                                      { 'text-primary border-primary': whatIsValid },
                                      { 'text-danger border-danger': whatIsInvalid },
                                    ]"
                                    ><i class="ni ni-zoom-split-in"></i
                                  ></span>
                              </div>
                                
                                </div>
                            </template>
                            <li class="dropdown-content" v-for="(item, index) in uniqueTitlesFiltered" 
                                :key="index" @click="selectWhat"> 
                                {{ item }}
                            </li>
                        </base-dropdown>
                        
                        <!---->
                      </div>

                      <div id="home-form-search-where" class="input-group">
                        <base-dropdown tag="div" style="width:100% !important" menuClasses="my-dropdown">
                            <template v-slot:title>
                              <div class="input-group">
                                <input
                                  aria-describedby="addon-right addon-left"
                                  placeholder="DÓNDE"
                                  class="form-control dropdown-input border-right-0"
                                  v-model="where"
                                  :class="[
                                    { 'border-primary': whereIsValid },
                                    { 'border-danger': whereIsInvalid },
                                  ]"
                                />
                                <div class="input-group-append">
                                  <span
                                    class="input-group-text border-left-0"
                                    :class="[
                                      { 'text-primary border-primary': whereIsValid },
                                      { 'text-danger border-danger': whereIsInvalid },
                                    ]"
                                    ><i class="ni ni-pin-3"></i
                                  ></span>
                              </div>
                                
                                </div>
                            </template>
                            <li class="dropdown-content" v-for="(item, index) in uniqueLocationsFiltered" 
                                :key="index" @click="selectWhere"> 
                                {{ item }}
                            </li>
                        </base-dropdown>
                        <!----><!---->
                      
                        <!---->
                      </div>

                    </div>

                    <div id="home-form-filter" v-else class="input-group">
                      
                      <div id="home-form-datepicker" class="input-group mb-2 input-daterange datepicker"
                      >
                        <base-input
                          name="calendar"
                          class="mb-0 pb-0"
                        >
                          <template v-slot:addonLeft>
                            <i class="ni ni-calendar-grid-58 mr-2"></i>
                            <span class="input-text">AFTER</span>
                          </template>

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
                      </div>

                      <div id="home-form-dropdown" class="input-group">
                        <text-dropdown />
                      </div>
                    </div>

                  </div>
                </div>

                <button id="home-form-btn"
                    class="btn btn-icon btn-default btn-style"
                    @click="search"
                  >
                    <!----><!----><!---->
                    <span class="btn-inner--icon"
                      ><i class="ni ni-atom"></i
                    ></span>
                    SEARCH RESULTS
                </button>

              </div>

              <div class="row justify-content-center"> 
                  <img class="p-2" src='img/theme/logo.jpg' alt="NoImage"/>
              </div>
          </div>

          <!--_Second Column: offerts list -->
          <div class="col-lg-8">

            <!-- ANYTHING SEARCHED SO FAR -->
            <div v-if="!searchPerformed" id="home-empty">
              <div class="flex-column text-container text-center">
                <h2>Get the best offerts now!</h2>
                <p class="font-weight-bold"> 
                  In Getin-Exp we know how difficult is to get your first job without experience. 
                  We've been there too! That's the reason we've created the perfect job finder for you. 
                  Let the search engine do your work for you! 
                </p>
                <div style ="height: 300px">
                  <img class="my-img-container" src="img/theme/experience.jpg" alt="wtf meme" />
                </div>
              </div>
            </div>

            <!-- INVALID USER INPUT -->
            <div v-else-if="searchPerformed & !searchIsValid" id="home-invalid-search">
              <div class="flex-column text-container text-center">
                <h2>HEY! Invalid Search Input</h2>
                <p class="font-weight-bold"> Please, fill up all the requested inputs before searching </p>
                <div style ="height: 300px">
                  <img class="my-img-container" src="img/theme/wtf.jpg" alt="wtf meme" />
                </div>
              </div>
            </div>

            <!-- NO RESULTS -->
            <div v-else-if="searchPerformed & searchIsValid & !hasResults" id="home-not-results">
              <div class="flex-column text-container text-center">
                <h2>OPS! No results found</h2>
                <p class="font-weight-bold"> You can try either changing the job title or the location. </p>
                <div style="height: 300px;">
                  <img class="my-img-container" src="img/theme/ops.jpg" alt="ops meme" />
                </div>
                
              </div>
              
            </div>

            <!-- DISPLAY OFFERTS -->
            <div v-else id="home-results">
              <div class="mb-3 ml-4 mr-4">
                <h4>
                  Ofertas relacionadas con
                  <span class="font-weight-bold text-uppercase">
                    {{ resultsWhat }}
                  </span>
                </h4>
                <small class="text-uppercase font-weight-bold">
                  {{ listaResultadosOfertas.length }} resultados en {{ resultsWhere }}
                </small>
                <hr class="mt-0" style="border: 1px solid black" />
              </div>

              <div class="row justify-content-center mb-3 ml-4 mr-4"></div>
              <ul id="offerts-panel">
                <li v-for="item in listaResultadosOfertas" :key="item.id">
                  <offert-card>
                    <template #title> {{ item.title }} </template>
                    <template #description> {{ item.description }} </template>
                    <template #company> {{ item.company }} </template>
                    <template #location> {{ item.location }} </template>
                    <template #money> {{ item.money }} </template>
                  </offert-card>
                </li>
              </ul>
            </div>

            

            

          </div>
        </div>
      </div>
    </body>
  </div>
</template>

<script>
import flatPicker from "vue-flatpickr-component";
import BaseDropdown from '../components/BaseDropdown.vue';
import TextDropdown from "./components/TextDropdown";
import OffertCard from "./components/OffertCard.vue";
import TabsSection from "./components/JavascriptComponents/TabsSection";
import ProgressSection from "./components/JavascriptComponents/ProgressPagination";
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
    BaseDropdown,
    TextDropdown,
    TabsSection,
    ProgressSection,
    OffertCard,
  },

  data() {
    return {
      what: "",
      where: "",
      category: "",
      dates: {
        simple: "2018-07-17",
      },

      advanced: false,
      searchPerformed: false,
      searchIsValid: false,
      hasResults: false,
      
      resultsWhat: "",
      resultsWhere: "",
      listaResultadosOfertas: [],
      listaOfertas: [
        {
          id: 1,
          title: "Responsable de Logística",
          description: "First Offert Mockup",
          company: "AXA Aseguradora",
          location: "Area Metropolitana de Barcelona",
          money: "10000$",
        },
        {
          id: 2,
          title: "Responsable de Logística",
          description: "Second Offert Mockup",
          company: "AXA Aseguradora",
          location: "Area Metropolitana de Barcelona",
          money: "10000$",
        },
        {
          id: 3,
          title: "Responsable de Logística",
          description: "Third Offert Mockup",
          company: "AXA Aseguradora",
          location: "Area Metropolitana de Barcelona",
          money: "10000$",
        },
        {
          id: 4,
          title: "Responsable de Logística",
          description: "Forth Offert Mockup",
          company: "AXA Aseguradora",
          location: "Area Metropolitana de Barcelona",
          money: "10000$",
        },
      ],
      
    };
  },

  methods: {
    search(event) {
      this.searchPerformed = true;
      this.resultsWhat = this.what;
      this.resultsWhere = this.where;
      this.searchIsValid = this.whatIsValid & this.whereIsValid;
      if (this.searchIsValid) {

        this.listaResultadosOfertas = this.listaOfertasFiltrada;
        this.hasResults = this.listaResultadosOfertas.length > 0;
      }

      // If the search is invalid,
      else{
        this.advanced = false;
        this.hasResults = false;
      }
    },

    selectWhat(event){
      console.log(event.target.firstChild.data);
      this.what = event.target.firstChild.data.replace(/(^\s+)|(\s+$)/g, '');
    },

    selectWhere(event){
      console.log(event.target.firstChild.data);
      this.where = event.target.firstChild.data.replace(/(^\s+)|(\s+$)/g, '');
    },

    selectCategory(event){
      console.log(event.target.firstChild.data);
      this.category = event.target.firstChild.data.replace(/(^\s+)|(\s+$)/g, '');
    },

    onlyUnique(value, index, self) {
      return self.indexOf(value) === index;
    },
  },

  computed: {
    whatIsValid() {
      return this.searchPerformed & (this.what.length > 0);
    },

    whatIsInvalid() {
      return this.searchPerformed & (this.what.length == 0);
    },

    whereIsValid() {
      return this.searchPerformed & (this.where.length > 0);
    },

    whereIsInvalid() {
      return this.searchPerformed & (this.where.length == 0);
    },

    uniqueTitles(){
      var mylist = [];
      for (var item of this.listaOfertas){
        if (!(mylist.includes(item.title))){
          mylist.push(item.title);
        }
      }
      return mylist
    },

    uniqueLocations(){
      var mylist = [];
      for (var item of this.listaOfertas){
        if (!(mylist.includes(item.location))){
          mylist.push(item.location);
        }
      }
      return mylist;
    },

    uniqueTitlesFiltered(){
      return this.uniqueTitles.filter(title => 
        title.toUpperCase().includes( this.what.toUpperCase() )
      );
    },

    uniqueLocationsFiltered(){
      return this.uniqueLocations.filter(location =>
        location.toUpperCase().includes( this.where.toUpperCase() )
      );
    },

    // async offerts list having applyed all the input restrictions
    listaOfertasFiltrada(){
      console.log(this.uniqueLocations);
      return this.listaOfertas.filter((item) => {
          return (
            item["title"].toUpperCase().includes(this.what.toUpperCase()) &
            item["location"].toUpperCase().includes(this.where.toUpperCase())
            // We can add here the category and the date filter contributions
          );
        });
    },

  },

};
</script>

<!-- Can't be scoped if we pretend to export label-style outside -->
<style>
.roundered {
  border-radius: 1.5rem;
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

.dropdown-input{
    padding-right: 0.75rem !important; 
    border: 1px solid #cad1d7 !important;
}

.my-dropdown{
    width: 100% !important;
    margin: 0 !important;
    padding: 0 !important;
}

.dropdown-content{
    padding: 10px;
}

.dropdown-content:hover{
    background-color: #cad1d7;
    border-block: 1px solid #659ac8;
}

.dropdown-categories {
  position: absolute;
  top: 100%;
  right: 100% !important;
  float: left;
  background-color: inherit;
  background-clip: padding-box;
}

#home-form-btn:hover{
  transform: none;
}

#offerts-panel {
  width: 100%;
  list-style: none;
  margin: 0;
  padding: 0;
}

#offerts-panel > li {
  margin-bottom: 1rem;
}

#home-form-advanced-btn{
  width: 100%;
}

.my-img-container{
  max-height: 100%;
}

.section {
  padding: 70px 0;
  background-color: transparent !important;
  margin-top: 1%;

  div.button-container {
    text-align: center;
    margin-top: -106px;
  }

  h4.title {
    margin-top: -106px;
  }
}

.checkout_card {
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
}

.my-input-is-valid . {
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