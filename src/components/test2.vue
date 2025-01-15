<template>
  <div>
    <button @click="isOpen = !isOpen">Toggle Dropdown</button>
    <transition name="dropdown">
      <div v-show="isOpen" class="dropdown-content">
        <div>Option 1</div>
        <div>Option 2</div>
        <div>Option 3</div>
      </div>
    </transition>
  </div>
</template>
 
<script>
export default {
    name: "CommonAnimation",
  data() {
    return {
      isOpen: false // 控制下拉内容是否显示
    };
  }
}
</script>
 
<style scoped>
.dropdown-content {
  max-height: 0; /* 初始高度为0 */
  overflow: hidden; /* 隐藏超出部分 */
  transition: max-height 0.3s ease; /* 添加过渡效果 */
}
.dropdown-enter-active, .dropdown-leave-active {
  max-height: 200px; /* 或者根据内容实际高度设置，确保有足够的空间展开 */
}
.dropdown-enter, .dropdown-leave-to {
  max-height: 0; /* 进入和离开时的目标高度 */
}
</style>
