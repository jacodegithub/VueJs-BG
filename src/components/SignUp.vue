<template>
    <h1 class="sign-up-title">Sign Up</h1>
    <div class="sign-up">
        <input type="text" v-model="name" placeholder="Enter name" />
        <input type="email" v-model="email" placeholder="Enter email" />
        <input type="password" v-model="password" placeholder="Enter password" />
        <button @click="signUp">Sign Up</button>
    </div>
</template>
<script>
export default {
    name: 'SignUp',
    data()
    {
        return {
            name: '',
            email: '',
            password: '',
        }
    },
    methods:{
        signUp()
        {
            console.log('clicked ', this.name)
        }
    }
}
</script>

<style>
.sign-up-title {
    text-align: center;
    margin: 1.5rem;
}

.sign-up {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 1.5rem;
}

.sign-up input {
    border: none;
    width: 20rem;
    height: 3rem;
    border-radius: .2rem;
}

.sign-up input:focus {
    outline: none;
}

.sign-up button {
    width: 20rem;
    height: 3rem;
    border-radius: .2rem;
    font-size: 1.2rem;
    font-weight: bold;
    background: black;
    color: white;
    border: none;
    cursor: pointer;
}

.sign-up button:active {
    transform: scale(.98);
}
</style>