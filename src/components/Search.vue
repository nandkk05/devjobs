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
          class="lg:w-2/3 mx-auto leading-relaxed sm:font-semibold sm:text-lg text-gray-300"
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
            class="w-full bg-gray-800 bg-opacity-40 rounded-lg border border-gray-700 focus:border-indigo-500 focus:ring-2 focus:ring-indigo-900 focus:bg-transparent text-base outline-none text-gray-100 py-2 px-3 leading-8 transition-colors duration-200 ease-in-out"
            placeholder="Filter by title, company name..."
          />
        </div>
      </div>
      <div class="p-4 flex flex-wrap items-center justify-left bg-gray-800">
        <CompanyCard :jobs="job" v-for="job in filteredJobs" :key="job.id" />
        <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full" v-if="loading">
          <div
            class="shadow-xl bg-gray-900 border-gray-800 p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
          >
            <div class="flex items-center p-4 rounded-lg">
              <div
                class="w-16 h-16 bg-gray-700 border-gray-700 rounded-full mr-4 animate-pulse"
              ></div>
              <div class="sm:p-6 w-max">
                <div
                  class="mt-3 w-full bg-gray-700 text-gray-700 text-sm rounded animate-pulse"
                >
                  loading loading data ...........
                </div>
                <div
                  class="w-20 mt-1 bg-gray-700 text-gray-700 py-1 text-sm rounded animate-pulse"
                ></div>
                <div>
                  <a
                    class="mt-4 inline-flex items-center bg-indigo-900 text-indigo-900 rounded-lg animate-pulse"
                  >
                    loading data
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full" v-if="loading">
          <div
            class="shadow-xl bg-gray-900 border-gray-800 p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
          >
            <div class="flex items-center p-4 rounded-lg">
              <div
                class="w-16 h-16 bg-gray-700 border-gray-700 rounded-full mr-4 animate-pulse"
              ></div>
              <div class="sm:p-6 w-max">
                <div
                  class="mt-3 w-full bg-gray-700 text-gray-700 text-sm rounded animate-pulse"
                >
                  loading loading data ...........
                </div>
                <div
                  class="w-20 mt-1 bg-gray-700 text-gray-700 py-1 text-sm rounded animate-pulse"
                ></div>
                <div>
                  <a
                    class="mt-4 inline-flex items-center bg-indigo-900 text-indigo-900 rounded-lg animate-pulse"
                  >
                    loading data
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full" v-if="loading">
          <div
            class="shadow-xl bg-gray-900 border-gray-800 p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
          >
            <div class="flex items-center p-4 rounded-lg">
              <div
                class="w-16 h-16 bg-gray-700 border-gray-700 rounded-full mr-4 animate-pulse"
              ></div>
              <div class="sm:p-6 w-max">
                <div
                  class="mt-3 w-full bg-gray-700 text-gray-700 text-sm rounded animate-pulse"
                >
                  loading loading data ...........
                </div>
                <div
                  class="w-20 mt-1 bg-gray-700 text-gray-700 py-1 text-sm rounded animate-pulse"
                ></div>
                <div>
                  <a
                    class="mt-4 inline-flex items-center bg-indigo-900 text-indigo-900 rounded-lg animate-pulse"
                  >
                    loading data
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full" v-if="loading">
          <div
            class="shadow-xl bg-gray-900 border-gray-800 p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
          >
            <div class="flex items-center p-4 rounded-lg">
              <div
                class="w-16 h-16 bg-gray-700 border-gray-700 rounded-full mr-4 animate-pulse"
              ></div>
              <div class="sm:p-6 w-max">
                <div
                  class="mt-3 w-full bg-gray-700 text-gray-700 text-sm rounded animate-pulse"
                >
                  loading loading data ...........
                </div>
                <div
                  class="w-20 mt-1 bg-gray-700 text-gray-700 py-1 text-sm rounded animate-pulse"
                ></div>
                <div>
                  <a
                    class="mt-4 inline-flex items-center bg-indigo-900 text-indigo-900 rounded-lg animate-pulse"
                  >
                    loading data
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full" v-if="loading">
          <div
            class="shadow-xl bg-gray-900 border-gray-800 p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
          >
            <div class="flex items-center p-4 rounded-lg">
              <div
                class="w-16 h-16 bg-gray-700 border-gray-700 rounded-full mr-4 animate-pulse"
              ></div>
              <div class="sm:p-6 w-max">
                <div
                  class="mt-3 w-full bg-gray-700 text-gray-700 text-sm rounded animate-pulse"
                >
                  loading loading data ...........
                </div>
                <div
                  class="w-20 mt-1 bg-gray-700 text-gray-700 py-1 text-sm rounded animate-pulse"
                ></div>
                <div>
                  <a
                    class="mt-4 inline-flex items-center bg-indigo-900 text-indigo-900 rounded-lg animate-pulse"
                  >
                    loading data
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full" v-if="loading">
          <div
            class="shadow-xl bg-gray-900 border-gray-800 p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
          >
            <div class="flex items-center p-4 rounded-lg">
              <div
                class="w-16 h-16 bg-gray-700 border-gray-700 rounded-full mr-4 animate-pulse"
              ></div>
              <div class="sm:p-6 w-max">
                <div
                  class="mt-3 w-full bg-gray-700 text-gray-700 text-sm rounded animate-pulse"
                >
                  loading loading data ...........
                </div>
                <div
                  class="w-20 mt-1 bg-gray-700 text-gray-700 py-1 text-sm rounded animate-pulse"
                ></div>
                <div>
                  <a
                    class="mt-4 inline-flex items-center bg-indigo-900 text-indigo-900 rounded-lg animate-pulse"
                  >
                    loading data
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full" v-if="loading">
          <div
            class="shadow-xl bg-gray-900 border-gray-800 p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
          >
            <div class="flex items-center p-4 rounded-lg">
              <div
                class="w-16 h-16 bg-gray-700 border-gray-700 rounded-full mr-4 animate-pulse"
              ></div>
              <div class="sm:p-6 w-max">
                <div
                  class="mt-3 w-full bg-gray-700 text-gray-700 text-sm rounded animate-pulse"
                >
                  loading loading data ...........
                </div>
                <div
                  class="w-20 mt-1 bg-gray-700 text-gray-700 py-1 text-sm rounded animate-pulse"
                ></div>
                <div>
                  <a
                    class="mt-4 inline-flex items-center bg-indigo-900 text-indigo-900 rounded-lg animate-pulse"
                  >
                    loading data
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full" v-if="loading">
          <div
            class="shadow-xl bg-gray-900 border-gray-800 p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
          >
            <div class="flex items-center p-4 rounded-lg">
              <div
                class="w-16 h-16 bg-gray-700 border-gray-700 rounded-full mr-4 animate-pulse"
              ></div>
              <div class="sm:p-6 w-max">
                <div
                  class="mt-3 w-full bg-gray-700 text-gray-700 text-sm rounded animate-pulse"
                >
                  loading loading data ...........
                </div>
                <div
                  class="w-20 mt-1 bg-gray-700 text-gray-700 py-1 text-sm rounded animate-pulse"
                ></div>
                <div>
                  <a
                    class="mt-4 inline-flex items-center bg-indigo-900 text-indigo-900 rounded-lg animate-pulse"
                  >
                    loading data
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full" v-if="loading">
          <div
            class="shadow-xl bg-gray-900 border-gray-800 p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
          >
            <div class="flex items-center p-4 rounded-lg">
              <div
                class="w-16 h-16 bg-gray-700 border-gray-700 rounded-full mr-4 animate-pulse"
              ></div>
              <div class="sm:p-6 w-max">
                <div
                  class="mt-3 w-full bg-gray-700 text-gray-700 text-sm rounded animate-pulse"
                >
                  loading loading data ...........
                </div>
                <div
                  class="w-20 mt-1 bg-gray-700 text-gray-700 py-1 text-sm rounded animate-pulse"
                ></div>
                <div>
                  <a
                    class="mt-4 inline-flex items-center bg-indigo-900 text-indigo-900 rounded-lg animate-pulse"
                  >
                    loading data
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
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
    loading: true,
  }),

  methods: {
    async fetchApi() {
      await axios
        .get(
          "https://mycorsproxy005.herokuapp.com/https://jobs.github.com//positions.json"
        )
        .then((response) => (this.jobs = response.data))
        .catch((e) => console.log(e));
      this.loading = false;
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
