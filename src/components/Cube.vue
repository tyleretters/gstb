<template>
  <div class="wrapper">
    <div class="cube">
      <div class="face front"></div>
      <div class="face back"></div>
      <div class="face left"></div>
      <div class="face right"></div>
      <div class="face top"></div>
      <div class="face bottom"></div>
    </div>
    <a href="https://goodshitsthebest.com" class="buy">I WOULD LIKE TO BUY.</a>
  </div>
</template>
<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 0;
}

.cube {
  margin-top: 100px;
  width: 200px;
  height: 200px;
  position: relative;
  transform-style: preserve-3d;
  transform: rotateX(-30deg) rotateY(-30deg);
  animation: rotateCube 10s infinite linear;
  z-index: 50;
}

@media screen and (min-width: 768px) {
  .cube {
    margin-top: 400px;
  }
}

.face {
  position: absolute;
  width: 200px;
  height: 200px;
  background-size: cover;
  background-position: center;
}

.front  { transform: rotateY(  0deg) translateZ(100px); background-image: url('../assets/cube-face.jpg'); }
.back   { transform: rotateY(180deg) translateZ(100px); background-image: url('../assets/cube-face.jpg'); }
.left   { transform: rotateY(-90deg) translateZ(100px); background-image: url('../assets/cube-face.jpg'); }
.right  { transform: rotateY( 90deg) translateZ(100px); background-image: url('../assets/cube-face.jpg'); }
.top    { transform: rotateX( 90deg) translateZ(100px); background-image: url('../assets/cube-face.jpg'); }
.bottom { transform: rotateX(-90deg) translateZ(100px); background-image: url('../assets/cube-face.jpg'); }

@keyframes rotateCube {
  0% { transform: rotateX(-30deg) rotateY(-30deg); }
  100% { transform: rotateX(-30deg) rotateY(330deg); }
}

.buy {
  text-align: center;
  width: auto;
  padding: 16px;
  height: 64px;
  display: block;
  text-align: center;
  line-height: 64px;
  font-size: 24px;
  text-transform: uppercase;
  text-decoration: none;
  position: absolute;
  background: #FF0000;
  color: #FFFF00;
  z-index: 100;
  &:hover {
    background: #FFFF00;
    color: #FF0000;
  }
  top: 500px;
}
</style>
