<script>
export default {
  data() {
    return {
      count: 0
    };
  }
};
</script>

<style scoped>
.load {
  background-color: var(--main-color);
  overflow: hidden;
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: center;
  z-index: 100000;
}

.loadElement {
  background-color: black;
  height: 20px;
  width: 20px;
  border-radius: 80px;
  margin: 5px;
}

.loadElement:nth-child(1) {
  animation: preloader 0.6s ease-in-out alternate infinite;
}

.loadElement:nth-child(2) {
  animation: preloader 0.6s ease-in-out alternate 0.3s infinite;
}

.loadElement:nth-child(3) {
  animation: preloader 0.6s ease-in-out alternate 0.6s infinite;
}
@keyframes preloader {
  0% {
    top: -5px;
    background: #cdd1e4;
    transform: scale(1);
  }
  100% {
    top: 5px;
    background: #4d13d1;
    transform: scale(1.2);
  }
}
</style>

<template>
  <div class="load">
    <div class="loadElement"></div>
    <div class="loadElement"></div>
    <div class="loadElement"></div>
  </div>
</template>