<template>
  <header class="bg-teal-600 mb-4">
    <div
      class="container mx-auto px-4 flex flex-row justify-between items-center"
    >
      <div>
        <div class="flex flex-row items-center">
          <p
            class="text-3xl text-center md:text-4xl m-2 text-white antialiased"
          >
            {{ header }}
          </p>
          <SearchBar />
        </div>
      </div>
      <div class="flex flex-row items-center">
        <UserIcon />
        <p class="text-white">{{ username }}</p>
      </div>
    </div>
  </header>
</template>

<script>
import UserIcon from "../Icons/UserIcon";
import SearchBar from "../InputField/SearchBar";
export default {
  components: { UserIcon, SearchBar },
  props: ["header", "username"]
};
</script>
