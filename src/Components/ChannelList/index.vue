<template>
  <div class="container">
    <div class="category">
      <div>Canais de Texto</div>
      <div class="category-icon">
        <AddCategoryIcon :size="21" />
      </div>
    </div>
    <ChannelButton selected channelName="chat-livre" />
    <ChannelButton channelName="vue-js" />
    <ChannelButton channelName="jogos" />
    <ChannelButton channelName="csgo" />
    <ChannelButton channelName="reac-js" />
  </div>
</template>

<script>
  import AddCategoryIcon from "vue-material-design-icons/Plus";
  import ChannelButton from "./ChannelButton";

  export default {
    components: {
      ChannelButton,
      AddCategoryIcon
    }
  }
</script>

<style lang="scss" scoped>
  .container {
    grid-area: CL;
    display: flex;
    flex-direction: column;
    padding: 24px 10px 0 16px;
    background-color: var(--secondary)
  }

  .category {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 6px;
    color: var(--grey);
    font-size: 12px;
    font-weight: 500;
    text-transform: uppercase;

    .category-icon {
      color: var(--symbol);
      cursor: pointer;
    }
  }

</style>
