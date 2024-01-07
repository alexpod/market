<script lang="ts" setup>

interface Props {
  tagName: 'p' | 'h1' | 'h2' | 'h3' | 'h4' | 'h5'
  bold?: boolean
  size?: 'xs' | 's' | 'm' | 'l' | 'xl'

}
  
const props = defineProps<Props>()

</script>

<template lang="pug">
component(
  :is="props.tagName"
  :class="['typography', size ? `size_${size}` : '', bold ? 'bold' : '', `tag_${tagName}`]"
)
  slot
</template>


<style lang="scss" scoped>
.size {
  &_xs { font-size: 0.75rem; }
  &_s { font-size: 1rem; }
  &_m { font-size: 1.125rem; }
  &_l { font-size: 1.5rem; }
  &_xl { font-size: 2.25rem; }
}
.tag {
  &_h1 { font-size: 64px; }
  &_h2 { font-size: 48px; }
  &_h3 { font-size: 36px; }
  &_h4 { font-size: 24px; }
  &_h5 { font-size: 18px; }
}
@media screen and (max-width: 768px) {
.size {
  &_xs { font-size: 8px; }
  &_s { font-size: 12px; }
  &_m { font-size: 14px; }
  &_l { font-size: 20px; }
  &_xl { font-size: 32px; }
}
.tag {
  &_h1 { font-size: 48px; }
  &_h2 { font-size: 36px; }
  &_h3 { font-size: 24px; }
  &_h4 { font-size: 18px; }
  &_h5 { font-size: 16px; }
} 
}
</style>