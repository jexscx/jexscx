<template>
      <b-calendar block class="calendar" locale="en-US"></b-calendar>
</template>


<script>
  export default {
    data() {
      return {
        value: '',
        context: null
      }
    },
    methods: {
      onContext(ctx) {
        this.context = ctx
      }
    }
  }
</script>

