<template>
  <div class="flex flex-col items-center">
    <div class="w-10/12 sm:w-8/12 p-2">
      <img
        src="https://demos.creative-tim.com/tailwindcss-starter-project/_next/static/images/team-1-800x800-fa5a7ac2c81a43925586ea85f2fea332.jpg"
        alt="profile picture"
        class="shadow rounded-full max-w-full h-auto align-middle border-none"
      />
    </div>
    <h1>{{ name }}</h1>
    <div class="flex items-center">
      <div class="container flex flex-col p-2 items-start mt-8">
        <h1>Account Information</h1>
        <h1>Account Settings</h1>
        <h1>My Purchase</h1>
        <h1 class="text-teal-500">My Promotions</h1>
        <h1>Help & FAQ</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["name"]
};
</script>
