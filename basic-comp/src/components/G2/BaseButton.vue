<script setup>
defineEmits(['clickMe'])
const prop = defineProps({
  buttonName: {
    type: String,
    // default: 'OK'
    require: true
  }
})
const num = 555
// console.log(prop.buttonName)
</script>

<template>
  <button class="button-color" @click="$emit('clickMe', $event)">
    {{ buttonName }}
  </button>
</template>

<style scoped>
.button-color {
  background-color: aqua;
}
</style>
