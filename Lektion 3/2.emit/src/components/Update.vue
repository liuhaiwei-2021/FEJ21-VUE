<template>
  <div class="col">
      <div class="card h-100">
        <div class="card-header bg-primary text-white py-4 text-center">
          <h2>Sign Up</h2>
        </div>
        <div class="card-body p-4">
          <form @submit.prevent="update">
            <div class="row mb-3">
              <div class="col">
                  <label class="form-label" for="form1">Name:</label>
                  <input type="text" id="form1" class="form-control" v-model="newName" />
              </div>
              <div class="col">
                  <label class="form-label" for="form1">Age:</label>
                  <input type="number" id="form1" class="form-control" v-model="newAge" />
              </div>
            </div>
              <div class="mb-4">
                  <label class="form-label" for="form1">Email:</label>
                  <input type="email" id="form1" class="form-control" v-model="newEmail" />
              </div>
              <button class="btn btn-outline-primary btn-block">Update</button>
          </form>

        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: ['name', 'age', 'email'],
  data() {
    return {
      newName: this.name,
      newAge: this.age,
      newEmail: this.email
    }
  },
  methods: {
    update() {

      let user = {
        name: this.newName,
        age: this.newAge,
        email: this.newEmail
      }

      this.$emit('update-user', user)
    }
  }
}
</script>

<style>

</style>