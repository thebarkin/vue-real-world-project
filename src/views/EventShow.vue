<template>
  <h1>Showing Event #{{ id }}</h1>
</template>

<script>
export default {
  props: {
    id: {
      type: Number,
      default: 1
    }
  }
};
</script>
