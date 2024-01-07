<script lang="ts" setup>
import { Container } from "@/shared/container/index.ts"
import { Logotype } from "@/shared/logo/index.ts"
import { Button } from "@/shared/button/index.ts"
</script>

<template lang="pug">
.header
  Container.header__container
    Logotype
    Button
    p Header
</template>

<style lang="scss" scoped>
.header{
  box-shadow: var(--shadow-default-s);
  &__container {
    display: flex;
    align-items: center;
    min-height: 72px;
  }
}
</style>