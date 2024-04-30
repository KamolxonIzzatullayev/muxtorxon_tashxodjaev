<script setup lang="ts"></script>

<template>
  <div class="my-banner">
    <div class="bg"></div>
    <div class="image">
      <img src="@/assets/person.jpeg" alt="" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.my-banner {
  // background: linear-gradientto bottom, rgba(0, 0, 0, 0) 0%, #0C0E40 10%);
  background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #0c0e40 100%);
  height: 16.5rem;
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: center;
  position: relative;

  .bg {
    background-image: url("@/assets/flag.png");
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: -1;
    bottom: 1%;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
  }

  .image {
    width: 202px;
    height: 202px;
    border-radius: 50%;
    overflow: hidden;
    border: 2px solid #d9d9d9;

    img {
      object-fit: cover;
      height: 100%;
    }
  }
}
</style>
