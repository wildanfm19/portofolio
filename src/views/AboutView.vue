<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        {
          id: 1,
          name: "Spring Boot",
          imageUrl:
            "https://cdn.worldvectorlogo.com/logos/spring-3.svg",
          status: "Advanced",
        },
        {
          id: 2,
          name: "Angular",
          imageUrl:
            "https://cdn.worldvectorlogo.com/logos/angular-icon-1.svg",
          status: "Intermediate",
        },
        {
          id: 3,
          name: "Laravel",
          imageUrl: "https://cdn.worldvectorlogo.com/logos/laravel-2.svg",
          status: "Intermediate",
        },
        {
          id: 4,
          name: "HTML",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/1051/1051277.png",
          status: "Intermediate",
        },
        {
          id: 5,
          name: "CSS",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/732/732190.png",
          status: "Intermediate",
        },
        {
          id: 6,
          name: "Javascript",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png",
          status: "Intermediate",
        },
        {
          id: 7,
          name: "Java",
          imageUrl:
            "https://cdn-icons-png.flaticon.com/512/226/226777.png",
          status: "Advanced",
        },
        {
          id: 8,
          name: "Python",
          imageUrl:
            "https://cdn-icons-png.flaticon.com/512/5968/5968350.png",
          status: "Intermediate",
        },
        {
          id: 9,
          name: "Bootstrap",
          imageUrl:
            "https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png",
          status: "Intermediate",
        },
        {
          id: 10,
          name: "ReactJS",
          imageUrl:
            "https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-512.png",
          status: "Beginner",
        },
        {
          id: 11,
          name: "PHP",
          imageUrl:
            "https://cdn-icons-png.flaticon.com/512/5968/5968332.png",
          status: "Intermediate",
        },
      ],
      tools: [
        {
          id: 1,
          name: "Git",
          imageUrl:
            "https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png",
          status: "Version Control",
        },
        {
          id: 2,
          name: "GitHub",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/25/25231.png",
          status: "Git Hosting",
        },
        {
          id: 3,
          name: "NPM",
          imageUrl:
            "https://cdn.iconscout.com/icon/free/png-256/free-npm-3-1175132.png",
          status: "Package Manager",
        },
        {
          id: 4,
          name: "MySQL",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/5968/5968313.png",
          status: "Database",
        },
        {
          id: 5,
          name: "Docker",
          imageUrl:
            "https://cdn.worldvectorlogo.com/logos/docker.svg",
          status: "Containerization",
        },
        {
          id: 6,
          name: "Kubernetes",
          imageUrl:
            "https://cdn.worldvectorlogo.com/logos/kubernets.svg",
          status: "Orchestration",
        },
        {
          id: 7,
          name: "Kafka",
          imageUrl:
            "https://cdn.worldvectorlogo.com/logos/kafka.svg",
          status: "Message Broker",
        },
        {
          id: 8,
          name: "PostgreSQL",
          imageUrl:
            "https://cdn.worldvectorlogo.com/logos/postgresql.svg",
          status: "Database",
        },
        {
          id: 9,
          name: "MongoDB",
          imageUrl:
            "https://cdn.worldvectorlogo.com/logos/mongodb-icon-1.svg",
          status: "Database",
        },
      ],
    };
  }
};
</script>
<template>
  <!-- Hero About Section -->
    <div class="bg-gradient-to-br from-[#1a1a1b] via-[#1e1e1f] to-[#252526] px-5 py-8 md:px-12 md:py-12 text-left border border-[#383838] rounded-3xl text-blue-50 mx-3 mb-8 relative overflow-hidden">
    <!-- Background shapes for visual interest -->
    <div class="absolute top-0 right-0 w-64 h-64 bg-blue-400 bg-opacity-5 rounded-full blur-3xl -translate-y-32 translate-x-32"></div>
    <div class="absolute bottom-0 left-0 w-48 h-48 bg-blue-400 bg-opacity-3 rounded-full blur-2xl translate-y-24 -translate-x-24"></div>
    
    <article data-page="about" class="relative z-10">
      <header class="mb-8">
        <div class="text-3xl md:text-4xl font-bold text-white mb-2 fadein-bot title-section flex items-center">
          About Me &nbsp;
          <div class="h-[2px] w-32 bg-gradient-to-r from-blue-400 to-blue-500 md:w-96 rounded-full"></div>
        </div>
        <p class="text-blue-400 text-lg md:text-xl font-medium fadein-bot">Full-Stack Developer & Problem Solver</p>
      </header>

      <section class="grid md:grid-cols-12 gap-8 items-center">
        <!-- Profile Image -->
        <div class="md:col-span-4 flex justify-center">
          <div class="relative group">
            <div class="absolute -inset-1 bg-gradient-to-r from-blue-400 to-blue-500 rounded-full blur opacity-25 group-hover:opacity-75 transition duration-1000 group-hover:duration-200"></div>
            <div class="relative bg-[#1e1e1f] rounded-full p-2 border border-blue-400 border-opacity-30">
              <img
                class="w-48 h-48 md:w-56 md:h-56 rounded-full object-cover fadein-up transform hover:scale-105 transition-transform duration-500"
                src="/avatar.png"
                alt="Wildan Fariezky Maaruf"
              />
            </div>
          </div>
        </div>

        <!-- Content -->
        <div class="md:col-span-8 space-y-6">
          <div class="fadein-left fadeins-1">
                        <h3 class="text-2xl font-semibold text-blue-400 mb-3">Hi, I'm Wildan Fariezky Maaruf 👋</h3>
            <p class="text-gray-300 leading-relaxed text-base md:text-lg">
              A passionate Computer Science student at <span class="text-blue-400 font-medium">BINUS University</span> with a love for creating innovative web solutions. I specialize in full-stack development using modern technologies like Spring Boot, Angular, and various cloud platforms.
            </p>
          </div>

          <div class="fadein-left fadeins-2">
            <p class="text-gray-300 text-lg leading-relaxed">
              I believe in writing clean, efficient code that solves real-world problems. My approach combines technical precision with creative thinking to deliver applications that are not just functional, but truly exceptional in user experience.
            </p>
          </div>
        </div>
      </section>
    </article>
  </div>

  <!-- What I Do Section -->
  <div class="bg-[#1e1e1f] px-5 py-8 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-blue-50 mx-3 mb-8">
    <div class="relative z-10">
      <div class="flex items-center justify-center flex-col fadein-bot delay-2">
        <h2 class="text-3xl md:text-4xl font-bold mb-4">What I Do</h2>
        <div class="h-[2px] w-24 bg-gradient-to-r from-blue-400 to-blue-500 md:w-64 rounded-full"></div>
      </div>

      <div class="grid md:grid-cols-3 gap-8 mt-12">
        <!-- Frontend Development -->
        <div class="bg-gradient-to-br from-[#2a2a2b] to-[#252526] p-6 rounded-xl border border-[#383838] hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105 group">
          <div class="w-12 h-12 bg-blue-400 bg-opacity-10 rounded-lg flex items-center justify-center mb-4 group-hover:bg-opacity-20 transition-colors duration-300">
            <svg class="w-6 h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-3 group-hover:text-blue-400 transition-colors duration-300">Frontend Development</h3>
          <p class="text-gray-400">Creating responsive, interactive user interfaces with modern frameworks like Vue.js, Angular, and React.</p>
        </div>

        <!-- Backend Development -->
        <div class="bg-gradient-to-br from-[#2a2a2b] to-[#252526] p-6 rounded-xl border border-[#383838] hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105 group">
          <div class="w-12 h-12 bg-blue-400 bg-opacity-10 rounded-lg flex items-center justify-center mb-4 group-hover:bg-opacity-20 transition-colors duration-300">
            <svg class="w-6 h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h14M5 12a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v4a2 2 0 01-2 2M5 12a2 2 0 00-2 2v4a2 2 0 002 2h14a2 2 0 002-2v-4a2 2 0 00-2-2m-2-4h.01M17 16h.01"></path>
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-3 group-hover:text-blue-400 transition-colors duration-300">Backend Development</h3>
          <p class="text-gray-400">Building robust server-side applications using Spring Boot, Laravel, and Node.js with secure APIs and databases.</p>
        </div>

        <!-- Full-Stack Solutions -->
        <div class="bg-gradient-to-br from-[#2a2a2b] to-[#252526] p-6 rounded-xl border border-[#383838] hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105 group">
          <div class="w-12 h-12 bg-blue-400 bg-opacity-10 rounded-lg flex items-center justify-center mb-4 group-hover:bg-opacity-20 transition-colors duration-300">
            <svg class="w-6 h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"></path>
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-3 group-hover:text-blue-400 transition-colors duration-300">Full-Stack Solutions</h3>
          <p class="text-gray-400">End-to-end web application development from concept to deployment, including cloud integration and optimization.</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Skills & Technologies Section -->
  <div class="bg-gradient-to-br from-[#1a1a1b] via-[#1e1e1f] to-[#252526] px-5 py-8 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-blue-50 mx-3 mb-8 relative overflow-hidden">
    <!-- Background decoration -->
    <div class="absolute top-0 left-0 w-72 h-72 bg-blue-400 bg-opacity-3 rounded-full blur-3xl -translate-y-36 -translate-x-36"></div>
    <div class="absolute bottom-0 right-0 w-56 h-56 bg-blue-500 bg-opacity-5 rounded-full blur-2xl translate-y-28 translate-x-28"></div>
    
    <article data-page="about" class="relative z-10">
      <header class="mb-8">
        <div class="text-2xl md:text-3xl font-bold text-white mb-2 fadein-bot title-section flex items-center">
          <div class="h-[2px] w-16 bg-gradient-to-r from-blue-500 to-blue-400 md:w-32 rounded-full mr-4"></div>
          Skills & Technologies
        </div>
        <p class="text-gray-400 text-lg">Technologies and tools I work with to bring ideas to life</p>
      </header>
      
      <section>
        <!-- Enhanced Tab Navigation -->
        <div class="mb-8">
          <div class="bg-[#2a2a2b] p-1 rounded-xl border border-[#383838] inline-flex">
            <button
              class="px-6 py-3 rounded-lg font-medium transition-all duration-300 mr-1"
              :class="{
                'text-white bg-blue-500 shadow-lg transform scale-105': activeTab === 1,
                'text-gray-400 hover:text-white hover:bg-[#383838]': activeTab !== 1
              }"
              @click="activeTab = 1"
            >
              <span class="flex items-center">
                <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"></path>
                </svg>
                Tech Stack
              </span>
            </button>
            <button
              class="px-6 py-3 rounded-lg font-medium transition-all duration-300"
              :class="{
                'text-white bg-blue-500 shadow-lg transform scale-105': activeTab === 2,
                'text-gray-400 hover:text-white hover:bg-[#383838]': activeTab !== 2
              }"
              @click="activeTab = 2"
            >
              <span class="flex items-center">
                <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                </svg>
                Tools & Platforms
              </span>
            </button>
          </div>
        </div>
        <!-- Tech Stack Tab -->
        <div v-show="activeTab === 1" class="animate-fade-in">
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6 pb-8">
            <div v-for="item in tech" :key="item.id" class="group">
              <div class="tech-card bg-gradient-to-br from-[#2a2a2b] to-[#252526] border border-[#383838] rounded-xl p-4 hover:border-blue-400 hover:shadow-lg hover:shadow-blue-400/10 transition-all duration-300 hover:transform hover:scale-105 relative overflow-hidden">
                <!-- Glow effect on hover -->
                <div class="absolute inset-0 bg-gradient-to-br from-blue-400/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl"></div>
                
                <div class="relative z-10 flex items-center space-x-4">
                  <div class="flex-shrink-0">
                    <div class="w-14 h-14 bg-[#1a1a1b] rounded-lg flex items-center justify-center border border-[#383838] group-hover:border-blue-400/30 transition-colors duration-300">
                      <img
                        :alt="item.name"
                        loading="lazy"
                        class="w-8 h-8 object-contain group-hover:scale-110 transition-transform duration-300"
                        :src="item.imageUrl"
                      />
                    </div>
                  </div>
                  
                  <div class="flex-1 min-w-0">
                    <h3 class="text-white font-semibold text-lg group-hover:text-blue-400 transition-colors duration-300">
                      {{ item.name }}
                    </h3>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Tools Tab -->
        <div v-show="activeTab === 2" class="animate-fade-in">
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 pb-8">
            <div v-for="item in tools" :key="item.id" class="group">
              <div class="tool-card bg-gradient-to-br from-[#2a2a2b] to-[#252526] border border-[#383838] rounded-xl p-6 hover:border-blue-400 hover:shadow-lg hover:shadow-blue-400/10 transition-all duration-300 hover:transform hover:scale-105 relative overflow-hidden">
                <!-- Glow effect on hover -->
                <div class="absolute inset-0 bg-gradient-to-br from-blue-400/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl"></div>
                
                <div class="relative z-10 text-center">
                  <div class="w-16 h-16 bg-[#1a1a1b] rounded-full flex items-center justify-center border border-[#383838] group-hover:border-blue-400/30 transition-all duration-300 mx-auto mb-4 group-hover:shadow-lg group-hover:shadow-blue-400/20">
                    <img
                      :alt="item.name"
                      loading="lazy"
                      class="w-8 h-8 object-contain group-hover:scale-110 transition-transform duration-300"
                      :src="item.imageUrl"
                    />
                  </div>
                  
                  <h3 class="text-white font-semibold text-lg mb-2 group-hover:text-blue-400 transition-colors duration-300">
                    {{ item.name }}
                  </h3>
                  
                  <span class="inline-block px-3 py-1 bg-blue-400 bg-opacity-10 text-blue-400 text-sm rounded-full border border-blue-400 border-opacity-30 group-hover:bg-opacity-20 transition-colors duration-300">
                    {{ item.status }}
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
/* Enhanced animations */
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.8s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(50px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadein-up {
  opacity: 0;
  animation: fadeInUp 0.8s ease-out forwards;
}

@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translateY(30px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.fadein-bot {
  opacity: 0;
  animation: fadeInBot 0.8s ease-out forwards;
}

@keyframes fadeInBot {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Staggered animations */
.fadeins-1 { animation-delay: 0.2s; }
.fadeins-2 { animation-delay: 0.4s; }
.fadeins-3 { animation-delay: 0.6s; }

/* Tab content animation */
.animate-fade-in {
  animation: tabFadeIn 0.5s ease-out forwards;
}

@keyframes tabFadeIn {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Card hover effects */
.tech-card {
  position: relative;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.tech-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, rgba(255, 219, 112, 0.1) 0%, transparent 50%);
  opacity: 0;
  transition: opacity 0.3s ease;
  border-radius: 0.75rem;
  pointer-events: none;
}

.tech-card:hover::before {
  opacity: 1;
}

.tool-card {
  position: relative;
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.tool-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: radial-gradient(circle at center, rgba(255, 219, 112, 0.1) 0%, transparent 70%);
  opacity: 0;
  transition: opacity 0.3s ease;
  border-radius: 0.75rem;
  pointer-events: none;
}

.tool-card:hover::before {
  opacity: 1;
}

/* Custom scrollbar for better aesthetics */
::-webkit-scrollbar {
  width: 6px;
}

::-webkit-scrollbar-track {
  background: #1a1a1b;
  border-radius: 3px;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(to bottom, #3b82f6, #2563eb);
  border-radius: 3px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(to bottom, #2563eb, #3b82f6);
}

/* Responsive design improvements */
@media (max-width: 640px) {
  .tech-card, .tool-card {
    padding: 1rem;
  }
  
  .tech-card .flex {
    flex-direction: column;
    text-align: center;
  }
  
  .tech-card .space-x-4 > :not([hidden]) ~ :not([hidden]) {
    margin-right: 0;
    margin-left: 0;
    margin-top: 0.75rem;
  }
}

/* Background gradient animation */
@keyframes gradientShift {
  0%, 100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}

.bg-gradient-animated {
  background: linear-gradient(270deg, #1a1a1b, #1e1e1f, #252526);
  background-size: 600% 600%;
  animation: gradientShift 8s ease infinite;
}
</style>
