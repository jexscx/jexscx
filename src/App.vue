<template>
  <div id="app">
    <b-container fluid class="app-row">
  <b-row class="container-row">
    <b-col class="settings">
      Settings
          <Settings />
    </b-col>
    <b-col class="calendar ">
          <Calendar />
    </b-col>
  </b-row>
    <b-row class="container-row">
    <b-col class="empty">
    </b-col>
    <b-col class="addDate ">
        <AddEventButton />
    </b-col>
  </b-row>
</b-container>
  </div>
</template>

<script>
import Settings from "./components/Settings.vue";
import Calendar from "./components/Calendar.vue";
import AddEventButton from "./components/AddEventButton.vue";

export default {
  name: "App",
  components: {
    Settings,
    Calendar,
    AddEventButton
  }
}
</script>

<style scoped>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100vh;
  margin: auto;
}
  .app-row{
    margin: auto;
  }

  .settings
  {
    margin: auto;
  }

  .calendar{
    text-align: right;
    margin: auto;

  }
 .container-row{
    margin: 0 0 2% 0;

  }

  
</style>
