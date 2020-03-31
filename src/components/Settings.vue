<template>
  
<div class="flex">
  <b-card-group deck>
  <b-card
    title="Animal faces"
    class="animal"
    @click='toggleAnimal'
  >
    <b-card-text >
      {{ animal }}
    </b-card-text>
  </b-card>
    <b-card
    @click='toggleBackground'
    class="background"
    title="Background"
  >
    <b-card-text >
      {{ background }}
    </b-card-text>
    </b-card>
    <b-card
    @click='toggleMirror'
    class="mirror"
    title="Distorting mirror"
  >
    <b-card-text >
      {{ mirror }}
    </b-card-text>
  </b-card>
  </b-card-group>
</div>
</template>

<script>
export default {
data() {
  return {
    animal: false,
    background: false,
    mirror: false
  }
},
methods: {
        toggleAnimal: function(){
            this.animal = !this.animal
        },
                toggleBackground: function(){
            this.background = !this.background
        },
                toggleMirror: function(){
            this.mirror = !this.mirror
        },
                toggle: function(){
            this.isOpen = !this.isOpen
        }
    }
}
</script>

<style scoped>

</style>