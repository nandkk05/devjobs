<template>
  <section class="text-gray-600 body-font">
    <div class="container px-5 py-24 mx-auto flex flex-wrap">
      <div class="flex flex-wrap -m-4">
        <div class="p-4 lg:w-1/2 md:w-full">
          <div
            class="flex border-2 rounded-lg border-gray-200 border-opacity-50 p-8 sm:flex-row flex-col"
          >
            <div
              class="w-16 h-16 sm:mr-8 sm:mb-0 mb-4 inline-flex items-center justify-center rounded-full bg-indigo-100 text-indigo-500 flex-shrink-0"
            >
              <img class="w-5/6 h-8" :src="company_logo" alt="" />
            </div>
            <div class="flex-grow">
              <h2 class="text-gray-900 text-lg title-font font-medium mb-3">
                {{ company }}
              </h2>
              <p class="leading-relaxed text-base">
                Blue bottle crucifix vinyl post-ironic four dollar toast vegan
                taxidermy. Gastropub indxgo juice poutine.
              </p>
              <a
                class="mt-3 text-indigo-500 inline-flex items-center"
                :href="url"
                >Learn More
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
        <div class="p-4 lg:w-1/2 md:w-full">
          <div
            class="flex border-2 rounded-lg border-gray-200 border-opacity-50 p-8 sm:flex-row flex-col"
          >
            <div
              class="w-16 h-16 sm:mr-8 sm:mb-0 mb-4 inline-flex items-center justify-center rounded-full bg-indigo-100 text-indigo-500 flex-shrink-0"
            >
              <svg
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                class="w-10 h-10"
                viewBox="0 0 24 24"
              >
                <path d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2"></path>
                <circle cx="12" cy="7" r="4"></circle>
              </svg>
            </div>
            <div class="flex-grow">
              <h2 class="text-gray-900 text-lg title-font font-medium mb-3">
                The Catalyzer
              </h2>
              <p class="leading-relaxed text-base">
                Blue bottle crucifix vinyl post-ironic four dollar toast vegan
                taxidermy. Gastropub indxgo juice poutine.
              </p>
              <a class="mt-3 text-indigo-500 inline-flex items-center"
                >Learn More
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
  </section>
</template>

<script>
export default {
  data: () => ({
    imageUrl:
      "https://images.unsplash.com/photo-1611095564350-2cbe940a8d99?ixid=MnwxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1351&q=80",
    id: "3caf1d30-d5ae-4971-bd7a-2ee47ec0a90e",
    type: "Full Time",
    url:
      "https://jobs.github.com/positions/3caf1d30-d5ae-4971-bd7a-2ee47ec0a90e",
    created_at: "Sat May 15 00:05:16 UTC 2021",
    company: "Amco International Education Services",
    company_url: null,
    description:
      "\u003cp\u003eWe are an education technology company teaching kids fluent English all over the world.\nWe started as one man's vision to solve a simple problem for the students of his own school. In a little, over a decade we've grown into an international multimillion-dollar company positively affecting the lives of over 300,000 students a year.\u003c/p\u003e\n\u003ch1\u003eJob Description\u003c/h1\u003e\n\u003cp\u003eYour bread and butter of the day will be not just to code, but to engineer solutions to sometimes simple, most of the time complex problems.\nYou'll work closely with software designers, developers, and sometimes end-users, to understand more about what each product is meant to do, its key features, and who will use it.\nYou'll often be working on more than one project at a time, one product in the first phase of testing and another in its second or final phase.\u003c/p\u003e\n\u003ch1\u003eResponsibilities\u003c/h1\u003e\n\u003cp\u003eWhen you apply at a company you want to have some idea of the kinds of projects you may eventually help with, here is just a small list of what we're currently working on:\u003c/p\u003e\n\u003cul\u003e\n\u003cli\u003eDesign, build and maintain efficient, reusable, and reliable Ruby/Elixir code\u003c/li\u003e\n\u003cli\u003eIntegration of data storage solutions for MySQL, Postgres and CouchDB\u003c/li\u003e\n\u003cli\u003eIntegration of client apps for web, Android, and iOS, with server-side infrastructure.\u003c/li\u003e\n\u003cli\u003eIdentify bottlenecks and bugs, and devise solutions to these problems\u003c/li\u003e\n\u003cli\u003eHelp maintain code quality, organization, and automatization\u003c/li\u003e\n\u003c/ul\u003e\n\u003ch1\u003eSkills\u003c/h1\u003e\n\u003cul\u003e\n\u003cli\u003eExperience with Ruby on Rails, along with other common libraries\u003c/li\u003e\n\u003cli\u003eHands-on experience/interest on Elixir/Phoenix framework\u003c/li\u003e\n\u003cli\u003eGood understanding of the syntax of Ruby and its nuances\u003c/li\u003e\n\u003cli\u003eSolid understanding of object-oriented programming\u003c/li\u003e\n\u003cli\u003eGood understanding of server-side templating languages such as Haml\u003c/li\u003e\n\u003cli\u003eGood understanding of server-side CSS preprocessors such as Sass\u003c/li\u003e\n\u003cli\u003eBasic understanding of front-end technologies, such as JavaScript, HTML5, and CSS3\u003c/li\u003e\n\u003cli\u003eFamiliarity with concepts of MVC, Mocking, ORM, and RESTful\u003c/li\u003e\n\u003cli\u003eA knack for writing clean, readable code\u003c/li\u003e\n\u003cli\u003eAbility to integrate multiple data sources and databases into one system\u003c/li\u003e\n\u003cli\u003eUnderstanding of fundamental design principles behind a scalable application\u003c/li\u003e\n\u003cli\u003eAble to create database schemas that represent and support business processes\u003c/li\u003e\n\u003cli\u003eAble to implement automated testing platforms and unit tests\u003c/li\u003e\n\u003cli\u003eProficient understanding of Git\u003c/li\u003e\n\u003cli\u003eFamiliarity with development aiding tools Bundler, Webpacker\u003c/li\u003e\n\u003cli\u003eFamiliarity with continuous integration\u003c/li\u003e\n\u003c/ul\u003e\n",
    how_to_apply:
      '\u003cp\u003eEmail your resume to \u003ca href="mailto:javierg@amco.me"\u003ejavierg@amco.me\u003c/a\u003e\u003c/p\u003e\n',
    company_logo:
      "https://jobs.github.com/rails/active_storage/blobs/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBdmlpIiwiZXhwIjpudWxsLCJwdXIiOiJibG9iX2lkIn19--dc9fec9a025caaf3eb1528dade6f46bd61e86725/Amco%20Logo@2x.png",
  }),
};
</script>

