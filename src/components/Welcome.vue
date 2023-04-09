<template>
  <div class="intro">
    <h2>Welcome to Java Version Manage</h2>
    <p>Select a version to install:</p>
  </div>
  <div class="card-array">
    <Card
      publisher="OpenJDK"
      javaVersion="Java 8"
      title="Java 8"
      image="https://www.oracle.com/a/ocom/img/obic-java-cup.svg"
    />
    <Card
      publisher="OpenJDK"
      javaVersion="Java 8"
      title="Java 8"
      image="https://www.oracle.com/a/ocom/img/obic-java-cup.svg"
    />
    <Card
      publisher="OpenJDK"
      javaVersion="Java 8"
      title="Java 8"
      image="https://www.oracle.com/a/ocom/img/obic-java-cup.svg"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Card from "./Card.vue";

export default defineComponent({
  name: "Welcome",
  setup() {
    return {};
  },
  components: {
    Card,
  },
});
</script>

<style scoped>
.intro {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  width: 100%;
  text-align: center;
}

.card-array {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  width: 100%;
  flex-wrap: wrap;
  text-align: center;
}

.card-array > * {
  margin: 1rem;
}
</style>
