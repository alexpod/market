<script lang="ts" setup>
interface Props {
  color?: 'primary' | 'secondary' | 'grayscale' | 'error'
  decoration?: 'default' | 'outline' | 'none'
  size?: 'L' | 'M' | 'S'
  disabled?: boolean
}

const props = defineProps<Props>()
const {
  color = 'primary',
  decoration = 'default',
  size = 'M',
  disabled = false
} = props
</script>

<template lang="pug">
  button
    leftIcon
</template>

<style lang="scss" scoped>

</style>