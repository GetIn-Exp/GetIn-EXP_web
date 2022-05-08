<template>
    <section class="section section-shaped section-lg my-0">
        <div class="shape shape-style-1 bg-gradient-default">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span></span>
        </div>
        <div class="container pt-lg-md">
            <div class="row justify-content-center">
                <div class="col-lg-6">
                    <card type="secondary" shadow
                          header-classes="bg-white pb-5"
                          body-classes="px-lg-5 py-lg-5"
                          class="border-0">
                        <template>
                            <div class="text-center text-muted mb-4">
                              <small>LOGIN</small>
                            </div>
                            <form role="form">
                              <label>Email</label>
                              <base-input alternative
                                          class="mb-3"
                                          placeholder="Email"
                                          v-model="user">
                              </base-input>
                              <label>Password</label>
                              <base-input alternative
                                          :type="typePassword"
                                          placeholder="Password"
                                          v-model="password">
                              </base-input>
                              <button v-on:click="showPassword()">
                                <small>{{ actionPassword }}</small>
                              </button>
                              <base-checkbox>
                                Remember me
                              </base-checkbox>
                              <div class="text-center">
                                <base-button type="primary" class="my-4" v-on:click="validateUserPsw()">
                                  LOGIN
                                </base-button>
                                <br>
                                <a href="#" class="text-light">
                                  <small>Forget your password?</small>
                                </a>
                              </div>
                            </form>
                        </template>
                        <template>
                            <hr class="hr-black">
                            <div class="text-muted text-center mb-3">
                                <small>ALTERNATIVE LOGIN</small>
                            </div>
                            <div class="btn-wrapper text-center">
                                <base-button type="neutral" v-on:click="showPassword()">
                                    <img slot="icon" src="img/icons/common/github.svg">
                                    Login Github
                                </base-button>
                                <p></p>
                                <base-button type="neutral">
                                    <img slot="icon" src="img/icons/common/google.svg">
                                    Login Google
                                </base-button>
                            </div>
                        </template>
                    </card>
                    <div class="btn-wrapper text-center">
                        <base-button type="primary" class="my-4">
                          CREATE NEW ACCOUNT
                        </base-button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
  data() {
    return {
      user: "",
      password: "",
      typePassword: "password",
      actionPassword: "Show password",
    };
  },
  methods: {
    showPassword: function() {
      if (this.typePassword === "password") {
        this.typePassword = "text";
        this.actionPassword = "Hide password";
      }  else {
        this.typePassword = "password";
        this.actionPassword = "Show password";
      }
    },
    validateUserPsw: function() {
      if (this.user !==  "aitana2022@gmail.com") {
        window.alert("wrong user");
      }else {
        if (this.password !==  "2022") {
          window.alert("password incorrecta");
        } else {
          window.alert("Welcome Aitana");
        }
      };
    },
  },
};
</script>

<style>
.hr-black {
  border-top: 1px solid black;
}
</style>
