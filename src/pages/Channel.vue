<template>
  <Layout>
    <template v-slot:head>
      <!-- <Menu /> -->
      菜单
    </template>
    <template v-slot:left>
      <Aside />
    </template>
    <template v-slot:main>
      <!-- <Main /> -->
      主区域
    </template>
  </Layout>
</template>

<script>
import Layout from "@/components/Layout";
import Aside from "@/components/Aside";
export default {
  components: {
    Layout,
    Aside,
  },
};
</script>

<style lang="less" scoped></style>
