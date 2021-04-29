<template>
  <div>
        <h1 class="display-5">Form Inputs</h1>

        <form id="form" class="mt-5">
            <!-- <input type="text" id="search" v-model="search" class="form-control" placeholder="Sök..."> -->
            <input type="text" id="search" ref="search" @keyup="handleChange" class="form-control" placeholder="Sök...">
        </form>

        <div class="mt-2">
            <p>Sök efter: {{search}}</p>
            <p>Giltig: {{valid}}</p>
        </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            search: '',
            valid: false
        }
    },
    methods: {
        handleChange() {
            console.log(this.$refs.search)

            this.search = this.$refs.search.value

            if(this.$refs.search.value.length > 5)
                this.valid = true
            else
                this.valid = false
        }
    }
}
</script>

<style>

</style>