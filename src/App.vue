<script setup lang="ts">
import Banner from "./widgets/Banner.vue";
import PersonData from "./widgets/PersonData.vue";
import ContactInfo from "./widgets/ContactInfo.vue";
import SocialNetworks from "./widgets/SocialNetworks.vue";
</script>

<template>
  <div class="my-page">
    <Banner />
    <PersonData />
    <ContactInfo />
    <SocialNetworks />
  </div>
</template>

<style lang="scss">
.my-page {
  margin: 0 auto;
  width: 100%;
}
</style>
