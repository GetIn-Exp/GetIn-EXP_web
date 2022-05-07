<template>
  <footer class="page-footer bg-lighter font-small stylish-color-dark pt-4" style="padding-left: 0px;">

    <!-- Footer Links -->
    <div class="container text-center text-md-left">

      <!-- Grid row -->
      <div class="row justify-content-center">


        <!-- Content -->
        <h4 class="font-weight-bold text-center text-default text-uppercase mt-3 mb-4 ">About Us</h4>
        <p class="text-center col-8 mb-4">Here you can discover the perfect job offer that best suits your skills. We help young profiles who are
          willing to start working and doesn't know where to start. If you want more information about us, don´t hesitate
          to follow us in social networks. Get-In Contact!
        </p>

        <!-- Social buttons -->
        <ul class="list-unstyled list-inline text-center ">
          <li class="list-inline-item ">
            <a style="font-size: 2.00rem" class="my-btn btn-floating btn-sm mx-1 waves-effect waves-light">
              <i class="fab fa-facebook text-primary"> </i>
            </a>
          </li>
          <li class="list-inline-item">
            <a style="font-size: 2.00rem" class="btn-floating btn-tw btn-lg mx-1 waves-effect waves-light">
              <i class="fab fa-twitter text-primary"> </i>
            </a>
          </li>
          <li class="list-inline-item">
            <a style="font-size: 2.00rem" class="btn-floating btn-gplus btn-lg mx-1 waves-effect waves-light">
              <i class="fab fa-google-plus text-primary"> </i>
            </a>
          </li>
          <li class="list-inline-item">
            <a style="font-size: 2.00rem" class="btn-floating btn-li btn-lg mx-1 waves-effect waves-light">
              <i class="fab fa-linkedin-in text-primary"> </i>
            </a>
          </li>
        </ul>
        <!-- Social buttons -->
      </div>
    </div>
    <br>

    <!-- Call to action -->
    <ul class="list-unstyled list-inline text-center py-2">
      <li class="list-inline-item">
        <h5 class="mb-1 text-default">Register for free</h5>
      </li>
      <li class="list-inline-item">
        <a href="#!" class="btn btn-primary btn-rounded waves-effect waves-light">Sign up!</a>
      </li>
    </ul>
    <!-- Call to action -->

    <!-- Copyright -->
    <div class="footer-copyright text-center text-default py-3 ">© 2022 Copyright:
      <a href="#"> Get-In Exp.com</a>
    </div>
    <!-- Copyright -->

  </footer>
</template>
<script>
export default {
  name: 'starter-footer',
  data() {
    return {
      year: new Date().getFullYear()
    }
  }
};
</script>
<style>
</style>
