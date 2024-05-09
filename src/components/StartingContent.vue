<template>
  <div class="main-content p-8 rounded-t-3xl">
    <div class="font-sans px-9 py-4">
      <h1 class="text-4xl font-bold mb-2 max-w-lg">
      Find your next career today within minutes.
    </h1>
    <h4 class="text-gray-600 font-medium text-sm max-w-lg" >
      Introducing our cutting-edge UI Kit, a game-changer for designers and
      developers alike! Our UI Kit empowers you to create stunning user
      interfaces.
    </h4>
    </div>
    <SearchBar></SearchBar>
  </div>
</template>

<script>
import SearchBar from "@/components/SearchBar.vue";

export default {
  name: "StartingContent",
  components: {
    SearchBar,
  },
};
</script>

<style scoped>
.main-content {
  flex: 1;
  margin-right: 20px;
  /* background-image: linear-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)), url('/src/assets/img/background.jpg'); */
  background-image: url('/public/img/background.jpg');
  background-size: cover;
  background-position: center;
}
</style>
