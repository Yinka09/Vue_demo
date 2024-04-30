<template>
  <div class="container">
    <p>{{ count }}</p>
    <p>{{ doubleCount }}</p>
    <button @click="increment">Add Count</button>
  </div>
</template>

<script>
export default {
  computed: {
    count() {
      return this.$store.state.count;
    },
    doubleCount() {
      return this.$store.getters.doubleCount;
    },
  },
  methods: {
    increment() {
      this.$store.dispatch("asyncIncrement", 20);
    },
  },
};
</script>
