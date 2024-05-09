<template>
  <div class="bg-white rounded-lg flex items-center justify-between p-2">
    <!-- <div class="grid grid-cols-12 gap-2 flex-1 p-1">
      <div class="col-span-5 input flex items-center gap-2">
        <span class="material-symbols-outlined"> search </span>
        <div class="flex-1">
          <span class="font-sans text-sky-800 font-semibold bg-gray-100 rounded-xl py-1 px-1  bg--100">{{ searchInput }}
            <span class="material-symbols-outlined text-gray-400 cursor-pointer text-xs"> clear </span>
          </span>
        </div>
        <span class="material-symbols-outlined cursor-pointer"> expand_more </span>
      </div>
      <div class="h-10 w-px bg-gray-300"></div>
      <label class="col-span-5 input flex items-center gap-2">
        <span class="material-symbols-outlined"> location_on </span>
        <input type="text" placeholder="location" class="flex-1" />
        <span class="material-symbols-outlined cursor-pointer"> expand_more </span>
      </label>
       <div class="col-span-1"></div> 
      <div class="col-span-2 flex items-center justify-around gap-2">
        <button class="btn btn-light-outline bg-white px-2">
          <span class="material-symbols-outlined"> tune </span>
          Filters
        </button>
        <button class="btn bg-blue-700 text-white">Search</button>
      </div>
    </div> -->

    <!-- First Dropdown -->
    <label class="flex items-center flex-1">
      <span class="material-symbols-outlined px-2"> search </span>
      <span v-if="selectedOption" class="font-sans text-sky-800 font-semibold bg-gray-100 rounded-xl py-1 px-1 bg--100">
        {{ selectedOption }}
        <span class="material-symbols-outlined text-gray-400 cursor-pointer text-xs" @click="clearSelection">clear</span>
      </span>
      <select v-else class="select w-full" v-model="selectedOption">
        <option disabled selected>type here</option>
        <option>Design</option>
        <option>Option 2</option>
        <option>Option 3</option>
      </select>
    </label>
    <span class="material-symbols-outlined">expand_more</span>
    <!-- Vertical Divider -->
    <div class="h-8 border-r-2 border-gray-300 mx-4"></div>

    <!-- Second Dropdown -->
    <label class="flex items-center flex-1">
      <span class="material-symbols-outlined text-gray-600"> location_on </span>
      <select class="select w-full">
        <option selected >Location</option>
        <option>Option 1</option>
        <option>Option 2</option>
        <option>Option 3</option>
      </select>
    </label>
    <div class=" flex items-center justify-around gap-2 m-1">
        <button class="btn btn-light-outline bg-white px-2">
          <span class="material-symbols-outlined"> tune </span>
          Filters
        </button>
        <button class="btn bg-blue-700 text-white">Search</button>
      </div>
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  data() {
    return {
      selectedOption: "",
    };
  },
  methods: {
    clearSelection() {
      this.selectedOption = "";
    },
  },
};
</script>
