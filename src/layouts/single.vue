<template>
  <div class="all-background">
    <Nuxt />
    <div
      style="
        height: 1px;
        background: linear-gradient(90deg, rgba(90, 196, 190, 0) 0%, rgb(156 156 156) 50%, rgba(194, 0, 251, 0) 100%);
      "
    />
    <Foot />
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'

@Component({})
export default class Single extends Vue {}
</script>

<style lang="less">
.all-background {
  background: #27262c;
}
</style>
