<template>
  <div>
    <Message :msg="msg" v-show="msg" />
    <div id="container">
      <h1>Light</h1>
      <div id="content">
        <img :src="image" :alt="desc" />
      </div>
      <div class="group-btn">
        <LigarLuz @ligar="LigarLuz" @click="ligou" />
        <DesligarLuz @desligar="DesligarLuz" @click="desligou" />
      </div>
    <Footer />
    </div>
  </div>
</template>

<script>
import LigarLuz from "@/components/LigarLuz.vue";
import DesligarLuz from "@/components/DesligarLuz.vue";
import Message from "@/components/Message.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "Light",

  components: {
    LigarLuz,
    DesligarLuz,
    Message,
    Footer,
  },
  data() {
    return {
      image: "/img/off.png",
      desc: "light image",
      msg: false,
    };
  },
  methods: {
    LigarLuz() {
      this.image = "/img/on.png";
      // document.getElementById('container').style.backgroundColor = '#FFFF';
      document.getElementById("content").style.backgroundColor =
        "rgba(241, 196, 15, 0.2)";
    },

    DesligarLuz() {
      this.image = "/img/off.png";
      document.getElementById("content").style.backgroundColor =
        "rgba(52, 73, 94, 2)";
    },

    ligou() {
      this.msg = "ligou";
      setTimeout(() => (this.msg = ""), 4000);
    },

    desligou() {
      this.msg = "desligou";
      setTimeout(() => (this.msg = ""), 4000);
    },
  },
};
</script>

<style scoped>
h1 {
  padding: 12px;
  color: #ffff;
}

#msg {
  width: 200px;
  height: 50px;
  background: #2980b9;
  border-radius: 6px;
  color: #ffff;
  font-size: 20px;
  right: 20px;

  display: flex;
  justify-content: center;
  align-items: center;
}
#container {
  margin: 0 auto;
  width: 60%;
  height: 520px;
  background: #2c3e50;
  border-radius: 6px;
}

#content {
  margin: 0 auto;
  width: 80%;
  height: 300px;
  background: rgba(52, 73, 94, 2);
  border-radius: 6px;
}

img {
  width: 300px;
}

.group-btn {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px;
}
</style>