<template>
  <div class="container">
    <ServerButton isHome/>

    <div class="separator">
      <ServerButton :mentions="3" />
      <ServerButton hasNotification />
      <ServerButton :mentions="32" hasNotification />
      <ServerButton :mentions="4"/>
      <ServerButton hasNotification/>
    </div>
  </div>
</template>

<script>
import ServerButton from "./ServerButton";

export default {
  components: {
    ServerButton
  }
};

</script>

<style scoped lang="scss">

.container {
  grid-area: SL;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: var(--tertiary);
  padding: 11px 0;
  max-height: 100vh;
}

.separator {
  width: 48px;
  border-bottom: solid 2px var(--quaternary);
  margin-bottom: 8px;
}

</style>
