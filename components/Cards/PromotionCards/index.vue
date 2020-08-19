<template>
  <div class="w-1/3 h-auto mb-4 px-12 sm:w-1/3 md:1/4">
    <div class="bg-white h-auto shadow-md p-6 cursor-pointer">
      <img class="object-contain" :src="image.imageUrl" :alt="image.imageAlt" />
      <div v-if="type === 'discount'" class="w-auto inline-block">
        <div
          class="border-solid border border-opacity-50 mt-2 border-red-600 p-1 rounded-sm"
        >
          <p class="text-red-600 text-xs">Promotion</p>
        </div>
      </div>
      <div v-else class="w-auto inline-block">
        <div
          class="border-solid border border-opacity-50 mt-2 border-red-600 bg-red-600 p-1 rounded-sm"
        >
          <p class="text-white text-xs">Redeem</p>
        </div>
      </div>
      <p class="underline">Additional details:</p>
      <p>Quantity: {{ quantity }}</p>
      <p v-if="discount">Discount: {{ discount }}</p>
      <p v-else class="text-white">"\n"</p>
      <div
        class="flex items-center justify-center border-solid border mt-2 rounded border-red-500 bg-red-500"
      >
        <h4 class="p-1 text-white">{{ title }}</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["title", "image", "discount", "type", "quantity"]
};
</script>
