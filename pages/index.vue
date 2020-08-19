<template>
  <div>
    <Header header="BEEP" v-bind:username="username" />
    <div class="flex flex-row">
      <div class="w-1/6">
        <UserContainer v-bind:name="username" />
      </div>
      <div class="5/6 bg-white shadow-lg mx-6">
        <Promotions v-bind:promotions="promotions" v-bind:image="image" />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "../components/Header";
import PromotionCards from "../components/Cards/PromotionCards";
import Promotions from "../components/Promotions";
import UserContainer from "../components/User/UserContainer";
export default {
  components: {
    Header,
    PromotionCards,
    Promotions,
    UserContainer
  },
  async asyncData({ $axios }) {
    let response = await $axios.get(
      `https://dev.beepbeep.tech/v1/sample_customer`
    );
    console.log(response.data);
    return {
      image: {
        imageUrl: "https://unsplash.com/photos/UcI5OAPD820/download?force=true",
        imageAlt: "image"
      },
      promotions: response.data.promotions,
      username: response.data.name
    };
  }
};
</script>
