<script setup>
import { ref } from "vue";
import WebLink from "./WebLink.vue";
import SocialLink from "./SocialLink.vue";
import Discord from "./Discord.vue";
import WebLinks from "./WebLinks.vue";

const user = ref({
  firstName: "Christopher",
  lastName: "Finster",
  image: "https://source.unsplash.com/featured/250x350",
});

const sites = ref([
  {
    siteName: "twitch",
    siteUrl: "https://www.twitch.tv/",
    siteImage:
      "https://1000logos.net/wp-content/uploads/2018/08/Twitch-emblem-500x281.jpg",
  },
  {
    siteName: "youtube",
    siteUrl: "https://www.youtube.com/",
    siteImage:
      "https://1000logos.net/wp-content/uploads/2021/04/YouTube-logo-500x281.png",
  },
  {
    siteName: "twitch",
    siteUrl: "https://www.twitch.tv/",
    siteImage:
      "https://1000logos.net/wp-content/uploads/2018/08/Twitch-emblem-500x281.jpg",
  },
  {
    siteName: "youtube",
    siteUrl: "https://www.youtube.com/",
    siteImage:
      "https://1000logos.net/wp-content/uploads/2021/04/YouTube-logo-500x281.png",
  },
  {
    siteName: "youtube",
    siteUrl: "https://www.youtube.com/",
    siteImage:
      "https://1000logos.net/wp-content/uploads/2021/04/YouTube-logo-500x281.png",
  },
  {
    siteName: "twitch",
    siteUrl: "https://www.twitch.tv/",
    siteImage:
      "https://1000logos.net/wp-content/uploads/2018/08/Twitch-emblem-500x281.jpg",
  },
  {
    siteName: "youtube",
    siteUrl: "https://www.youtube.com/",
    siteImage:
      "https://1000logos.net/wp-content/uploads/2021/04/YouTube-logo-500x281.png",
  },
  {
    siteName: "twitch",
    siteUrl: "https://www.twitch.tv/",
    siteImage:
      "https://1000logos.net/wp-content/uploads/2018/08/Twitch-emblem-500x281.jpg",
  },
]);

const socialLinks = ref([
  {
    siteName: "LinkedIn",
    siteUrl: "https://www.linkedin.com/in/christopher-finster/",
    showStatus: false,
    active: false,
  },
  {
    siteName: "Facebook",
    siteUrl: "https://www.facebook.com/",
    showStatus: false,
    active: false,
  },
  {
    siteName: "Instagram",
    siteUrl: "https://www.instagram.com/",
    showStatus: false,
    active: false,
  },
  {
    siteName: "Twitter",
    siteUrl: "https://twitter.com/",
    showStatus: false,
    active: false,
  },
  {
    siteName: "Xbox Live",
    siteUrl: "https://www.xbox.com/en-US/live",
    showStatus: true,
    active: false,
  },
  {
    siteName: "Playstation Network",
    siteUrl: "https://www.playstation.com/en-us/network/",
    showStatus: true,
    active: true,
  },
]);

const discordServers = ref([
  {
    embedSrc: "https://discord.com/widget?id=340337686059548672&theme=dark",
  },
  {
    embedSrc: "https://discord.com/widget?id=267111225245040641&theme=dark",
  },
]);
</script>

<style scoped>
.user-info-left {
  /* width: 250px; */
}
.user-image-container {
  height: 350px;
  width: 250px;
  background-color: darkgray;
  border-radius: 40px;
  border: 1px black;
  overflow: hidden;
  box-shadow: 0 0 7px 7px rgba(0, 0, 0, 0.4);
}

.user-image {
  width: 250px;
}

.user-name-container {
  padding-block: 10px;
}

.user-name {
  color: #d6662b;
}

.link {
  color: white;
}

.online-status {
  width: 15px;
  height: 15px;
  border-radius: 50%;
  border: 1px solid black;
  background-color: greenyellow;
}

.web-links-wrapper {
  border-radius: 30px;
  border: 1px solid black;
  padding: 20px 10px;
}

.web-link-header {
  color: #d6662b;
  padding-left: 15px;
  margin-bottom: 5px;
}

.add-social-modal {
  background-color: gray;
  width: 100%;
}
</style>

<template>
  <!-- Make User component -->
  <section class="user-section uk-margin-bottom">
    <!-- Make user component -->
    <div
      class="user-info-container uk-flex uk-flex-center uk-child-width-1-2 uk-width-1-1"
    >
      <div class="user-info-left uk-flex uk-flex-column uk-flex-center">
        <div class="user-image-container uk-align-center">
          <img class="user-image" :src="user.image" alt="User Image" />
        </div>
        <div class="user-name-container uk-text-center uk-text-large">
          <span class="user-name">{{ user.firstName + " " + user.lastName }}</span>
        </div>
      </div>
      <div class="social-links-container uk-margin-left uk-child-width-1-1">
        <div class="user-container-right uk-text-center">
          <div class="user-link uk-margin-bottom">
            <SocialLink
              v-for="link in socialLinks"
              :showStatus="link.showStatus"
              :active="link.active"
              :siteName="link.siteName"
              :siteUrl="link.siteUrl"
              :embedSrc="link.embedSrc"
            />
          </div>
        </div>
      </div>
    </div>
  </section>

  <section>
    <WebLinks :sites="sites" />
  </section>

  <section id="discord-section">
    <div class="discord-servers-container">
      <Discord :servers="discordServers" />
    </div>
  </section>
</template>
