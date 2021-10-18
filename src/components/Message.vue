<template>
  <div class="message-container">
    <p>Você {{ msg }} a luz!</p>
  </div>
</template>

<script>
export default {
  name: "Message",
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.message-container {
  position: absolute;
  right: 10px;
  color: #ffff;
  background: #2ecc71;
  /* border: 2px solid #27AE60; */
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 6px;
  padding: 10px;
  max-width: 400px;
  min-width: 200px;
  margin: 30px auto;
  animation-duration: 2s;
  animation-name: fade-out;
}

@keyframes fade-out {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
