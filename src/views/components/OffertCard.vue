<template>
    <component 
        class="container"
        :is="tag"
        >
        <div class="card border my-card">
            <div class="row">
                <div class="col-4 img-container-container"> 
                    <img class="p-2" src='img/theme/axa-logo-rrss.png' alt="NoImage"/>
                </div>

                <div class="col-8">
                    <div class="row">
                        <div class="col">
                        <div class="card-title mt-3 mb-0">
                            <h5 class="tab-pane-title font-weight-bold text-uppercase">
                            <slot name="title">
                                Responsable de Logística
                            </slot>
                            </h5>
                        </div>
                        <div class="card-company mb--5">
                            <small class="font-weight-bold "> 
                            <slot name="company">
                                Dalt Tech SL
                            </slot>
                            </small>
                        </div>
                        <div class="card-location">
                            <small class="font-weight-bold "> 
                            <slot name="location">
                                Área Metropolitana de Barcelona, 08392
                            </slot>
                            </small>
                        </div>
                        </div>

                        <div class="col">
                        <p class="card-money text-right m-3">
                            <slot name="money">
                                20.000$ - 30.000$
                            </slot>
                        </p>
                        </div>
                    
                    </div>

                    <div class="card-body ml-0 pl-0 text-justify">
                        <slot name="description">
                            Raw denim you probably haven't heard of them jean shorts
                            Austin. Nesciunt tofu stumptown aliqua, retro synth
                            master cleanse. Mustache cliche tempor, williamsburg
                            carles vegan helvetica. Reprehenderit butcher retro
                            keffiyeh dreamcatcher synth.
                        </slot>
                    </div>
                </div>
            </div>
        </div>
    </component>
</template>
<script>
export default {
  name: "offert-card",
  props: {
    tag: {
      type: String,
      default: "li",
      description: "Dropdown html tag (e.g div, li etc)"
    }
  },
};
</script>

<style scoped>
.my-card:hover{
    background-color: #F1FDFE;
    box-shadow: 0px 10px 25px 0px rgba(0, 0, 0, 0.2);
}

</style>