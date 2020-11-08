<template>
  <div class="item" :class="{ active: isActive }" @click="handleClick">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    isActive: {
      type: Boolean, //约束该属性的类型是boolean
      // required: true,  //约束该属性必须要传递
      default: false,
    },
  },
  methods: {
    handleClick() {
      this.$emit("active");
    },
  },
};
</script>

<style lang="less" scoped>
.active {
  background: #e7e7e7;
}
.item {
  cursor: pointer;
  width: 100%;
  height: 100%;
  transition: 0.2s;
}
.item:hover {
  background: #f4f4f4;
}
</style>
