<template>
  <div>
    <h1>Result</h1>
    <p>Your Reaction time is :{{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
  </div>
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
    if (this.score < 250) {
      this.rank = "In Human Reaction";
    } else if (this.score < 400) {
      this.rank = "Faster than Michirina2K";
    } else {
      this.rank = "tie w/ Michirina2K";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
