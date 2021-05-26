<template>
  <Layout>
    <Head />
    <Setting />

    <Content>
      <Nuxt />
    </Content>
    <div
      style="
        height: 1px;
        background: linear-gradient(90deg, rgba(90, 196, 190, 0) 0%, rgb(255 255 255) 50%, rgba(194, 0, 251, 0) 100%);
      "
    />
    <Foot />
  </Layout>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'

import { Layout } from 'ant-design-vue'
import Setting from '@/components/Setting.vue'

const { Content } = Layout

@Component({
  components: {
    Layout,
    Content,
    Setting
  }
})
export default class Default extends Vue {}
</script>

<style lang="less">
.ant-layout {
  min-height: 100vh;
}
.ant-layout-content {
  background-image: url('@/assets/background/background.jpg');
  background-size: cover;
  min-height: calc(100vh - 64px - 82px);
}

// footer {
//   width: 100%;
//   height: 100px;
//   position: absolute;
//   bottom: 0;
//   left: 0;
//   background: #333;
// }
</style>
