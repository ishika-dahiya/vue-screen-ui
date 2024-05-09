<template>
  <div
    class="job-recommendations bg-white ml-9 mt-3 mb-32 py-1 px-6 rounded-lg"
  >
    <div class="flex justify-between items-center mb-3">
      <p class="text-lg font-bold">{{ totalJobs }} jobs found</p>
      <div class="dropdown font-bold">
        <select v-model="selectedOption" class="select">
          <option
            v-for="(option, index) in dropdownOptions"
            :key="index"
            :value="option.value"
            class="text-lg"
          >
            {{ option.label }}
          </option>
        </select>
      </div>
    </div>
    <div class="grid grid-cols-1 gap-2">
      <div
        v-for="(job, index) in jobRecommendations"
        :key="index"
        class="relative border-2 border-gray-200 p-4 rounded-lg"
      >
        <div class="flex items-start">
          <div
            class="w-10 h-10 bg-gray-300 rounded-xl flex items-center justify-center mr-2"
            v-html="job.logo"
          ></div>
          <div class="flex-1">
            <p class="font-sans font-bold text-sm">{{ job.role }}</p>
            <p class="text-xs text-gray-400 font-bold">
              <span class="font-bold text-gray-600"> {{ job.company }} </span>
              &nbsp; {{ job.type }} • {{ job.employees }} employees •
              <span class="text-blue-500">{{ job.salary }}</span>
            </p>
            <div class="flex items-center mt-3.5">
              <div class="bg-gray-200 rounded-full p-1 flex items-center">
                <img
                  :src="
                    job.country === 'Australia'
                      ? 'https://upload.wikimedia.org/wikipedia/commons/thumb/8/88/Flag_of_Australia_%28converted%29.svg/188px-Flag_of_Australia_%28converted%29.svg.png'
                      : 'https://upload.wikimedia.org/wikipedia/commons/thumb/a/a9/Flag_of_the_United_States_%28DoS_ECA_Color_Standard%29.svg/188px-Flag_of_the_United_States_%28DoS_ECA_Color_Standard%29.svg.png'
                  "
                  :alt="job.country"
                  class="w-4 h-4 mr-1 rounded-full"
                />
                <span class="text-xs font-thin">{{ job.country }}</span>
              </div>
            </div>
          </div>
        </div>
        <div
          class="absolute bg-gray-200 rounded top-0 right-0 mt-4 mr-4 flex items-center"
        >
          <span class="material-symbols-outlined text-gray-500 p-1"
            >bookmark</span
          >
        </div>
        <div class="absolute bottom-0 right-0 mb-4 mr-4 flex items-center">
          <span class="text-sm text-gray-400 font-thin">{{
            job.postedTime
          }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "JobRecommendations",
  props: {
    totalJobs: {
      type: Number,
      required: true,
    },
    jobRecommendations: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      selectedOption: "relevant",
      dropdownOptions: [
        { label: "Relevant", value: "relevant" },
        { label: "All", value: "all" },
        { label: "Others", value: "others" },
      ],
    };
  },
};
</script>
