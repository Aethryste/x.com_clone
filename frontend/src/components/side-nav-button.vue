<script lang="ts">

interface sideNavButton {
  icon: string;
  displayText: string;
  isFirst: boolean;
}

export default {
  name: 'sideNavButton',
  props: {
    icon: {
      type: String,
      required: true
    },
    displayText: {
      type: String,
      required: true
    },
    isFirst: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<template>
  <div class="side-nav-button-container">
    <div class="button-hover-container">
      <span class="navButton-icon" :style="{background: 'url(src/assets/icon/' + icon + ')', filter: 'invert(1)'}"/>
      <span class="navButton-label" v-if="!isFirst">{{ displayText }}</span>
    </div>
  </div>
</template>

<style scoped>
.side-nav-button-container {
  width: 100%;
  cursor: pointer;
  &:hover .button-hover-container {
    background: rgba(255,255,255,0.1);
  }
  .button-hover-container {
    border-radius: 2.2em;
    width: fit-content;
    height: 30px;
    padding: 10px;
    display: flex;
    flex-direction: row;
    margin: 5px;
    transition: 200ms;
    .navButton-icon {
      display: flex;
      width: 26px;
      height: 26px;
      margin: 3px;
    }
    .navButton-label {
      display: flex;
      height: fit-content;
      width: fit-content;
      font-size: 1.3em;
      margin: auto 15px auto 15px;
      color: rgb(255, 255, 255, 0.9)
    }
  }
}
</style>