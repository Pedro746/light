<template>
  <Light />
</template>

<script>
import Light from "@/components/Light.vue";

export default {
  name: "App",
  components: {
    Light,
  },
};
</script>

<style>
Body {
  @import url("https://fonts.googleapis.com/css2?family=Nunito:wght@200;300;400;600;800&display=swap");
  font-family: "Nunito", sans-serif;
  background: #bdc3c7;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
