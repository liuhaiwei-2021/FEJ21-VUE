<template>
  <div>
      <form>
          <div class="form-group">
              <input type="text" placeholder="Ange förnamn..." v-model="firstName" class="form-control">
          </div>
          <div class="form-group mt-3">
              <input type="text" placeholder="Ange efternamn..." v-model="lastName" class="form-control">
          </div>
      </form>
      <div class="mt-3">Fullständigt namn: {{ firstName }} {{ lastName }}</div>
      <div class="mt-3">Fullständigt namn: {{ fullName }}</div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            firstName: 'Hans',
            lastName: 'Mattin-Lassei'
        }
    },
    computed: {
        fullName() {
            return `${this.firstName} ${this.lastName}`
        }
    }
}
</script>

<style>

</style>