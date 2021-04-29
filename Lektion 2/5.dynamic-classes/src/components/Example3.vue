<template>
<div>
  <div :class="{'text-success': isActive}">Hans Mattin-Lassei</div>
  <div :class="[{'text-success': isActive}, 'bg-dark']">Hans Mattin-Lassei</div>
  <div :class="[isActive ? 'text-success':'text-danger', 'bg-dark', 'ps-5']">Hans Mattin-Lassei</div>
</div>

</template>

<script>
export default {
    data() {
        return {
            isActive: true
        }
    }
}
</script>

<style>

</style>