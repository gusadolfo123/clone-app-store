<template>
  <div id="app" class="font-sans flex min-h-screen">
    <sidebar></sidebar>
    <router-view />
  </div>
</template>

<script>
import Sidebar from "./components/Sidebar";

export default {
  components: {
    Sidebar
  }
};

const customTitlebar = require("custom-electron-titlebar");

let customTitleBar = new customTitlebar.Titlebar({
  backgroundColor: customTitlebar.Color.fromHex("#444")
});

customTitleBar.updateIcon("./assets/icono.png");
customTitleBar.updateTitle("Generate Batch App");

</script>

<style src="./assets/main.css">
