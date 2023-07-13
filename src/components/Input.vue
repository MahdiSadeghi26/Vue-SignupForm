<script setup>
import { ref, computed } from 'vue'
// start validating on start set on true start at submitin set on false
const startValidation = ref(false);
// first name value and validator
const firstName = ref('');
const validatefName = computed(() => {
    if (firstName.value == '' && startValidation.value) {
        return false
    } else {
        return true
    }
})
// last name value and validator
const lastName = ref('')
const validatelName = computed(() => {
    if (lastName.value == '' && startValidation.value) {
        return false
    } else {
        return true
    }
})
// email value and validator
const email = ref('')
const emailValidator = computed(() => {
    if (startValidation.value) {
        return /^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$/.test(email.value)
    } else {
        return true
    }
})
// password value and validator
const password = ref('')
const passwordValidator = computed(() => {

    if (password.value == '' && startValidation.value) {
        return false
    } else {
        return true
    }
})
// submit fucntion
const registerSuccess= computed(()=>{
    startValidation.value=true
    alert('Trail is sent For you!')
    firstName.value=''
    lastName.value=''
    email.value=''
    password.value=''
    startValidation.value=false
})
</script>
<template>
    <div class="input">
        <!-- firstName -->
        <input v-model="firstName" :class="{ error: !validatefName }" type="text" class="inputItem"
            :placeholder="validatefName ? 'First Name' : placeholder">
        <p v-if="!validatefName" class="validatorMessage">FirstName cannot be empty</p>
        <input v-model="lastName" :class="{ error: !validatelName }" type="text" class="inputItem"
            :placeholder="validatelName ? 'Last Name' : placeholder">
        <p v-if="!validatelName" class="validatorMessage">LastName cannot be empty</p>
        <input v-model="email" :class="{ error: !emailValidator }" type="email" class="inputItem"
            :placeholder="emailValidator ? 'Email Address' : placeholder = 'example@gmail.com'">
        <p v-if="!emailValidator" class="validatorMessage">Looks like this is not an email</p>
        <input v-model="password" :class="{ error: !passwordValidator }" type="password" class="inputItem"
            :placeholder="passwordValidator ? 'Password' : placeholder = ''">
        <p v-if="!passwordValidator" class="validatorMessage">Password cannot be empty</p>
        <button @click="registerSuccess" class="submit">CLAIM YOUR FREE TIRAL</button>
        <p class="agreement">By clicking the button, you are agreeing to our <span class="terms">Terms and Services</span>
        </p>
    </div>
</template>
<style lang="scss" scoped>
.input {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    text-align: center;
    .firstName {
        width: 100%;
    }

    .inputItem {
        width: 100%;
        height: 65px;
        padding: 0 20px 0 30px;
        border-radius: 10px;
        border: 1.5px solid hsl(246, 25%, 77%);
        font-weight: 600;
        font-size: 16px;

        &::placeholder {
            font-size: 16px;
            color: black;
            font-weight: 600;
        }

        &:focus {
            border: 2px solid black;
            outline: none;
        }
    }

    .error {
        border: 2px solid hsl(0, 100%, 74%);
        background: url('./images/icon-error.svg') no-repeat right;
        background-position-x: 97%;

        &::placeholder {
            color: hsl(0, 100%, 74%);
        }
    }

    .validatorMessage {
        font-size: 14px;
        margin: 3px 0 15px 0;
        color: #FE0000;
        align-self: flex-end;
    }

    .submit {
        color: white;
        width: 100%;
        border: none;
        height: 60px;
        border-radius: 10px;
        font-weight: 600;
        font-size: 18px;
        box-shadow: 0px 7px 0px -1px rgba(0, 0, 0, 0.17);
        background-color: hsl(154, 59%, 51%);
        cursor: pointer;
        &:hover{
            // background-color: hsl(154, 65%, 38%);
            align-self: center;
            width: 95%;
            background-color: #35A29F;
            transition: all .45s;
        }
    }

    .agreement {
        color: hsl(246, 25%, 77%);
        font-size: 14px;
        span {
            color: hsl(0, 100%, 74%);
        }
    }
}
</style>