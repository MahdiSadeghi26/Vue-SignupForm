<script setup>
import SignupForm from "./components/SignupForm.vue";
</script>

<template>
  <div class="container">
    <div class="content">
      <div class="leftSide">
        <div class="message">
          <p class="title">Learn to code by watching others</p>
        </div>
        <div class="description">
          <p>See how experienced developers solve problems in real-time. Watching scripted tutorials is great, but
            understanding how developers think is invaluable</p>
        </div>
      </div>
      <div class="rightSide">
        <SignupForm/>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.container {
  width: 100vw;
  height: 100vh;
  background: url('./images/bg-intro-desktop.png'), hsl(0, 100%, 74%);
  display: flex;
  justify-content: center;
  align-items: center;
  >.content {
    width: 85%;
    height: 85%;
    display: grid;
    grid-template-columns: 50% 50%;
    >.leftSide {
      display: flex;
      justify-content: center;
      align-items: flex-start;
      color: white;
      flex-direction: column;
      >.message {
        width: 500px;
        >.title {
          font-weight: 700;
          font-size: 55px;
          text-align: left;
          line-height: 55px;
        }
      }
      >.description {
        width: 550px;
        margin-top: 20px;
        >p {
          font-size: 16px;
        }
      }
    }
    .rightSide {
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
  }
}
@media screen and (min-width:1600px) {
  .container{
    >.content{
      width: 80%;
      >.leftSide{
        >.message{
          width: 600px;
          >.title{
            align-self: center;
            line-height: 65px;
            font-size: 60px;
          }
          .description{
            align-self: flex-start;
          }
        }
      }
    }
  }
}
</style>
