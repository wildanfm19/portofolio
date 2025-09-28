<script>
export default {
  mounted() {
    // Add keyboard event listener for ESC key
    document.addEventListener('keydown', this.handleEscapeKey);
  },
  unmounted() {
    // Clean up event listener
    document.removeEventListener('keydown', this.handleEscapeKey);
    // Restore body scroll if component is unmounted while modal is open
    document.body.style.overflow = 'auto';
  },
  data() {
    return {
      selectedProject: null,
      showModal: false,
      items: [
        {
          id: 1,
          name: 'Personal Website',
          imageUrl: 'portfolio_v1',
          category: 'Web Development',
          shortDescription: 'Modern portfolio website showcasing personal projects and skills',
          fullDescription: 'My personal website built with Vue.js 3 and Tailwind CSS. This website showcases my profile, skills, and projects while serving as a platform to experiment with new technologies. Features responsive design, smooth animations, and modern UI/UX principles.',
          technologies: ['Vue.js 3', 'Tailwind CSS', 'JavaScript', 'HTML5', 'CSS3', 'Responsive Design'],
          features: [
            'Responsive design for all devices',
            'Smooth scroll animations',
            'Modern dark theme',
            'Interactive portfolio gallery',
            'Contact form integration',
            'SEO optimized'
          ],
          github: 'https://github.com/rakha-elctrnx/Portofolio-v2',
          demo: 'https://bagasrakha.netlify.app/',
          year: '2025'
        },
        {
          id: 2,
          name: 'Food Tracker App',
          imageUrl: 'portfolio_v2',
          category: 'Full Stack Application',
          shortDescription: 'Comprehensive food diary application for tracking nutrition and meal planning',
          fullDescription: 'A comprehensive food diary application built with Spring Boot backend and Angular frontend. This application helps users track their daily nutrition intake, plan meals, and monitor their dietary habits. Features robust REST API architecture, secure authentication, and real-time data visualization for health and wellness management.',
          technologies: ['Spring Boot', 'Angular', 'MySQL', 'TypeScript', 'Bootstrap', 'JWT Authentication'],
          features: [
            'Daily food intake tracking',
            'Meal planning and scheduling',
            'User authentication and profiles',
            'Progress tracking and reports',
            'Mobile-responsive design'
          ],
          github: 'https://github.com/wildanfm19/frontend-foodtracker-v2',
          demo: 'https://dailybytes-blue.vercel.app/',
          year: '2025'
        },
         {
          id: 3,
          name: 'B-COD Marketplace',
          imageUrl: 'portfolio_v3',
          category: 'E-Commerce Platform',
          shortDescription: 'Exclusive marketplace for BINUS University students with Cash on Delivery payment system',
          fullDescription: 'B-COD is a specialized e-commerce marketplace designed exclusively for BINUS University students and community. Built with Laravel backend and React.js frontend, this platform enables students to buy and sell products with a unique Cash on Delivery (COD) payment system. Features secure authentication with student verification, campus-based delivery zones, and comprehensive order management tailored for university environment.',
          technologies: ['Laravel', 'React.js', 'MySQL', 'PHP', 'JavaScript', 'Bootstrap', 'RESTful API'],
          features: [
            'BINUS student verification system',
            'Cash on Delivery (COD) payment only',
            'Campus-based delivery zones',
            'Product listing and search',
            'Student seller dashboard',
          ],
          github: 'https://github.com/wildanfm19/frontend_bcod',
          demo: 'https://b-cod.vercel.app/',
          year: '2025'
        }
      ]
    };
  },
  methods: {
    openProjectModal(project) {
      this.selectedProject = project;
      this.showModal = true;
      document.body.style.overflow = 'hidden';
      // Emit event to parent to hide navbar
      this.$emit('modal-opened');
    },
    closeModal() {
      this.showModal = false;
      this.selectedProject = null;
      document.body.style.overflow = 'auto';
      // Emit event to parent to show navbar
      this.$emit('modal-closed');
    },
    handleEscapeKey(event) {
      if (event.key === 'Escape' && this.showModal) {
        this.closeModal();
      }
    },
    getTechColor(tech) {
      const colors = {
        'Vue.js': 'bg-green-500',
        'Laravel': 'bg-red-500',
        'PHP': 'bg-blue-500',
        'JavaScript': 'bg-blue-500',
        'MySQL': 'bg-orange-500',
        'Tailwind': 'bg-cyan-500',
        'Bootstrap': 'bg-purple-500'
      };
      return colors[tech] || 'bg-gray-500';
    }
  }
}
</script>
<template>
  <!-- Portfolio Section -->
  <div class="bg-gradient-to-br from-[#1a1a1b] via-[#1e1e1f] to-[#252526] px-5 py-8 md:px-12 md:py-12 text-left border border-[#383838] rounded-3xl text-blue-50 mx-3 mb-8 relative overflow-hidden">
    <!-- Background decoration -->
    <div class="absolute top-0 right-0 w-72 h-72 bg-blue-500 bg-opacity-5 rounded-full blur-3xl -translate-y-36 translate-x-36"></div>
    <div class="absolute bottom-0 left-0 w-56 h-56 bg-blue-400 bg-opacity-3 rounded-full blur-2xl translate-y-28 -translate-x-28"></div>
    
    <article data-page="portfolio" class="relative z-10">
      <header class="text-center mb-12">
        <h2 class="text-3xl md:text-4xl font-bold text-white mb-4 fadein-bot">
          My Portfolio
        </h2>
        <p class="text-lg md:text-xl text-gray-400 fadein-bot">
          Discover the projects I've built with passion and dedication
        </p>
        <div class="h-[2px] w-24 bg-gradient-to-r from-blue-400 to-blue-600 rounded-full mx-auto mt-6"></div>
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
            <div class="bg-gradient-to-br from-[#2a2a2b] to-[#252526] border border-[#383838] rounded-xl overflow-hidden hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105 relative">
              <!-- Glow effect on hover -->
              <div class="absolute inset-0 bg-gradient-to-br from-blue-400/5 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-xl"></div>
              
              <!-- Project Image -->
              <div class="relative overflow-hidden h-48 bg-[#1a1a1b]">
                <img 
                  :alt="item.name" 
                  loading="lazy" 
                  class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
                  :src="'/img/portfolio-' + item.imageUrl + '.png'"
                >
                <div class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent"></div>
                <div class="absolute top-4 left-4">
                  <span class="px-3 py-1 bg-blue-500 bg-opacity-90 text-white text-xs font-medium rounded-full">
                    {{ item.category }}
                  </span>
                </div>
                <div class="absolute top-4 right-4 text-gray-300 text-sm">
                  {{ item.year }}
                </div>
              </div>

              <!-- Project Info -->
              <div class="p-6 relative z-10">
                <h3 class="text-xl font-semibold text-white mb-3 group-hover:text-blue-400 transition-colors duration-300">
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
                  <button class="text-blue-400 hover:text-blue-300 text-sm font-medium flex items-center gap-2 group-hover:translate-x-1 transition-transform duration-300">
                    View Details
                    <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
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
                      <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
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
                      <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"></path>
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

  <!-- Project Detail Modal -->
  <transition 
    enter-active-class="transition-all duration-300 ease-out"
    leave-active-class="transition-all duration-200 ease-in"
    enter-from-class="opacity-0 scale-95"
    enter-to-class="opacity-100 scale-100"
    leave-from-class="opacity-100 scale-100"
    leave-to-class="opacity-0 scale-95"
  >
    <div 
      v-if="showModal && selectedProject" 
      class="fixed inset-0 z-[9999] flex items-center justify-center p-4 bg-black bg-opacity-75 backdrop-blur-sm"
      @click="closeModal"
      style="margin: 0 !important;"
    >
      <div 
        class="bg-gradient-to-br from-[#1e1e1f] to-[#252526] border border-[#383838] rounded-2xl max-w-4xl w-full max-h-[90vh] overflow-y-auto relative shadow-2xl"
        @click.stop
      >
        <!-- Close Button -->
      <button 
        @click="closeModal"
        class="absolute top-4 right-4 z-10 w-10 h-10 bg-red-500 bg-opacity-20 hover:bg-opacity-40 text-red-400 rounded-full flex items-center justify-center transition-all duration-300"
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
        </svg>
      </button>

      <!-- Modal Content -->
      <div class="p-8">
        <!-- Header -->
        <div class="flex flex-col md:flex-row gap-6 mb-8">
          <div class="md:w-1/2">
            <img 
              :alt="selectedProject.name"
              class="w-full h-64 object-cover rounded-xl border border-[#383838]"
              :src="'/img/portfolio-' + selectedProject.imageUrl + '.png'"
            >
          </div>
          <div class="md:w-1/2">
            <div class="flex items-center gap-3 mb-4">
              <span class="px-3 py-1 bg-blue-500 bg-opacity-20 text-blue-400 text-sm font-medium rounded-full border border-blue-500 border-opacity-30">
                {{ selectedProject.category }}
              </span>
              <span class="text-gray-400 text-sm">{{ selectedProject.year }}</span>
            </div>
            
            <h2 class="text-3xl font-bold text-white mb-4">{{ selectedProject.name }}</h2>
            <p class="text-gray-300 text-lg leading-relaxed">{{ selectedProject.fullDescription }}</p>
            
            <div class="flex gap-4 mt-6">
              <a 
                v-if="selectedProject.github" 
                :href="selectedProject.github" 
                target="_blank"
                class="px-6 py-3 bg-blue-500 hover:bg-blue-600 text-white rounded-lg font-medium transition-colors duration-300 flex items-center gap-2"
              >
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                </svg>
                View Code
              </a>
              <a 
                v-if="selectedProject.demo" 
                :href="selectedProject.demo" 
                target="_blank"
                class="px-6 py-3 border border-blue-500 text-blue-400 hover:bg-blue-500 hover:text-white rounded-lg font-medium transition-colors duration-300 flex items-center gap-2"
              >
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"></path>
                </svg>
                Live Demo
              </a>
            </div>
          </div>
        </div>

        <!-- Technologies Used -->
        <div class="mb-8">
          <h3 class="text-xl font-semibold text-white mb-4">Technologies Used</h3>
          <div class="flex flex-wrap gap-3">
            <span 
              v-for="tech in selectedProject.technologies" 
              :key="tech"
              class="px-4 py-2 bg-blue-500 bg-opacity-10 text-blue-400 rounded-lg border border-blue-500 border-opacity-30 font-medium"
            >
              {{ tech }}
            </span>
          </div>
        </div>

        <!-- Key Features -->
        <div>
          <h3 class="text-xl font-semibold text-white mb-4">Key Features</h3>
          <div class="grid md:grid-cols-2 gap-4">
            <div 
              v-for="feature in selectedProject.features" 
              :key="feature"
              class="flex items-center gap-3 p-3 bg-[#2a2a2b] rounded-lg border border-[#383838]"
            >
              <div class="w-2 h-2 bg-blue-400 rounded-full flex-shrink-0"></div>
              <span class="text-gray-300">{{ feature }}</span>
            </div>
          </div>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<style scoped>
