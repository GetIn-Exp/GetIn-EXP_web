<template>
  <div>
    <div style="margin-top: 5rem" class="container ">
      <div class="row">
        <div class="col-lg-6 col-xl-5">
          <div class="text-container">
            <h1 class="h1-large">Find influencers for your products</h1>
            <p class="p-large">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut dignissim, neque ut ultrices sollicitudin</p>
            <a class="btn-solid-lg" href="#services">Offered services</a>
          </div>
        </div>
        <div class="col-lg-6 col-xl-7">
          <div class="image-container">
            <img class="" src="assets/images/header-image.png" alt="alternative" />
          </div>
        </div>
      </div>
    </div>
  <div id="services" class="cards-1 bg-gray">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <h2>Explore our services</h2>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-12">


          <div class="card">
            <div class="card-icon">
              <span class="fas fa-headphones-alt"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">Analyse your product</h5>
              <p>Et blandit nisl libero at arcu. Donec ac lectus sed tellus mollis viverra. Nullam pharetra ante at nunc elementum</p>
              <a class="read-more no-line" href="#">Learn more <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
          </div>

          <div class="card">
            <div class="card-icon red">
              <span class="far fa-clipboard"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">Evaluate opportunities</h5>
              <p>Vulputate nibh feugiat. Morbi pellent diam nec libero lacinia, sed ultrices velit scelerisque. Nunc placerat justo sem</p>
              <a class="read-more no-line" href="#">Learn more <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
          </div>

          <div class="card">
            <div class="card-icon green">
              <span class="far fa-comments"></span>
            </div>
            <div class="card-body">
              <h5 class="card-title">Find the influencers</h5>
              <p>Ety suscipit metus sollicitudin euqu isq imperdiet nibh nec magna tincidunt, nec pala vehicula neque sodales verum</p>
              <a class="read-more no-line" href="#">Learn more <span class="fas fa-long-arrow-alt-right"></span></a>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
  </div>
</template>

<script>
import StarterHeader from "@/layout/starter/StarterHeader";
export default {
  name: "home",
  components: {StarterHeader}
};
</script>
