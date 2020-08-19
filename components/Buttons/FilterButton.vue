<template>
  <button
    v-if="color === 'teal'"
    class="bg-transparent hover:bg-teal-500 text-teal-700 font-semibold hover:text-white py-2 px-4 border border-teal-500 hover:border-transparent rounded-full mx-2"
  >
    {{ name }}
  </button>
  <button
    v-else-if="color === 'red'"
    class="bg-transparent hover:bg-red-500 text-red-700 font-semibold hover:text-white py-2 px-4 border border-red-500 hover:border-transparent rounded-full mx-2"
  >
    {{ name }}
  </button>
  <button
    v-else-if="color === 'blue'"
    class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border border-blue-500 hover:border-transparent rounded-full mx-2"
  >
    {{ name }}
  </button>
</template>

<script>
export default {
  props: ["name", "color"]
};
</script>
