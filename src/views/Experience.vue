<template>
  <div class="flex-1 h-full py-8 px-6 justify-center text-gray-800">
    <div class="max-w-6xl mx-auto py-8">
      <div class="lg:mx-12 text-5xl text-blue-700 font-normal">Experience</div>
      <transition-group appear tag="div" class="skill" name="animation">
        <div
          class="lg:mx-12 mt-6 sm:mt-12 bg-job rounded overflow-hidden shadow-lg md:flex"
          v-for="job in jobs"
          v-bind:key="job.title"
        >
          <div class="md:w-1/2 md:pt-16 md:pr-0 md:pl-12">
            <a
              class="block relative padding-image-sm md:padding-image-lg"
              :href="job.link"
              target="_blank"
            >
              <img
                class="inset-0 absolute block rounded-t md:rounded-b md:shadow-lg hover:opacity-75"
                :src="job.img.src"
                :alt="job.img.alt"
              />
            </a>
          </div>
          <div
            class="px-6 pb-6 pt-3 md:w-1/2 md:px-12 md:py-8 md:flex md:items-center"
          >
            <div>
              <div class="antialiased text-2xl md:text-2xl font-medium ">
                <a
                  :href="job.link"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="text-gray-100 hover:text-gray-300"
                  >{{ job.title }}</a
                >
              </div>
              <div
                class="text-gray-100 mt-2 md:mt-3 antialiased font-medium text-sm md:text-md leading-tight md:leading-normal opacity-90"
              >
                {{ job.description }}
              </div>
              <div class="px-6 py-4">
                <a
                  :href="tool.link"
                  target="_blank"
                  v-for="tool in job.tools"
                  v-bind:key="tool.name"
                  class="inline-block shadow-md bg-gray-300 hover:bg-gray-500 rounded-full px-3 py-1 text-xs font-semibold text-gray-700 mr-2"
                  >{{ tool.name }}</a
                >
              </div>
            </div>
          </div>
        </div>
      </transition-group>
    </div>
    <div class="flex  sm:invisible pt-4">
      <router-link
        to="/contact"
        class=" mx-auto text-center font-bold py-2 px-4 rounded flex items-center bg-blue-500 hover:bg-blue-700 text-gray-100 px-4 border-b-4 border-blue-800 shadow-md"
      >
        <span class="pr-3 tracking-wider font-mono">Contact Me</span>
        <svg
          class="fill-current"
          style="width:24px;height:24px"
          viewBox="0 0 24 24"
        >
          <path
            d="M4,11V13H16L10.5,18.5L11.92,19.92L19.84,12L11.92,4.08L10.5,5.5L16,11H4Z"
          />
        </svg>
      </router-link>
    </div>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      jobs: [
        {
          title: "SaveBiking",
          description: `Developed Single Page Application using React.js, Redux, designed responsive web interface with Tailwindcss and
prototyped the UI with Figma.
• Ensuring the high security, designed and developed REST API together with cookie based JWT authentication using
Express.js and MongoDB databese.
• Reduced the latency by using AWS S3 for media files, Redis caching mechanism, and MongoDB high performing index
searching.`,
          link: "https://savebiking.com/?lang=en",
          img: {
            src: "./img/Experience/SaveBiking.png",
            alt: "SaveBiking"
          },
          tools: [
            { name: "React Native", link: "https://facebook.github.io/react-native/" },
            { name: "Ruby on Rails", link: "https://kivy.org/" },
            { name: "AWS", link: "https://aws.amazon.com" }
          ]
        },
        {
          title: "Yellow-Space",
          link: "https://yellowspace.netlify.app/",
          description: `Developed Single Page Application using React.js, Redux, designed responsive web interface with Tailwindcss and
prototyped the UI with Figma.
• Ensuring the high security, designed and developed REST API together with cookie based JWT authentication using
Express.js and MongoDB databese.
• Reduced the latency by using AWS S3 for media files, Redis caching mechanism, and MongoDB high performing index
searching.`,
          img: {
            src: "/img/Experience/UCA.png",
            alt: "Yellow-Space"
          },
          tools: [
            {
              name: "React",
              link: "https://wordpress.org"
            },
            {
              name: "Express",
              link: "https://wordpress.org"
            },
            {
              name: "Node",
              link: "https://wordpress.org"
            },
            {
              name: "MongoDB",
              link: "https://wordpress.org"
            },
            {
              name: "AWS S3",
              link: "https://wordpress.org"
            },
            
          ]
        },
        {
          title: "Zummit Infolabs",
          link: "https://zummitlabs.com/",
          description: `Developed an object detection system to help auto-cleaner detect dirty floors.
• Improved the accuracy of computer vision system by 10% through implementing transfer learning technique.
• Implemented online learning and deployed the Machine Learning model by using streaming techniques.
• Used CNN architecture (EfficientNet, YOLO) segmentation (Mask R-CNN) to improve the accuracy of CNN model`,
          img: {
            src: "/img/Experience/Zummit.png",
            alt: "PGA"
          },
          tools: [
            { name: "Pytorch", link: "https://wordpress.org" },
            { name: "Computer Vision", link: "https://www.php.net" },
            { name: "Google Colab", link: "https://www.php.net" },
            ]
        },
        {
          title: "Tajrupt",
          link: "https://zypl.ai/",
          description:
            "My responsibilities included the initial research and development of features and projects, and develop web application tools for internal use and web applications for the company clients.",
          img: {
            src: "/img/Experience/Tajrupt.png",
            alt: "Tajrupt"
          },
          tools: [
          { name: "Pytorch", link: "https://wordpress.org" },
            { name: "React", link: "https://www.php.net" },
            { name: "Django", link: "https://www.php.net" },
            { name: "Selenium", link: "https://www.php.net" }
          ]
        },
        {
          title: "Silk Road Professionals .LLC",
          link: "https://www.silkroadprofessionals.com/",
          description:
            `Built Restful API with ASP.NET that served data to the Typescript front-end based on dynamically chosen user inputs that
handled over 50,000 concurrent users.
• Collaborated with 3 interns and senior developer to brainstorm and implement ideas and feedback into app’s development.
• Delivered 3 back-end applications written in ASP.NET and .NET Framework.
• Tested software for bugs and operating speed, fixing bugs and documenting processes to increase efficiency.
• Implemented caching mechanism to lower the latency of a platform by 18%`,
          img: {
            src: "/img/Experience/SilkRoad.png",
            alt: "Silk Road Professionals .LLC"
          },
          tools: [
            { name: "ASP.NET", link: "https://angular.io/" },
          { name: "Redis", link: "https://angular.io/" },
          { name: "Typescript", link: "https://angular.io/" },
          { name: "Visual Studio", link: "https://angular.io/" },
        ]
        }
      ]
    };
  }
};
</script>
<style scoped>
.bg-job {
  background-color: #5b6467;
  background-image: linear-gradient(315deg, #5b6467 0%, #8b939a 74%);
}
</style>
