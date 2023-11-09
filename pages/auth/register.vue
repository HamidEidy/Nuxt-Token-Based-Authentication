<template>
    <div class="container">
        <div class="row justify-content-center mt-5">
            <div class="col-md-4">
                <form @submit.prevent="register">
                    <div class="mb-3">
                        <label htmlFor="name" class="form-label">Name</label>
                        <input type="text" class="form-control" id="name" v-model="formdata.name" />
                    </div>
                    <div class="mb-3">
                        <label htmlFor="email" class="form-label">Email address</label>
                        <input type="text" class="form-control" id="email" v-model="formdata.email" />
                    </div>
                    <div class="mb-3">
                        <label htmlFor="password" class="form-label">Password</label>
                        <input type="password" class="form-control" id="password" v-model="formdata.password" />
                    </div>
                    <div class="mb-3">
                        <label htmlFor="c_password" class="form-label">Confirm Password</label>
                        <input type="password" class="form-control" id="c_password" v-model="formdata.c_password" />
                    </div>
                    <button class="btn btn-primary">
                        Register
                    </button>
                </form>
            </div>
        </div>
    </div>
</template>




<script setup>

const formdata = reactive({
    name: "",
    email: "",
    password: "",
    c_password: ""

});
async function register() {
    try {
        const user = await $fetch('/api/auth/register', {
            method: 'POST',
            body: formdata
        })
        console.log(user);
    } catch (error) {
        console.log(error.data.data);
    }
}





</script>