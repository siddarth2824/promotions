<template>
  <div class="container mx-auto">
    <div class="w-full h-auto mb-4 px-12 sm:w-2/4 md:1/4 p-2">
      <h1 class="font-bold text-2xl mb-2">My Promotions</h1>
    </div>
    <div
      class="container w-full mb-4 px-16 flex flex-row items-center justify-center"
    >
      <p class="mr-2">Add Vouchers</p>
      <InputForm />
      <SquareButton name="Redeem" />
    </div>
    <div class="container w-full mb-4 px-16 flex flex-row">
      <RoundButton name="All Promotions" color="teal" />
      <RoundButton name="Discounts" color="red" />
      <RoundButton name="Free Redeems" color="blue" />
    </div>
    <div class="flex flex-wrap ">
      <PromotionCards
        v-bind:key="promotion.title"
        v-for="promotion in promotions"
        :title="promotion.title"
        :discount="promotion.discount"
        :type="promotion.type"
        :quantity="promotion.quantity"
        v-bind:image="image"
      />
    </div>
  </div>
</template>

<script>
import PromotionCards from "./Cards/PromotionCards";
import InputForm from "./InputField/InputForm";
import RoundButton from "./Buttons/RoundButton";
import SquareButton from "./Buttons/SquareButton";
export default {
  components: {
    PromotionCards,
    InputForm,
    RoundButton,
    SquareButton
  },
  props: ["promotions", "image"],
  methods: {
    changeFilter(filter) {}
  }
};
</script>
