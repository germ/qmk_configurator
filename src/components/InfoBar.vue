<template functional>
  <transition name="fadelong" appear>
    <div v-if="props.msg.length" class="bottom-fixed">{{ props.msg }}</div>
  </transition>
</template>
<script>
export default {
  name: 'InfoBar',
  props: {
    msg: {
      type: String,
      required: true
    }
  }
};
</script>
<style scoped>
.bottom-fixed {
  position: fixed;
  z-index: 500;
  bottom: 0px;
  left: 0;
  width: 100%;
  text-align: center;
  background: #add8e6;
  color: #222;
  line-height: 250%;
  font-size: 150%;
  opacity: 0.8;
}

.fadelong-enter-active,
.fadelong-leave-active {
  transition: opacity 0.5s;
}

.fadelong-enter,
.fadelong-leave-to {
  opacity: 0;
}
</style>
