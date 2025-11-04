<template>
  <!-- component -->
  <!-- This is an example component -->
  <div class="max-w-7xl mx-auto flex flex-col relative">

    <nav class="max-w-7xl px-5 md:fixed top-0 z-[98] w-screen backdrop-blur-md bg-[#121212] bg-opacity-80 transition-opacity duration-300" :class="{ 'opacity-0 pointer-events-none': isModalOpen }">
      <div class="container mx-auto flex flex-wrap items-center justify-between">
        <button @click="redirectToHome" class="flex">
          <span class="self-center text-lg text-blue-400 font-semibold whitespace-nowrap fadein-bot hover:text-blue-300">Portofolio</span>
        </button>
        <div class="flex md:order-2 fadein-bot">
          <a href="https://github.com/wildanfm19"><img class="w-9 rounded-full" src="https://seeklogo.com/images/G/github-logo-2E3852456C-seeklogo.com.png" alt="github"></a>
        </div>
        <div class="hidden md:flex justify-between items-center w-full md:w-auto md:order-1" id="mobile-menu-3">
          <ul class="flex-col md:flex-row flex md:space-x-8 mt-4 md:mt-0 md:text-sm md:font-medium">
            <li>
              <a @click="scrollToSection('home')"
                class="fadein-bot text-gray-700 hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0 cursor-pointer"
                aria-current="page">Home</a>
            </li>
            <li>
              <a @click="scrollToSection('about')"
                class="fadein-bot fadein-1 text-gray-700 hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0 cursor-pointer">About</a>
            </li>
            <li>
              <a @click="scrollToSection('portfolio')"
                class="fadein-bot fadein-2 text-gray-700 hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0 cursor-pointer">Portfolio</a>
            </li>
            <li>
              <a @click="scrollToSection('contact')"
                class="fadein-bot fadein-3 text-gray-700 hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0 cursor-pointer">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div>
      <!-- Home Section -->
      <section id="home" class="min-h-screen pt-16 md:pt-20 fade-in">
        <HomeView />
      </section>
      
      <!-- About Section -->
      <section id="about" class="min-h-screen pt-16 md:pt-20 fade-in">
        <AboutView />
      </section>
      
      <!-- Portfolio Section -->
      <section id="portfolio" class="min-h-screen fade-in">
        <PortfolioView @modal-opened="handleModalOpened" @modal-closed="handleModalClosed" @open-project-modal="openProjectModal" />
      </section>
      
      <!-- Contact Section -->
      <section id="contact" class="min-h-screen pt-16 md:pt-20 fade-in">
        <!-- Enhanced Contact Section -->
        <div class="bg-gradient-to-br from-[#1a1a1b] via-[#1e1e1f] to-[#252526] px-5 py-8 md:px-12 md:py-12 text-left border border-[#383838] rounded-3xl text-blue-50 mx-3 mb-8 relative overflow-hidden">
          <!-- Background decoration -->
          <div class="absolute top-0 right-0 w-64 h-64 bg-blue-500 bg-opacity-5 rounded-full blur-3xl -translate-y-32 translate-x-32"></div>
          <div class="absolute bottom-0 left-0 w-48 h-48 bg-blue-400 bg-opacity-3 rounded-full blur-2xl translate-y-24 -translate-x-24"></div>
          
          <div class="relative z-10">
            <!-- Header -->
            <header class="text-center mb-12">
              <h2 class="text-3xl md:text-4xl font-bold text-white mb-4 fade-in">
                Let's Connect
              </h2>
              <p class="text-lg md:text-xl text-gray-400 fade-in">
                Ready to bring your ideas to life? Let's start a conversation!
              </p>
              <div class="h-[2px] w-24 bg-gradient-to-r from-blue-400 to-blue-600 rounded-full mx-auto mt-6"></div>
            </header>
            
            <!-- Contact Methods -->
            <div class="grid md:grid-cols-2 gap-8 mb-12">
              <!-- Direct Contact -->
              <div class="space-y-6">
                <h3 class="text-2xl font-semibold text-white mb-6 flex items-center gap-3">
                  <div class="w-8 h-8 bg-blue-500 bg-opacity-20 rounded-lg flex items-center justify-center">
                    <svg class="w-5 h-5 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path>
                    </svg>
                  </div>
                  Get In Touch
                </h3>
                
                <!-- Email Cards -->
                <a href="mailto:wildanfm19@gmail.com" class="block group">
                  <div class="bg-gradient-to-r from-[#2a2a2b] to-[#252526] p-6 rounded-xl border border-[#383838] hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105">
                    <div class="flex items-center gap-4">
                      <div class="w-12 h-12 bg-red-500 bg-opacity-20 rounded-lg flex items-center justify-center group-hover:bg-opacity-30 transition-colors">
                        <svg class="w-6 h-6 text-red-400" fill="currentColor" viewBox="0 0 24 24">
                          <path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-.904.732-1.636 1.636-1.636h3.819l6.545 4.91 6.545-4.91h3.819A1.636 1.636 0 0 1 24 5.457z"/>
                        </svg>
                      </div>
                      <div>
                        <h4 class="text-white font-semibold">Personal Email</h4>
                        <p class="text-gray-400 text-sm">dracko.maaruftm@gmail.com</p>
                      </div>
                    </div>
                  </div>
                </a>

                <a href="mailto:wildan.maaruf@binus.ac.id" class="block group">
                  <div class="bg-gradient-to-r from-[#2a2a2b] to-[#252526] p-6 rounded-xl border border-[#383838] hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105">
                    <div class="flex items-center gap-4">
                      <div class="w-12 h-12 bg-blue-500 bg-opacity-20 rounded-lg flex items-center justify-center group-hover:bg-opacity-30 transition-colors">
                        <svg class="w-6 h-6 text-blue-400" fill="currentColor" viewBox="0 0 24 24">
                          <path d="M7.25 2A5.25 5.25 0 002 7.25v9.5A5.25 5.25 0 007.25 22h9.5A5.25 5.25 0 0022 16.75v-9.5A5.25 5.25 0 0016.75 2h-9.5z"/>
                          <path fill="white" d="M6 8h12v8H6z"/>
                        </svg>
                      </div>
                      <div>
                        <h4 class="text-white font-semibold">University Email</h4>
                        <p class="text-gray-400 text-sm">wildan.maaruf@binus.ac.id</p>
                      </div>
                    </div>
                  </div>
                </a>
              </div>

              <!-- Social Media -->
              <div class="space-y-6">
                <h3 class="text-2xl font-semibold text-white mb-6 flex items-center gap-3">
                  <div class="w-8 h-8 bg-blue-500 bg-opacity-20 rounded-lg flex items-center justify-center">
                    <svg class="w-5 h-5 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M9 19l3 3m0 0l3-3m-3 3V10"></path>
                    </svg>
                  </div>
                  Follow Me
                </h3>
                
                <div class="space-y-3">
                  <!-- LinkedIn -->
                  <a href="https://www.linkedin.com/in/wildan-maaruf-1a7370305/" target="_blank" class="flex items-center gap-4 p-4 bg-gradient-to-r from-[#2a2a2b] to-[#252526] rounded-lg border border-[#383838] hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105 group">
                    <div class="w-10 h-10 bg-blue-600 bg-opacity-20 rounded-lg flex items-center justify-center group-hover:bg-opacity-30 transition-colors">
                      <svg class="w-5 h-5 text-blue-400" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                      </svg>
                    </div>
                    <div>
                      <span class="text-white font-medium">LinkedIn</span>
                      <p class="text-gray-400 text-sm">Professional Network</p>
                    </div>
                  </a>

                  <!-- GitHub -->
                  <a href="https://github.com/wildanfm19" target="_blank" class="flex items-center gap-4 p-4 bg-gradient-to-r from-[#2a2a2b] to-[#252526] rounded-lg border border-[#383838] hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105 group">
                    <div class="w-10 h-10 bg-gray-600 bg-opacity-20 rounded-lg flex items-center justify-center group-hover:bg-opacity-30 transition-colors">
                      <svg class="w-5 h-5 text-gray-400" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                      </svg>
                    </div>
                    <div>
                      <span class="text-white font-medium">GitHub</span>
                      <p class="text-gray-400 text-sm">Code Repository</p>
                    </div>
                  </a>

                  <!-- Instagram -->
                  <a href="https://instagram.com/wildnfm" target="_blank" class="flex items-center gap-4 p-4 bg-gradient-to-r from-[#2a2a2b] to-[#252526] rounded-lg border border-[#383838] hover:border-blue-400 transition-all duration-300 hover:transform hover:scale-105 group">
                    <div class="w-10 h-10 bg-pink-500 bg-opacity-20 rounded-lg flex items-center justify-center group-hover:bg-opacity-30 transition-colors">
                      <svg class="w-5 h-5 text-pink-400" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                      </svg>
                    </div>
                    <div>
                      <span class="text-white font-medium">Instagram</span>
                      <p class="text-gray-400 text-sm">Personal Updates</p>
                    </div>
                  </a>
                </div>
              </div>
            </div>

            <!-- Call to Action -->
            <div class="text-center bg-gradient-to-r from-[#2a2a2b] to-[#252526] p-8 rounded-2xl border border-[#383838]">
              <h3 class="text-2xl font-bold text-white mb-4">Ready to Start Your Project?</h3>
              <p class="text-gray-300 mb-6 max-w-2xl mx-auto">
                Whether you need a web application, mobile app, or technical consultation, 
                I'm here to help bring your vision to life. Let's discuss your project!
              </p>
              <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="mailto:dracko.maaruftm@gmail.com" class="px-8 py-4 bg-blue-500 hover:bg-blue-600 text-white font-semibold rounded-xl transition-all duration-300 hover:transform hover:scale-105 flex items-center justify-center gap-2">
                  <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 4.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
                  </svg>
                  Send Message
                </a>
                <a href="https://www.linkedin.com/in/wildan-maaruf-1a7370305/" target="_blank" class="px-8 py-4 border-2 border-blue-500 text-blue-400 hover:bg-blue-500 hover:text-white font-semibold rounded-xl transition-all duration-300 hover:transform hover:scale-105 flex items-center justify-center gap-2">
                  <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                  </svg>
                  Connect on LinkedIn
                </a>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
    
    <!-- Global Project Detail Modal -->
    <transition 
      enter-active-class="transition-all duration-300 ease-out"
      leave-active-class="transition-all duration-200 ease-in"
      enter-from-class="opacity-0 scale-95"
      enter-to-class="opacity-100 scale-100"
      leave-from-class="opacity-100 scale-100"
      leave-to-class="opacity-0 scale-95"
    >
      <div 
        v-if="showProjectModal && selectedProject" 
        class="fixed top-0 left-0 w-full h-full z-[9999] bg-black bg-opacity-75 backdrop-blur-sm"
        @click="closeProjectModal"
        style="margin: 0 !important; padding: 0 !important;"
      >
        <div class="flex items-center justify-center min-h-full p-4">
          <div 
            class="bg-gradient-to-br from-[#1e1e1f] to-[#252526] border border-[#383838] rounded-2xl max-w-4xl w-full max-h-[90vh] overflow-y-auto relative shadow-2xl mx-auto"
            @click.stop
          >
            <!-- Close Button -->
            <button 
              @click="closeProjectModal"
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
      </div>
    </transition>
  </div>
  <footer class="block md:hidden fixed bottom-0 left-0 right-0 rounded-t-3xl border border-[#383838] bg-[#121212] bg-opacity-80 backdrop-blur-md backdrop-opacity-90 transition-opacity duration-300" :class="{ 'opacity-0 pointer-events-none': isModalOpen }">
  <nav class="flex justify-around py-4 text-xs">
    <a @click="scrollToSection('home')" class="text-gray-300 hover:text-white cursor-pointer">Home</a>
    <a @click="scrollToSection('about')" class="text-gray-300 hover:text-white cursor-pointer">About</a>
    <a @click="scrollToSection('portfolio')" class="text-gray-300 hover:text-white cursor-pointer">Portfolio</a>
    <a @click="scrollToSection('contact')" class="text-gray-300 hover:text-white cursor-pointer">Contact</a>
  </nav>
