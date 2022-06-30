<template>
  <div class="show">
    <div class="show__results" v-for="(result, index) in results" :key="index">
      <p class="top__link">{{ result.link }}</p>
      <p class="title">
        <a :href="result.link"> {{ result.title }}</a>
      </p>
      <p class="description">{{ result.snippet }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["results"],
};
</script>

<style scoped>
.show {
  width: 1200px;
  margin: 50px auto;
}
.show__results {
  width: 700px;
  margin-top: 20px;
  margin-bottom: 30px;
}
.top__link {
  color: #bdc1c6;
  font-size: 13px;
  margin-bottom: 5px;
}
.title a {
  color: #8ab4f8;
  text-decoration: none;
  font-size: 20px;
  display: inline-block;
  margin-bottom: 9px;
}
.description {
  color: #bdc1c6;
}
</style>
