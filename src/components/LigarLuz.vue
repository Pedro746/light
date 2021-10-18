<template>
  <div>
    <button id="btn-on" @click="$emit('Ligar')">Ligar</button>
  </div>
</template>

<script>
export default {
  name: "LigarLuz",
  emits: ["Ligar"],
};
</script>

<style scoped>
#btn-on {
  border: none;
  border-radius: 6px;
  font-size: 18px;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  background: rgba(241, 196, 15, 1);
  border: 2px solid rgba(241, 196, 15, 1);
  color: #ffff;
  transition: 0.5s;
}

#btn-on:hover {
  background: #ffff;
  border: 2px solid rgba(241, 196, 15, 1);
  color: #222;
}

button {
  width: 100px;
  padding: 12px;

  margin: 0 15px;
  cursor: pointer;
}
</style>