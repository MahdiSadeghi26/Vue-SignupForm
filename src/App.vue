<script setup>
</script>

<template>
  <div class="container">
    <div class="content">
      <div class="leftSide">
          
      </div>
      <div class="rightSide"></div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.container{
  width: 100vw;
  height: 100vh;
  background: url('./images/bg-intro-desktop.png'),hsl(0, 100%, 74%) ;
  display: flex;
  justify-content: center;
  align-items: center;
  .content{
    width: 80%;
    height: 90vh;
    display: grid;
    grid-template-columns: 50% 50%;
    .leftSide{
    }
    .rightSide{
    }
  }
}
</style>
