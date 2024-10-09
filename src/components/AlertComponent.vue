<script setup>
import { ref } from "vue";

const props = defineProps({
  type: String,
});

const emit = defineEmits(["closed"]);

const tag = ref();
tag.value = props.type;

const count = ref(0);

function functionClicked() {
  emit("closed");
}
</script>

<template>
  <div class="alert alert-dismissible fade show" :class="`alert-${props.type}`">
    <strong><slot></slot></strong>
    <button
      @click="functionClicked()"
      type="button"
      class="btn-close"
      data-bs-dismiss="alert"
      aria-label="Close"
    ></button>
  </div>
</template>

<style scoped></style>
