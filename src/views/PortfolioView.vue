<script>
export default {
  data() {
    return {
      items: [
        {
          id: 1,
          name: "Personal Website",
          imageUrl: "portfolio_v1",
          category: "Web Development",
          shortDescription:
            "Modern portfolio website showcasing personal projects and skills",
          fullDescription:
            "My personal website built with Vue.js 3 and Tailwind CSS. This website showcases my profile, skills, and projects while serving as a platform to experiment with new technologies. Features responsive design, smooth animations, and modern UI/UX principles.",
          technologies: [
            "Vue.js 3",
            "Tailwind CSS",
            "JavaScript",
            "HTML5",
            "CSS3",
            "Responsive Design",
          ],
          features: [
            "Responsive design for all devices",
            "Smooth scroll animations",
            "Modern dark theme",
            "Interactive portfolio gallery",
            "Contact form integration",
            "SEO optimized",
          ],
          github: "https://github.com/wildanfm19/portofolio",
          demo: "https://portofolio-wine-six.vercel.app/",
          year: "2025",
        },
        {
          id: 2,
          name: "Food Tracker App",
          imageUrl: "portfolio_v2",
          category: "Full Stack Application",
          shortDescription:
            "Comprehensive food diary application for tracking nutrition and meal planning",
          fullDescription:
            "A comprehensive food diary application built with Spring Boot backend and Angular frontend. This application helps users track their daily nutrition intake, plan meals, and monitor their dietary habits. Features robust REST API architecture, secure authentication, and real-time data visualization for health and wellness management.",
          technologies: [
            "Spring Boot",
            "Angular",
            "PostgreSQL",
            "TypeScript",
            "Bootstrap",
            "JWT Authentication",
          ],
          features: [
            "Daily food intake tracking",
            "Meal planning and scheduling",
            "User authentication and profiles",
            "Progress tracking and reports",
            "Mobile-responsive design",
          ],
          github: "https://github.com/wildanfm19/frontend-foodtracker-v2",
          demo: "https://dailybytes-blue.vercel.app/",
          year: "2025",
        },
        {
          id: 3,
          name: "B-COD Marketplace",
          imageUrl: "portfolio_v3",
          category: "E-Commerce Platform",
          shortDescription:
            "Exclusive marketplace for BINUS University students with Cash on Delivery payment system",
          fullDescription:
            "B-COD is a specialized e-commerce marketplace designed exclusively for BINUS University students and community. Built with Laravel backend and React.js frontend, this platform enables students to buy and sell products with a unique Cash on Delivery (COD) payment system. Features secure authentication with student verification, campus-based delivery zones, and comprehensive order management tailored for university environment.",
          technologies: [
            "Laravel",
            "React.js",
            "MySQL",
            "PHP",
            "JavaScript",
            "Bootstrap",
            "RESTful API",
          ],
          features: [
            "BINUS student verification system",
            "Cash on Delivery (COD) payment only",
            "Campus-based delivery zones",
            "Product listing and search",
            "Student seller dashboard",
          ],
          github: "https://github.com/wildanfm19/frontend_bcod",
          demo: "https://b-cod.vercel.app/",
          year: "2025",
        },
        {
          id: 4,
          name: "Fitness AI Microservices",
          imageUrl: "fitness-ai", // you can replace with a relevant image
          category: "Microservices AI Application",
          shortDescription:
            "Microservices-based fitness tracker with AI recommendations and secure authentication.",
          fullDescription:
            "Fitness AI Microservices is a fitness tracking platform built using a microservices architecture. It uses RabbitMQ for communication between services, Keycloak for secure OAuth authentication, and Gemini API to provide AI-powered personalized recommendations. Spring Boot handles backend services, while each module communicates seamlessly to offer a robust and scalable solution.",
          technologies: [
            "Spring Boot",
            "React",
            "RabbitMQ",
            "Keycloak",
            "Gemini API",
            "PostgreSQL",
          ],
          features: [
            "Microservices architecture for scalable backend",
            "AI-powered personalized fitness recommendations",
            "Secure OAuth authentication with Keycloak",
            "Inter-service communication using RabbitMQ",
            "Frontend dashboard to track fitness data",
          ],
          github: "https://github.com/wildanfm19/fitness-mircoservices", // replace with actual GitHub repo
          year: "2025",
        },
        {
          id: 5,
          name: "Gmail AI Reply Extension",
          imageUrl: "email-extension", // replace with a relevant image
          category: "Browser Extension",
          shortDescription:
            "A Gmail extension that generates AI-powered email replies automatically.",
          fullDescription:
            "Gmail AI Reply Extension integrates directly into Gmail, helping users compose email responses quickly using AI. When the user clicks 'Compose' in Gmail, the AI generates a suggested reply. Built as a browser extension, it leverages the **Gemini API** for AI responses and works seamlessly with Gmail’s interface.",
          technologies: ["JavaScript", "Gemini API", "Chrome Extension APIs"],
          features: [
            "AI-powered automatic email replies",
            "Direct integration with Gmail",
            "Lightweight browser extension",
            "Quick reply generation without leaving Gmail",
          ],
          github: "https://github.com/wildanfm19/email-assistant-extension", // replace with actual repo
          year: "2025",
        },

        {
          id: 6,
          name: "Gmail AI Reply Web App",
          imageUrl: "email-ai-website", // replace with a relevant image
          category: "FullStack Web Application",
          shortDescription:
            "A web app that generates AI-powered email replies automatically.",
          fullDescription:
            "Gmail AI Reply Web App helps users compose email responses quickly using AI. Users can customize and generate replies directly from the web interface. The frontend is built with **React**, the backend uses **Spring Boot**, and the **Gemini API** powers AI response generation. This project demonstrates full-stack development and AI integration for productivity.",
          technologies: ["React", "Spring Boot", "Gemini API", "Tailwind"],
          features: [
            "AI-powered automatic email replies",
            "Web app interface for customizing replies",
            "Responsive frontend built with React",
            "Backend logic handled by Spring Boot",
          ],
          github: "https://github.com/wildanfm19/email-assistant-frontend",
          demo: "https://email-assistant-frontend-beta.vercel.app/", // replace with actual repo
          year: "2025",
        },

        {
          id: 7,
          name: "Gmail AI Reply Web App",
          imageUrl: "email-ai-website", // replace with a relevant image
          category: "FullStack Web Application",
          shortDescription:
            "A web app that generates AI-powered email replies automatically.",
          fullDescription:
            "Gmail AI Reply Web App helps users compose email responses quickly using AI. Users can customize and generate replies directly from the web interface. The frontend is built with **React**, the backend uses **Spring Boot**, and the **Gemini API** powers AI response generation. This project demonstrates full-stack development and AI integration for productivity.",
          technologies: ["React", "Spring Boot", "Gemini API", "Tailwind"],
          features: [
            "AI-powered automatic email replies",
            "Web app interface for customizing replies",
            "Responsive frontend built with React",
            "Backend logic handled by Spring Boot",
          ],
          github: "https://github.com/wildanfm19/email-assistant-frontend",
          demo: "https://email-assistant-frontend-beta.vercel.app/", // replace with actual repo
          year: "2025",
        },

        {
          id: 8,
          name: "NBA 2025 Stats Web App",
          imageUrl: "nba-stats-2025", // replace with a relevant image
          category: "FullStack Web Application",
          shortDescription:
            "A web app that provides NBA player and team statistics using web scraping and a dynamic dashboard.",
          fullDescription:
            "NBA Stats Web App is a full-stack platform that allows users to view and analyze NBA player and team statistics. The backend scrapes data from basketball-reference.com using **Python, pandas, and BeautifulSoup** and stores it in a database. The frontend, built with **React**, displays interactive tables and visualizations. Jupyter Notebooks are used for data analysis and cleaning. This project demonstrates web scraping, backend API development, and responsive frontend design.",
          technologies: [
            "React",
            "Spring Boot",
            "PostgreSQL",
            "Python",
            "pandas",
            "BeautifulSoup",
            "Jupyter Notebook",
            "Tailwind",
          ],
          features: [
            "Web scraping of NBA stats from basketball-reference.com using Python",
            "Data analysis and cleaning in Jupyter Notebook",
            "Interactive tables and dashboards for players and teams",
            "Search and Filter functionality for stats",
            "Responsive frontend built with React",
            "Backend API built with Spring Boot and database integration",
          ],
          github: "https://github.com/wildanfm19/nba_stats_2024-2025", // replace with actual repo
          demo: "https://nba-player-stats-2024-2025-react.vercel.app/home", // replace with actual demo link
          year: "2025",
        },
      ],
    };
  },
  methods: {
    openProjectModal(project) {
      // Emit event to parent App.vue to open global modal
      this.$emit("open-project-modal", project);
    },
    getTechColor(tech) {
      const colors = {
        "Vue.js": "bg-green-500",
        Laravel: "bg-red-500",
        PHP: "bg-blue-500",
        JavaScript: "bg-blue-500",
        MySQL: "bg-orange-500",
        Tailwind: "bg-cyan-500",
        Bootstrap: "bg-purple-500",
      };
      return colors[tech] || "bg-gray-500";
    },
  },
};
</script>
<template>
  <!-- Portfolio Section -->
  <div
    class="bg-gradient-to-br from-[#1a1a1b] via-[#1e1e1f] to-[#252526] px-5 py-8 md:px-12 md:py-12 text-left border border-[#383838] rounded-3xl text-blue-50 mx-3 mb-8 relative overflow-hidden"
  >
    <!-- Background decoration -->
    <div
      class="absolute top-0 right-0 w-72 h-72 bg-blue-500 bg-opacity-5 rounded-full blur-3xl -translate-y-36 translate-x-36"
    ></div>
    <div
      class="absolute bottom-0 left-0 w-56 h-56 bg-blue-400 bg-opacity-3 rounded-full blur-2xl translate-y-28 -translate-x-28"
    ></div>

    <article data-page="portfolio" class="relative z-10">
      <header class="text-center mb-12">
        <h2 class="text-3xl md:text-4xl font-bold text-white mb-4 fadein-bot">
          My Portfolio
        </h2>
        <p class="text-lg md:text-xl text-gray-400 fadein-bot">
          Discover the projects I've built with passion and dedication
        </p>
        <div
          class="h-[2px] w-24 bg-gradient-to-r from-blue-400 to-blue-600 rounded-full mx-auto mt-6"
        ></div>
      </header>

      <section>
        <!-- Project Grid -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 pb-8">
          <div
            v-for="item in items"
            :key="item.id"
            @click.prevent="openProjectModal(item)"
            class="project-card group cursor-pointer select-none"
            role="button"
            tabindex="0"
            @keydown.enter="openProjectModal(item)"
            @keydown.space.prevent="openProjectModal(item)"
          >
            <div
              class="bg-gradient-to-br from-[#2a2a2b] to-[#252526] border border-[#383838] rounded-xl overflow-hidden hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105 relative"
            >
              <!-- Glow effect on hover -->
              <div
                class="absolute inset-0 bg-gradient-to-br from-blue-400/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl"
              ></div>

              <!-- Project Image -->
              <div class="relative overflow-hidden h-48 bg-[#1a1a1b]">
                <img
                  :alt="item.name"
                  loading="lazy"
                  class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
                  :src="'/img/portfolio-' + item.imageUrl + '.png'"
                />
                <div
                  class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent"
                ></div>
                <div class="absolute top-4 left-4">
                  <span
                    class="px-3 py-1 bg-blue-500 bg-opacity-90 text-white text-xs font-medium rounded-full"
                  >
                    {{ item.category }}
                  </span>
                </div>
                <div class="absolute top-4 right-4 text-gray-300 text-sm">
                  {{ item.year }}
                </div>
              </div>

              <!-- Project Info -->
              <div class="p-6 relative z-10">
                <h3
                  class="text-xl font-semibold text-white mb-3 group-hover:text-blue-400 transition-colors duration-300"
                >
                  {{ item.name }}
                </h3>

                <p class="text-gray-400 text-sm mb-4 line-clamp-2">
                  {{ item.shortDescription }}
                </p>

                <!-- Tech Stack Preview -->
                <div class="flex flex-wrap gap-2 mb-4">
                  <span
                    v-for="tech in item.technologies.slice(0, 3)"
                    :key="tech"
                    class="px-2 py-1 bg-blue-500 bg-opacity-10 text-blue-400 text-xs rounded border border-blue-500 border-opacity-30"
                  >
                    {{ tech }}
                  </span>
                  <span
                    v-if="item.technologies.length > 3"
                    class="px-2 py-1 bg-gray-700 text-gray-400 text-xs rounded"
                  >
                    +{{ item.technologies.length - 3 }}
                  </span>
                </div>

                <!-- Action Links -->
                <div class="flex items-center justify-between">
                  <button
                    class="text-blue-400 hover:text-blue-300 text-sm font-medium flex items-center gap-2 group-hover:translate-x-1 transition-transform duration-300"
                  >
                    View Details
                    <svg
                      class="w-4 h-4"
                      fill="none"
                      stroke="currentColor"
                      viewBox="0 0 24 24"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M17 8l4 4m0 0l-4 4m4-4H3"
                      ></path>
                    </svg>
                  </button>

                  <div class="flex gap-3">
                    <a
                      v-if="item.github"
                      :href="item.github"
                      target="_blank"
                      @click.stop
                      class="text-gray-400 hover:text-blue-400 transition-colors duration-300"
                      title="View GitHub Repository"
                    >
                      <svg
                        class="w-5 h-5"
                        fill="currentColor"
                        viewBox="0 0 24 24"
                      >
                        <path
                          d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"
                        />
                      </svg>
                    </a>
                    <a
                      v-if="item.demo"
                      :href="item.demo"
                      target="_blank"
                      @click.stop
                      class="text-gray-400 hover:text-blue-400 transition-colors duration-300"
                      title="View Live Demo"
                    >
                      <svg
                        class="w-5 h-5"
                        fill="none"
                        stroke="currentColor"
                        viewBox="0 0 24 24"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"
                        ></path>
                      </svg>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style scoped>
/* Project Card Animations */
.project-card {
  animation: fadeInUp 0.6s ease-out;
}

.project-card:nth-child(1) {
  animation-delay: 0.1s;
}
.project-card:nth-child(2) {
  animation-delay: 0.2s;
}
.project-card:nth-child(3) {
  animation-delay: 0.3s;
}
.project-card:nth-child(4) {
  animation-delay: 0.4s;
}
.project-card:nth-child(5) {
  animation-delay: 0.5s;
}
.project-card:nth-child(6) {
  animation-delay: 0.6s;
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

/* Line clamp utility */
.line-clamp-2 {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

/* Enhanced Hover Effects */
.project-card .group:hover .bg-gradient-to-br {
  background: linear-gradient(135deg, #2563eb, #1d4ed8);
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .project-card {
    animation-delay: 0s !important;
  }
}
</style>
