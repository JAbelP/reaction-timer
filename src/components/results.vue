<template>
  <p>Reaction Time: {{ score }}ms - Rank: {{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score <= 250) {
      this.rank = "Finger Guns";
    } else if (this.score <= 400) {
      this.rank = "close call";
    } else {
      this.rank = "maybe you should stick to a joypad";
    }
  },
};
</script>

<style></style>
