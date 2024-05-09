<template>
  <div id="app" class="mx-52 my-24">
    <StartingContent class="w-full"></StartingContent>
    <div class="bg-white flex flex-row justify-between w-full rounded-b-3xl">
      <JobRecommendations
        :totalJobs="totalJobs"
        :jobRecommendations="jobRecommendations"
        class="flex-1 w-full"
      ></JobRecommendations>
      <SideView :relatedCareers="relatedCareers" class="w-full"></SideView>
    </div>
  </div>
</template>

<script>
import StartingContent from "@/components/StartingContent.vue";
import SideView from "@/components/SideView.vue";
import JobRecommendations from "@/components/JobRecommendations.vue";

export default {
  name: "MainLayout",
  components: {
    StartingContent,
    SideView,
    JobRecommendations,
  },
  data() {
    return {
      totalJobs: 250,
      jobRecommendations: [
        {
          logo: '<img src="https://cdn-icons-png.freepik.com/256/11024/11024424.png?semt=ais_hybrid" />',
          role: "Product Design Lead",
          company: "GitHub",
          type: "Full Time",
          employees: "50-100",
          salary: "190-21K AUD",
          country: "Australia",
          postedTime: "10 hours ago",
        },
        {
          logo: '<img src="https://cdn-teams-slug.flaticon.com/google.jpg" />',
          role: "Product Designer",
          company: "Google",
          type: "Full Time",
          employees: "50-100",
          salary: "180-200K USD",
          country: "United States",
          postedTime: "10 hours ago",
        },
        {
          logo: '<img src="https://e1.pngegg.com/pngimages/481/966/png-clipart-macos-app-icons-evernote-thumbnail.png"/>',
          role: "Product Design Manager",
          company: "Evernote",
          type: "Full Time",
          employees: "50-100",
          salary: "120-140K AUD",
          country: "Australia",
          postedTime: "10 hours ago",
        },
        {
          logo: '<img src="https://w7.pngwing.com/pngs/54/524/png-transparent-figma-app-logo-tech-companies-thumbnail.png" />',
          role: "Design Head",
          company: "Figma",
          type: "Full Time",
          employees: "50-100",
          salary: "250-320K AUD",
          country: "United States",
          postedTime: "10 hours ago",
        },
      ],
      relatedCareers: [
        { name: "UI Designer", positions: 24 },
        { name: "UX Researcher", positions: 56 },
        { name: "Graphic designer", positions: 109 },
        { name: "Web designer", positions: 145 },
        { name: "Product designer", positions: 78 },
        { name: "Webflow designer", positions: 45 },
      ],
    };
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
