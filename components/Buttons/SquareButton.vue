<template>
  <button
    class="bg-transparent hover:bg-teal-500 text-teal-700 font-semibold hover:text-white py-2 px-4 border border-teal-500 hover:border-transparent rounded ml-2"
  >
    {{ name }}
  </button>
</template>

<script>
export default {
  props: ["name"]
};
</script>
