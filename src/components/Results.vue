<template>
  <p class="results">tu score es {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
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
      this.rank = "Mero reflejos pa";
    } else if (this.score < 400) {
      this.rank = "Normal";
    } else {
      this.rank = "Reflejos de cucho";
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
