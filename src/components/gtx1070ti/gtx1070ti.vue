<template>
  <div class="root">
    <div class="main-card" @click="show1070Modal = true">
      <img class="card-image1070" src="./1070ti.png" />

             <div class="image-overlay image-overlay__primary">
        <p class="image-title">Информация</p>        
      </div>
      <h1 class="card-header">GTX 1070ti</h1>

      <p class="card-text">
    GeForce GTX 1070 Ti — высокопроизводительная видеокарта от NVIDIA, выпущенная 2 ноября 2017 года.
      </p>
    </div>

    <Teleport to="body">
      <Modal 
        :show="show1070Modal"
        @close="show1070Modal = false"
      />
    </Teleport>
  </div>
</template>

<script>
import Modal from './modal1070.vue'

  export default {
    components: {
      Modal,
    },

    data: () => ({
      show1070Modal: false,
    })
  };

</script>

<style>
.main-card {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;

  font-family: "Geforce";
  color: #00ff29;

  background-color: black;
  box-shadow: 10px 10px 10px rgba(24, 24, 24, 0.379);

  margin-top: 30px;
  margin-right: 62px;

  padding: 10px;

  width: 220px;
  height: 350px;
}

.card-text {
  color: #fff;
  font-weight: bold;
  font-size: 18px;
}
.card-image1070 {
  width: 160px;
  height: 160px;
  transform: rotate(10deg);
}
</style>