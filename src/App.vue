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
  background: url('./images/bg-intro-desktop.png') hsl(0, 100%, 74%);
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
// media query
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
      .rightSide{
        align-items: center;
      }
    }
  }
}
// 1400px
@media screen and (max-width:1400px) {
  .container{
    >.content{
      width: 90%;
      >.leftSide{
        >.message{
          width: 500;
          .title{
            font-size: 50px;
          }
        }
      }
      >.rightSide{
        align-items: flex-end;
      }
    }
  }
}
// 1200px
@media screen and (max-width:1200px) {
  .container{
    height: 100vh;
    >.content{
      width: 95%;
      >.leftSide{
        >.message{
          >.description{
            width: 100%;
          }
        }
      }
      >.rightSide{
        align-items: flex-end;
      }
    }
  }
}
// 992px
@media screen and (max-width:992px) {
  .container{
    background: url('./images/bg-intro-mobile.png') hsl(0, 100%, 74%);
    height: auto;
    >.content{
      display: flex;
      padding: 50px;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      >.leftSide{
        align-items: center;
        margin-bottom: 20px;
        text-align: center;
        >.message{
          width: 300px;
          >.title{
            text-align: center;
            font-size: 35px;
          }
        }
        >.description{
          width: 400px;
        }
      }
      >.rightSide{
        align-items: center;
        width: 90%;
      }
    }
  }
}
</style>
