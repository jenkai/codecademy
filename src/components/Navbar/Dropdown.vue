<template>
  <div class="nav-text">
    <button
      class="nav-button"
      v-bind:class="{ '-active': isActive }"
      @click="toggleActive"
    >
      <span>{{ mainTitle }}</span>
      <span class="triangle"></span>
    </button>
    <div v-if="isActive" class="drop-rect">
      <div class="list">
        <a
          href="/"
          class="nav-button"
          v-for="title in titles"
          v-bind:key="title"
          >{{ title }}</a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Dropdown",
  props: {
    titles: Array,
    mainTitle: String,
  },
  methods: {
    toggleActive() {
      this.isActive = !this.isActive;
    },
  },
  data() {
    return {
      isActive: false,
    };
  },
};
</script>

<style scoped>
.nav-text {
  margin: 0 0.5rem;
  text-decoration: none;
  color: #10162f;
  position: relative;
}
.nav-button {
  all: unset;
  cursor: pointer;
  color: #10162f;
  white-space: pre;
}
.triangle {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 0.315rem;
  vertical-align: middle;

  border-left: 4px solid transparent;
  border-right: 4px solid transparent;
  border-top: 6px solid #10162f;
  transition: all 0.4s ease-in-out;
}
.nav-button.-active .triangle {
  transform: rotate(-180deg);
}

.drop-rect {
  position: absolute;
  background-color: white;
  border-radius: 2px;
  border-width: 1px;
  border-color: black;
  border-style: solid;
  margin-top: 4px;
}

.list {
  padding: 20px 28px;
}
.list > a {
  /* line-height: 50px; */
  display: block;
  padding: 20px 0;
}

.list > a:hover,
.nav-button:hover,
.nav-text:hover {
  color: #3a10e5;
}
</style>
