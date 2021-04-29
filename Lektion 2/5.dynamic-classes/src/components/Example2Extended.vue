<template>
  <div>
        <form class="mb-3">
            <input type="text" v-model="email" @keyup="validateEmail" :class="valid ? '': 'error'">
        </form>
  </div>
</template>

<script>
export default {
    data() {
        return {
            valid: false,
            email: ''
        }
    },
    methods: {
        validateEmail() {
            const regex = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;

            if(regex.test(String(this.email).toLowerCase()))
                this.valid = true
            else
                this.valid = false
        }
    }
}
</script>

<style>
.error {
    background: pink;
    border-color: red;
}


</style>