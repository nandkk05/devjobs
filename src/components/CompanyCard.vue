<template>
  <div class="xl:w-1/3 md:w-1/2 p-4 sm: w-full">
    <div
      class="bg-white dark:bg-gray-800 border p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full"
    >
      <div class="p-6">
        <div
          class="text-gray-600 text-xs uppercase font-semibold tracking-wide"
        >
          {{ jobs.type }}
        </div>
        <h4 class="font-semibold text-xl mt-2 leading-relaxed truncate">
          {{ jobs.title }}
        </h4>
        <div class="mt-1 leading-relaxed truncate">
          {{ jobs.company }}
        </div>
        <div>
          <a
            class="mt-2 text-blue-500 inline-flex items-center font-semibold"
            :href="jobs.url"
            >See job
            <svg
              fill="none"
              stroke="currentColor"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              class="w-4 h-4 ml-2"
              viewBox="0 0 24 24"
            >
              <path d="M5 12h14M12 5l7 7-7 7"></path>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["jobs"],
};
</script>

