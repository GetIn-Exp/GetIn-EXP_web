<template>
    <component 
        class="tab-content"
        :is="tag"
        >
        <div class="card my-card">
            <!---->
            <div class="card-body">
                <div class="tab-pane fade active show">
                    <div class="ml-1">
                        <h5 class="tab-pane-title font-weight-bold text-uppercase">
                            <slot name="title">
                                Responsable de Logística
                            </slot>
                        </h5>
                        <small class="tab-pane-company text-uppercase font-weight-bold"> 
                            <slot name="company">
                                Dalt Tech SL
                            </slot>
                        </small>
                        <small class="tab-pane-location text-uppercase font-weight-bold"> 
                            <slot name="location">
                                Área Metropolitana de Barcelona, 08392
                            </slot>
                        </small>
                    </div>
                    
                    <p class="tab-pane-description">
                        <slot name="description">
                            Raw denim you probably haven't heard of them jean shorts
                            Austin. Nesciunt tofu stumptown aliqua, retro synth
                            master cleanse. Mustache cliche tempor, williamsburg
                            carles vegan helvetica. Reprehenderit butcher retro
                            keffiyeh dreamcatcher synth.
                        </slot>
                    </p>

                    <div class="tab-pane-minifooter mt-1">
                        <small class="tab-pane-date text-uppercase font-weight-bold"> 
                            Active since 
                            <slot name="date"> 
                                07 - 05 - 2022 
                            </slot>
                        </small>
                    </div>
                </div>
            </div>
            <!----><!---->
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
.my-card{
    border: 1px solid black;
}

</style>