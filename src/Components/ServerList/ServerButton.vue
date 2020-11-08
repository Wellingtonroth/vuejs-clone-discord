<template>
  <div class="serverbutton" :class="{'serverbutton-hasNotification' : hasNotification}">

  </div>
</template>

<script>
export default {
  props: {
    selected: Boolean,
    isHome: Boolean,
    hasNotification: Boolean,
    mentions: Number
  }
};
</script>

<style scoped lang="scss">
.serverbutton {
  display: flex;
  flex-shrink: 0;
  align-items: center;
  justify-content: center;
  width: 48px;
  height: 48px;
  margin-bottom: 8px;
  background-color: var(--primary);
  cursor: pointer;
  position: relative;
  border-radius: 50%;
  transition: .2s;

  &.active,
  &:hover {
    border-radius: 16px;
    background-color: var(--discord);
  }
}

.serverbutton-hasNotification {
  &::before {
    content: "";
    width: 9px;
    height: 9px;
    background-color: var(--white);
    position: absolute;
    left: -17px;
    top: calc(50% - 4.5px);
    border-radius: 50%;
    display: block;
  }
}
</style>
