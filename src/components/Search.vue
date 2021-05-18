<template>
  <div class="bg-gray-800 body-font text-gray-100">
    <div class="container px-5 py-16 mx-auto h-full">
      <!-- <div class="flex justify-end items-center px-4 space-x-2">
        <span class="text-sm text-gray-800 dark:text-gray-500">Light</span>
        <div>
          <input
            type="checkbox"
            name=""
            id="toggle"
            class="hidden"
            v-model="checkbox"
            v-on:input="checkbox != checkbox"
          />
          <label for="toggle">
            <div
              class="w-9 h-5 flex items-center bg-gray-300 rounded-full p-1 dark:bg-gray-600"
            >
              <div
                class="toggle-dot w-4 h-4 bg-white rounded-full shadow-md transform duration-300 ease-in-out"
              ></div>
            </div>
          </label>
        </div>
        <span class="text-sm text-gray-400 dark:text-gray-100">Dark</span>
      </div> -->
      <div class="flex flex-col text-center w-full mb-8">
        <h1
          class="sm:text-5xl text-4xl font-bold title-font mb-4 text-gray-100"
        >
          devJobs
        </h1>
        <p
          class="lg:w-2/3 mx-auto leading-relaxed font-semibold text-lg text-gray-300"
        >
          Platform for searching your next dream job &#128640;
        </p>
      </div>
      <div
        class="flex mb-4 lg:w-5/6 w-full sm:flex-row flex-col mx-auto px-4 sm:space-x-4 sm:space-y-0 space-y-4 sm:px-0"
      >
        <div class="relative flex-grow w-full">
          <input
            type="text"
            v-model="search"
            class="w-full bg-gray-800 bg-opacity-40 rounded border border-gray-700 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-900 focus:bg-transparent text-base outline-none text-gray-100 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out"
            placeholder="Filter by title, company name..."
          />
        </div>
      </div>
      <div class="p-4 flex flex-wrap items-center justify-left bg-gray-800">
        <CompanyCard :jobs="job" v-for="job in filteredJobs" :key="job.id" />
      </div>
    </div>
  </div>
</template>

<script>
import CompanyCard from "./CompanyCard.vue";
import axios from "axios";

export default {
  components: { CompanyCard },
  name: "Search",
  data: () => ({
    search: "",
    checkbox: false,
    jobs: [],
  }),

  methods: {
    fetchApi() {
      axios
        .get("http://localhost:8080/positions.json")
        //.then((response) => (this.jobs = response.data))
        .then((response) => console.log(response))
        .catch((e) => console.log(e));
    },
  },
  mounted() {
    this.fetchApi();
  },
  computed: {
    filteredJobs() {
      return this.jobs.filter((job) =>
        job.title.toLowerCase().includes(this.search.toLowerCase())
      );
    },
  },
};
</script>

<style scoped>
</style>