</footer>
</template>

<script>
import HomeView from './views/HomeView.vue'
import AboutView from './views/AboutView.vue'
import PortfolioView from './views/PortfolioView.vue'

export default {
  components: {
    HomeView,
    AboutView,
    PortfolioView
  },
  data() {
    return {
      isModalOpen: false,
      showProjectModal: false,
      selectedProject: null
    }
  },
  mounted() {
    this.initScrollAnimations()
    // Add keyboard event listener for ESC key
    document.addEventListener('keydown', this.handleEscapeKey);
  },
  unmounted() {
    // Clean up event listener
    document.removeEventListener('keydown', this.handleEscapeKey);
    // Restore body scroll if component is unmounted while modal is open
    document.body.style.overflow = 'auto';
  },
  methods: {
    redirectToHome() {
      this.scrollToSection('home')
    },
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId)
      if (element) {
        const navbarHeight = 80 // Reduced navbar height offset
        const elementPosition = element.offsetTop
        const offsetPosition = elementPosition - navbarHeight

        window.scrollTo({
          top: offsetPosition,
          behavior: 'smooth'
        })
      }
    },
    handleModalOpened() {
      this.isModalOpen = true;
    },
    handleModalClosed() {
      this.isModalOpen = false;
    },
    openProjectModal(project) {
      this.selectedProject = project;
      this.showProjectModal = true;
      this.isModalOpen = true;
      document.body.style.overflow = 'hidden';
    },
    closeProjectModal() {
      this.showProjectModal = false;
      this.selectedProject = null;
      this.isModalOpen = false;
      document.body.style.overflow = 'auto';
    },
    handleEscapeKey(event) {
      if (event.key === 'Escape' && this.showProjectModal) {
        this.closeProjectModal();
      }
    },
    initScrollAnimations() {
      const observerOptions = {
        threshold: 0.2,
        rootMargin: '0px 0px -100px 0px'
      }

      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add('is-visible')
          } else {
            // Remove class when scrolling away to trigger animation again
            entry.target.classList.remove('is-visible')
          }
        })
      }, observerOptions)

      // Observe all fade-in elements
      const fadeElements = document.querySelectorAll('.fade-in')
      fadeElements.forEach(element => {
        observer.observe(element)
      })
    }
  },
}
</script>

<style>
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

::-webkit-scrollbar {
  width: 5px; /* for vertical scrollbar */
  height: 5px; /* for horizontal scrollbar */
}

::-webkit-scrollbar-track {
  background: hsl(240, 1%, 17%);
  border-radius: 5px;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(to bottom, #3b82f6, #2563eb);
  border-radius: 5px;
}

::-webkit-scrollbar-button { width: 20px; }

body {
  font-family: 'Poppins', sans-serif;
  background: hsl(0, 0%, 7%);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  scroll-behavior: smooth;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  transition: color 0.3s;
}

nav a.router-link-exact-active {
  display: inline-flex;
  flex-direction: column;
  color: white;
  transition: color 0.3s;
}

nav a.router-link-exact-active::after {
  display: inline-block;
  content: "";
  margin-top: 0.08em;
  width: 100%;
  height: 4px;
  border-radius: 2px;
  background-color: #3b82f6;
}

nav a.router-link-exact-active:hover {
  color: white;
}


@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

/* Simple Fade-in animations */
.fade-in {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}

.fade-in.is-visible {
  opacity: 1;
  transform: translateY(0);
}

</style>
