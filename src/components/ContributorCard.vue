<template>
  <div class="card" v-html="contributor"></div>
</template>

<script>
export default {
  props: {
    contributor: String,
  },
  mounted() {
    console.log(this.contributor);
  },
};
</script>

<style>
.card {
  background-image: radial-gradient(
    circle 674px at 17.4% 30.3%,
    rgba(58, 231, 224, 0.7) 0%,
    rgba(59, 173, 219, 1) 66.6%
  );
  border-radius: 10px;
  height: 80px;
  width: 40%;
  font-size: 1.6em;
  display: flex;
  align-items: center;
  justify-content: center;
}

.card p {
  color: black;
  font-weight: bold;
}
</style>
