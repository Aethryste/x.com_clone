<script lang="ts">
import sideNavButton from "./side-nav-button.vue";
export default {
  name: 'sideNav',
  components: {
    sideNavButton
  },
  data() {
    return {
      navButtons: [
        {
          name: 'logo',
          icon: 'icon-x.svg',
          displayText: ''
        },
        {
          name: 'home',
          icon: 'icon-home.svg',
          displayText: 'Home'
        },
        {
          name: 'explore',
          icon: 'icon-search.svg',
          displayText: 'Explore'
        },
        {
          name: 'notifications',
          icon: 'icon-bell.svg',
          displayText: 'Notifications'
        },
        {
          name: 'messages',
          icon: 'icon-mail.svg',
          displayText: 'Messages'
        },
        {
          name: 'lists',
          icon: 'icon-list.svg',
          displayText: 'Lists'
        },
        {
          name: 'bookmarks',
          icon: 'icon-bookmark.svg',
          displayText: 'Bookmarks'
        },
        {
          name: 'communities',
          icon: 'icon-group.svg',
          displayText: 'Communities'
        },
        {
          name: 'premium',
          icon: 'icon-x.svg',
          displayText: 'Premium'
        },
        {
          name: 'profile',
          icon: 'icon-user.svg',
          displayText: 'Profile'
        },
        {
          name: 'more',
          icon: 'icon-more.svg',
          displayText: 'More'
        }
      ]
    }
  }
}
</script>

<template>
  <header class="side-nav-container">
    <div class="buttons-container">
      <side-nav-button v-for="(button, index) in navButtons"
                       :key="button.name"
                       :icon="button.icon"
                       :display-text="button.displayText"
                       :is-first="index === 0"
      />
      <button class="button-post">Post</button>
    </div>
  </header>
</template>

<style scoped>
.side-nav-container {
  border-right: 1px solid rgba(255, 255, 255, 0.2);
  width: 31%;
  min-height: 100%;
  margin: 0;
  top: 0;
  position: relative;
  display: flex;
  flex-basis: auto;
  flex-shrink: 0;
  flex-direction: column;
  .buttons-container {
    width: 275px;
    margin: auto 0 auto auto;
    justify-content: start;
    flex-grow: 2;
    .button-post {
      font-family: ChirpBold, sans-serif;
      font-size: 1.05em;
      color: white;
      width: 85%;
      height: 52px;
      background: rgb(29, 155, 240);
      margin: 16px auto 16px 5px;
      border: none;
      border-radius: 2em;
      cursor: pointer;
    }
  }
}
</style>