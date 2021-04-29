<template>
  <div>
        <div class="mb-2">
            <button class="btn btn-secondary me-2" @click="enable">Enable</button>
            <button class="btn btn-secondary me-2" @click="disable">Disable</button>
        </div>
        <div :class="{isCheckedClass: enabled}" style="font-size: 2.5rem;">Hans</div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            enabled: false
        }
    },
    methods: {
        enable() {
            this.enabled = true
        },
        disable() {
            this.enabled = false
        }
    }
}
</script>

<style>
.isCheckedClass {
    color: green
}
</style>