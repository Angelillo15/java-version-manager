<template>
  <div class="card">
    <div class="infos">
      <div class="image">
        <img :src="image" alt="image" />
      </div>
      <div class="info">
        <div>
          <p class="name">
            {{ title }}
          </p>
        </div>
        <div class="stats">
          <p class="flex flex-col">
            Java Version
            <span class="state-value">
              {{ javaVersion }}
            </span>
          </p>
          <p class="flex flex-col">
            Publisher
            <span class="state-value">
              {{ publisher }}
            </span>
          </p>
        </div>
      </div>
    </div>
    <button class="request" type="button">Install</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Card",
  setup() {
    return {};
  },
  data() {
    return {};
  },
  props: {
    title: {
      type: String,
      required: true,
    },
    javaVersion: {
      type: String,
      required: true,
    },
    publisher: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },

  },
});
</script>

<style>
.card {
  max-width: 320px;
  border-radius: 1rem;
  background-color: rgb(51, 51, 51);
  padding: 1.5rem;
}

.infos {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  grid-gap: 1rem;
  gap: 1rem;
}

.image {
  height: 7rem;
  width: 7rem;
  border-radius: 0.5rem;
  background-color: rgb(118, 36, 194);
  background: linear-gradient(
    to bottom right,
    rgb(118, 36, 194),
    rgb(185, 128, 240)
  );
}

.info {
  height: 7rem;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.name {
  font-size: 1.25rem;
  line-height: 1.75rem;
  font-weight: 500;
  color: rgba(255, 255, 255, 1);
}

.function {
  font-size: 0.75rem;
  line-height: 1rem;
  color: rgba(156, 163, 175, 1);
}

.stats {
  width: 90%;
  border-radius: 0.5rem;
  background-color: rgba(255, 255, 255, 1);
  padding: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 0.75rem;
  line-height: 1rem;
  color: rgba(0, 0, 0, 1);
}

.flex {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 4px;
}

.state-value {
  font-weight: 700;
  color: rgb(118, 36, 194);
}

.request {
  margin-top: 2rem;
  width: 100%;
  border: 1px solid transparent;
  border-radius: 0.5rem;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  line-height: 1.5rem;
  transition: all 0.3s ease;
}

.request:hover {
  background-color: rgb(118, 36, 194);
  color: #fff;
}
</style>
