<script setup>
import Input from './Input.vue';

</script>
<template>
    <div class="signupContainer">
        <div class="terial">Try it free 7 days then <span>$20/mo. thereafter</span></div>
        <div class="form">
            <Input/>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .signupContainer{
        width: 100%;
        height: 600px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        >.terial{
        width: 95%;
        font-weight: 600;
        font-size: 18px;
        color: white;
        padding: 18px;
        border-radius: 10px;
        background-color: hsl(248, 32%, 49%);
        text-align: center;
        box-shadow: 0px 10px 0px -1px rgba(0,0,0,0.17);
        span{
            color: #F5F5F5;
            font-weight: 300;
        }
    }
    >.form{
        width: 95%;
        height: 550px;
        border-radius: 10px;
        background-color: white;
        margin-top: 20px;
        box-shadow: 0px 10px 0px -1px rgba(0,0,0,0.17);
        padding: 40px 25px 30px 25px;
      }
    }
    // media query
    @media screen and (min-width: 1600px) {
        .signupContainer{
            width: 600px;
            align-items: flex-end;
        }
    }
    // 1200px
    @media screen and (max-width:1200px) {
        .signupContainer{
            width: 90%;
            // height: 590px;
        }
    }
    // 576 px
    @media screen and (max-width:576px) {
        .signupContainer{
            width: 100%;
            
        }
    }
</style>