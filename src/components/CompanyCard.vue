<template >
  <div class="xl:w-1/3 md:w-1/2 sm:p-3 sm: w-full">
    <div
      class="anime shadow-xl p-2 flex flex-wrap rounded-lg overflow-hidden sm: mt-4 w-full bg-gray-900 border-gray-800"
    >
      <div class="h-full flex items-center p-4 rounded-lg">
        <img
          alt="team"
          class="w-16 h-16 object-cover object-center flex-shrink-0 rounded-full mr-4"
          :src="
            jobs.company_logo != null
              ? jobs.company_logo
              : 'https://logodix.com/logo/32094.jpg'
          "
        />
        <div class="sm:p-4">
          <div
            class="w-max text-xs leading-wide font-semibold text-indigo-800 bg-indigo-200 px-2 sm:py-0.5 rounded-full"
          >
            {{ jobs.type }} - {{ jobs.location }}
          </div>
          <div
            class="font-medium lg: font-semibold sm:text-xl mt-3 overflow-hidden ..."
          >
            {{ jobs.title }}
          </div>
          <div
            class="mt-1 leading-relaxed sm: text-xs overflow-ellipsis overflow-hidden ... text-gray-400 sm:text-sm"
          >
            {{ jobs.company }}
          </div>
          <div>
            <a
              class="mt-4 inline-flex items-center font-semibold text-indigo-400"
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
  </div>
</template>

<script>
export default {
  props: ["jobs"],
};
</script>

