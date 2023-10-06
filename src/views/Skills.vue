<template>
  <div class="flex-1 h-full py-8 px-6 justify-center text-gray-800">
    <div class="max-w-6xl mx-auto py-8">
      <div class="lg:mx-12 text-5xl text-blue-700 font-normal">Skills</div>
      <div class="pt-6">
        <transition-group appear tag="div" class="skill" name="animation">
          <div
            class="skill md:flex mx-auto my-4 lg:mx-12 shadow-lg lg:max-w-full"
            v-for="(skill, index) in skills"
            v-bind:key="skill.title"
            :class="{'md:flex-row-reverse': index % 2 === 0}"
          >
            <div
              class="h-64 md:h-auto md:w-1/2 flex-none rounded-t text-center overflow-hidden bg-grad"
              :class="{'md:rounded-none md:rounded-r ': index % 2 === 0, ' md:rounded-none md:rounded-l ': index % 2 !== 0}"
            >
              <div class="py-16 inline-flex justify-around imgs-row">
                <img
                  v-for="skillImg in skill.imgs"
                  v-bind:key="skillImg.alt"
                  class="h-32"
                  :src="skillImg.src"
                  alt="Tool logo"
                />
              </div>
            </div>
            <div
              class="w-full md:w-1/2 border-r border-b border-l border-gray-300 md:border-l-0 md:border-t bg-white rounded-b md:rounded-b-none p-4 flext flex-col justify-between leading-normal"
              :class="{'md:rounded-l ': index % 2 === 0, 'md:rounded-r ': index % 2 !== 0}"
            >
              <div class="font-bold text-xl mb-2 p-2 text-gray-800">{{skill.title}}</div>
              <div class=" text-base p-2 text-gray-700">{{skill.description}}</div>
            </div>
          </div>
        </transition-group>
      </div>
      <div class="flex  sm:invisible pt-4">
        <router-link
          to="/experience"
          class=" mx-auto text-center font-bold py-2 rounded flex items-center bg-blue-500 hover:bg-blue-700 text-gray-100 px-4 border-b-4 border-blue-800 shadow-md"
        >
          <span class="pr-3 tracking-wider font-mono">Experience</span>
          <svg class="fill-current" style="width:24px;height:24px" viewBox="0 0 24 24">
            <path  d="M4,11V13H16L10.5,18.5L11.92,19.92L19.84,12L11.92,4.08L10.5,5.5L16,11H4Z" />
          </svg>
        </router-link>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      skills: [
        {
          title: "Web Application",
          description: `I possess a strong command of JavaScript, with extensive experience in working with the DOM API and a deep understanding of JavaScript's core concepts and ES6 features. I am well-versed in popular frameworks and tools such as React, Redux, and Node.js. Furthermore, I am proficient in modern development tooling, including Webpack, NPM/Yarn, and Babel.`,
          imgs: [
            {
              alt: "React",
              src: "/img/react.svg"
            },
            {
              alt: "Redux",
              src: "/img/redux.svg"
            },
            {
              alt: "Tailwind",
              src: "/img/tailwind.svg"
            },
            {
              alt: "Node.js",
              src: "/img/express.svg"
            }
          ]
        },
        {
          title: "Backend development",
          description: `I have a year of experience with different backend frameworks (Django, Express and ASP.NET). I have good skill in optimizing and buidling large scale systems by scaling the system horizontally with high security measures.`,
          imgs: [
            {
              alt: "Django",
              src: "/img/django.svg"
            },
            {
              alt: "ASP.NET",
              src: "/img/asp.svg"
            },
            {
              alt: "Express.js",
              src: "/img/express.svg"
            },
            
          ]
        },
        {
          title: "Mobile Application",
          description: `In my current job as a full stack mobile developer I am using React Native to build cross platform native mobile application for a startup company. The main tasks I did using React Native is building the application main tasks and serving it on google play and app store.`,
          imgs: [
            {
              alt: "React Native",
              src: "/img/reactNative.svg"
            }
          ]
        },
        {
          title: "Machine Learning",
          description: `Skilled machine learning professional with 1+ year of experience in designing and developing ML models and systems across diverse industries. Possesses a diverse experience in collating & analyzing data, enhancing existing models, and revamping business processes as part of providing compelling value to key clients.`,
          imgs: [
            {
              alt: "PyTorch",
              src: "/img/pytorch.svg"
            },
            {
              alt: "Tensorflow",
              src: "/img/tensorflow.svg"
            },
            {
              alt: "Scikit-Learn",
              src: "/img/scikit-learn.svg"
            }
          ]
        },
        {
          title: "Database",
          description: `I have taken Database Management system in my university. In addition to this, I have also hands on experience with database adminitation. I have built several Postgresql and MongoDB schemas for different applications.`,
          imgs: [
            {
              alt: "AWS",
              src: "/img/aws.svg"
            },
            {
              alt: "MongoDB",
              src: "/img/mongodb.svg"
            },
            {
              alt: "PostgreSQL",
              src: "/img/postgresql.svg"
            }
          ]
        },
        {
          title: "DevOps",
          description: `I’m able to create a REST API using API Gateway and Lambda functions. 
I have experience creating CI/CD using Pipeline to automate the deployment of webapps.
Full understanding of IAM to grant the necessary permission.`,
          imgs: [
            {
              alt: "Docker",
              src: "/img/docker.svg"
            },
            {
              alt: "Gitlab",
              src: "/img/gitlab.svg"
            },
            {
              alt: "SQLALchemy",
              src: "/img/python.svg"
            }
          ]
        },
      ]
    };
  }
};
</script>
<style>
.imgs-row {
  width: 130%;
  animation-duration: 25s;
  animation-timing-function: linear;
  animation-delay: 0s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-fill-mode: both;
  animation-play-state: running;
  animation-name: imgs;
}
@keyframes imgs {
  100% {
    transform: translate(20%);
  }
  50% {
    transform: translate(-20%);
  }
}
.bg-grad {
  background-color: #5b6467;
  background-image: linear-gradient(315deg, #5b6467 0%, #8b939a 74%);
}
</style>
