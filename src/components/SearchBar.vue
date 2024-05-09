<template>
  <div class="bg-white rounded-lg flex items-center justify-between px-2 py-1">
    <div class="grid grid-cols-12 gap-2 flex-1">
      <div class="col-span-5 input flex items-center gap-2">
        <span class="material-symbols-outlined"> search </span>
        <div class="flex-1">
          <span class="font-sans text-sky-800 font-semibold bg-gray-100 rounded-xl py-1 px-1  bg--100">{{ searchInput }}
            <span class="material-symbols-outlined text-gray-400 cursor-pointer text-xs"> clear </span>
          </span>
        </div>
        <span class="material-symbols-outlined cursor-pointer"> expand_more </span>
      </div>
      <label class="col-span-5 input flex items-center gap-2 ">
        <span class="material-symbols-outlined"> location_on </span>
        <input type="text" placeholder="location" class="flex-1" />
        <span class="material-symbols-outlined cursor-pointer"> expand_more </span>
      </label>
      <div class="col-span-2 flex items-center justify-end gap-2">
        <button class="btn btn-light-outline bg-white px-2">
          <span class="material-symbols-outlined"> tune </span>
          Filters
        </button>
        <button class="btn bg-blue-700 text-white">Search</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  data() {
    return {
      searchInput: "Design",
    };
  },

};
</script>
