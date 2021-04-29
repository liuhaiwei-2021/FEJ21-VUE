<template>
  <div>
        <div :class="enabled ? 'text-success': 'text-danger'" style="font-size: 2.5rem;">Hans</div>
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

    }
}
</script>

<style>

</style>