<template>
  <div class="side-view">
    <div class="subscribe-box bg-blue-50 p-7 my-6 mx-6 rounded-lg">
      <span class="material-symbols-outlined text-blue-700 mb-5 ml-4"> mail </span>
      <h2 class="text-xl font-semibold">Subscribe for updates</h2>
      <p class="mb-4 text-sm text-blue-900">
        Turn on this job alert so you don't miss out on openings that could fit your needs
      </p>
      <input
        type="email"
        placeholder="enter email"
        class="input shadow-md w-full mb-2"
      />
      <button class="btn bg-blue-700 text-white w-full">Subscribe</button>
    </div>
    <div class="bg-white px-7 rounded-lg">
      <h2 class="text-lg font-sans font-bold mb-2">Related careers</h2>
      <div class="related-careers flex flex-wrap px-0.5">
        <button
          v-for="(career, index) in relatedCareers"
          :key="index"
          class="btn btn-custom-outline btn-white btn-sm mb-2 mr-1"
        >
          <div class="text-sm">{{ career.name }}</div>
          <div class="bg-gray-200 rounded text-xs px-0">
            {{ career.positions }}
          </div>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SideView",
  props: {
    relatedCareers: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.side-view {
  width: 400px;
}

.related-careers {
  display: flex;
  flex-wrap: wrap;
}

.btn-custom-outline {
  border-color: #e7e7e9e6;
  background-color: white;
}
</style>