/* Project Card Animations */
.project-card {
  animation: fadeInUp 0.6s ease-out;
}

.project-card:nth-child(1) { animation-delay: 0.1s; }
.project-card:nth-child(2) { animation-delay: 0.2s; }
.project-card:nth-child(3) { animation-delay: 0.3s; }
.project-card:nth-child(4) { animation-delay: 0.4s; }
.project-card:nth-child(5) { animation-delay: 0.5s; }
.project-card:nth-child(6) { animation-delay: 0.6s; }

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

/* Modal Animation */
.modal-enter-active, .modal-leave-active {
  transition: opacity 0.3s ease;
}

.modal-enter-from, .modal-leave-to {
  opacity: 0;
}

.modal-content-enter-active, .modal-content-leave-active {
  transition: all 0.3s ease;
}

.modal-content-enter-from, .modal-content-leave-to {
  opacity: 0;
  transform: scale(0.9) translateY(20px);
}

/* Enhanced Hover Effects */
.project-card .group:hover .bg-gradient-to-br {
  background: linear-gradient(135deg, #2563eb, #1d4ed8);
}

/* Scrollbar for modal */
.overflow-y-auto::-webkit-scrollbar {
  width: 6px;
}

.overflow-y-auto::-webkit-scrollbar-track {
  background: #1a1a1b;
  border-radius: 3px;
}

.overflow-y-auto::-webkit-scrollbar-thumb {
  background: linear-gradient(to bottom, #3b82f6, #2563eb);
  border-radius: 3px;
}

.overflow-y-auto::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(to bottom, #2563eb, #1d4ed8);
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .project-card {
    animation-delay: 0s !important;
  }
}
</style>