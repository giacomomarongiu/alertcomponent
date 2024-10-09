<script setup>
import AlertComponent from "./components/AlertComponent.vue";

function hadleEvent() {
  console.log("Hai chiuso un alert");
}
</script>

<template>
  <div class="container">
    <AlertComponent type="info"> Informazioni Ottenute </AlertComponent>
    <AlertComponent type="danger"> Informazioni Pericolose </AlertComponent>
    <AlertComponent type="warning"> NON PUOI FRAMI QUESTO</AlertComponent>
    <AlertComponent type="success" @closed="hadleEvent">
      Puoi fare cio' che vuoi
    </AlertComponent>
  </div>
</template>

<style scoped></style>
