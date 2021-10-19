<template>
  <div>
    <button id="btn-of" @click="$emit('Desligar')">Desligar</button>
  </div>
</template>

<script>
export default {
  name: "DesligarLuz",
  emits: ["Desligar"],
};
</script>

<style scoped>
#btn-of {
  border: none;
  border-radius: 6px;
  font-size: 18px;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  background: rgba(52, 73, 94, 1);
  border: 2px solid rgba(52, 73, 94, 1);
  color: #ffff;
  background: rgba(52, 73, 94, 1);
  transition: 0.5s;
}
#btn-of:hover {
  background: #ffff;
  border: 2px solid rgba(52, 73, 94, 1);
  color: #222;
}

button {
  width: 100px;
  padding: 12px;

  margin: 0 15px;
  cursor: pointer;
}

@media only screen and (max-width: 600px) {
  button {
    width: 250px;
  }
}
</style>