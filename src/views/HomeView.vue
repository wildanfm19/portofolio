<template>
  <main class="relative overflow-hidden min-h-screen flex items-center justify-center">
    <!-- Animated Background -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="floating-shapes">
        <div class="shape shape-1"></div>
        <div class="shape shape-2"></div>
        <div class="shape shape-3"></div>
        <div class="shape shape-4"></div>
        <div class="shape shape-5"></div>
      </div>
    </div>
    
    <!-- Main Content -->
    <div class="relative z-10 container mx-auto px-6 flex flex-col-reverse gap-12 items-center md:flex-row md:gap-20 md:justify-between">
      
      <!-- Text Content -->
      <div class="flex-1 text-center md:text-left space-y-6 hero-text">
        <!-- Greeting -->
        <div class="greeting">
          <span class="text-blue-400 text-lg font-medium tracking-wider">Hello everyone, I'm</span>
        </div>
        
        <!-- Main Name -->
        <div class="name-container">
          <h1 class="name-text text-5xl md:text-7xl font-bold text-white leading-tight">
            Wildan <br>
            <span class="text-gradient">Fariezky</span> <br>
            Maaruf
          </h1>
        </div>
        
        <!-- Typewriter Effect -->
        <div class="typewriter-container py-4">
          <h2 class="typewrite text-2xl md:text-3xl font-semibold" ref="typewriter">
            <span class="wrap">{{ txt }}</span>
          </h2>
        </div>
        
        <!-- Welcome Message -->
        <div class="welcome-msg">
          <p class="text-gray-300 text-lg leading-relaxed max-w-md">
            Welcome to my portfolio website! Let's build something amazing together 
            <span class="wave">👋🏼</span>
          </p>
        </div>
        
        <!-- Action Buttons -->
        <div class="action-buttons flex flex-col sm:flex-row gap-4 mt-8">
          <button @click="scrollToPortfolio" class="btn-primary group">
            <span>View My Work</span>
            <svg class="w-5 h-5 ml-2 group-hover:translate-x-1 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
            </svg>
          </button>
          
          <a href="#" target="_blank" class="btn-cv group">
            <span>Download CV</span>
            <svg class="w-5 h-5 ml-2 group-hover:translate-y-1 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path>
            </svg>
          </a>
          
          <button @click="scrollToContact" class="btn-secondary group">
            <span>Get In Touch</span>
            <svg class="w-5 h-5 ml-2 group-hover:scale-110 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"></path>
            </svg>
          </button>
        </div>
        
        <!-- Social Media Links -->
        <div class="social-links flex justify-center md:justify-start gap-4 mt-8">
          <a href="https://github.com/wildanfm19" target="_blank" class="social-icon">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
            </svg>
          </a>
          <a href="https://www.linkedin.com/in/wildan-maaruf-1a7370305/" target="_blank" class="social-icon">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
            </svg>
          </a>
          <a href="https://instagram.com/wildnfm" target="_blank" class="social-icon">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
            </svg>
          </a>
          <a href="#" target="_blank" class="social-icon cv-link" title="Download CV">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"></path>
            </svg>
          </a>
        </div>
      </div>
      
      <!-- Profile Image -->
      <div class="flex-shrink-0 hero-image">
        <div class="image-container relative">
          <div class="image-glow"></div>
          <img 
            alt="Wildan Fariezky Maaruf" 
            class="profile-img" 
            src="/avatar.png"
          >
          <div class="image-border"></div>
        </div>
      </div>
      
    </div>

    <!-- Scroll Indicator -->
    <div class="scroll-indicator">
      <div class="scroll-arrow">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
        </svg>
      </div>
      <span class="scroll-text">Scroll to explore</span>
    </div>
  </main>
</template>

<script>
export default {
  name: 'HomeView',
  data() {
    return {
      toRotate: ["Full Stack Developer", "With Springboot", "And React"],
      period: 2000,
      txt: '',
      loopNum: 0,
      isDeleting: false,
    };
  },
  mounted() {
    this.$nextTick(() => {
      this.tick();
      this.initAnimations();
    });
  },
  methods: {
    tick() {
      let typewriter = this.$refs.typewriter;

      if (!typewriter) {
        return;
      }

      let i = this.loopNum % this.toRotate.length;
      let fullTxt = this.toRotate[i];

      this.txt = this.isDeleting ? fullTxt.substring(0, this.txt.length - 1) : fullTxt.substring(0, this.txt.length + 1);
      typewriter.innerHTML = `<span class="wrap">${this.txt}</span>`;

      let that = this;
      let delta = 150 - Math.random() * 100;

      if (this.isDeleting) {
        delta /= 2;
      }

      if (!this.isDeleting && this.txt === fullTxt) {
        delta = this.period;
        this.isDeleting = true;
      } else if (this.isDeleting && this.txt === '') {
        this.isDeleting = false;
        this.loopNum++;
        delta = 500;
      }

      setTimeout(() => {
        that.tick();
      }, delta);
    },
    scrollToPortfolio() {
      document.getElementById('portfolio')?.scrollIntoView({ 
        behavior: 'smooth',
        block: 'start'
      });
    },
    scrollToContact() {
      document.getElementById('contact')?.scrollIntoView({ 
        behavior: 'smooth',
        block: 'start'
      });
    },
    initAnimations() {
      // Stagger animations for better visual impact
      const elements = document.querySelectorAll('.hero-text > *');
      elements.forEach((el, index) => {
        el.style.opacity = '0';
        el.style.transform = 'translateY(30px)';
        el.style.transition = 'opacity 0.8s ease-out, transform 0.8s ease-out';
        
        setTimeout(() => {
          el.style.opacity = '1';
          el.style.transform = 'translateY(0)';
        }, (index + 1) * 200);
      });
    }
  }
}
</script>

<style scoped>
/* Floating Background Shapes */
.floating-shapes {
  position: absolute;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: 1;
}

.shape {
  position: absolute;
  opacity: 0.1;
  border-radius: 50%;
  background: linear-gradient(45deg, #3b82f6, #2563eb);
  animation: float 6s ease-in-out infinite;
}

.shape-1 {
  width: 200px;
  height: 200px;
  top: 10%;
  left: 10%;
  animation-delay: 0s;
}

.shape-2 {
  width: 150px;
  height: 150px;
  top: 70%;
  right: 10%;
  animation-delay: 2s;
}

.shape-3 {
  width: 100px;
  height: 100px;
  top: 40%;
  left: 80%;
  animation-delay: 4s;
}

.shape-4 {
  width: 120px;
  height: 120px;
  top: 20%;
  right: 30%;
  animation-delay: 1s;
}

.shape-5 {
  width: 80px;
  height: 80px;
  bottom: 20%;
  left: 20%;
  animation-delay: 3s;
}

@keyframes float {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
  }
  50% {
    transform: translateY(-20px) rotate(180deg);
  }
}

/* Text Gradient */
.text-gradient {
  background: linear-gradient(135deg, #3b82f6 0%, #2563eb 50%, #1d4ed8 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: gradientShift 3s ease-in-out infinite;
}

@keyframes gradientShift {
  0%, 100% {
    filter: hue-rotate(0deg);
  }
  50% {
    filter: hue-rotate(20deg);
  }
}

/* Typewriter Effect */
.typewrite {
  color: #3b82f6;
  font-weight: 600;
  letter-spacing: 0.5px;
}

.typewrite > .wrap {
  border-right: 0.08em solid #3b82f6;
  animation: blink 1s infinite;
}

@keyframes blink {
  0%, 50% {
    border-color: #3b82f6;
  }
  51%, 100% {
    border-color: transparent;
  }
}

/* Buttons */
.btn-primary {
  padding: 1rem 2rem;
  background: linear-gradient(to right, #3b82f6, #2563eb);
  color: white;
  font-weight: 600;
  border-radius: 9999px;
  display: flex;
  align-items: center;
  justify-content: center;
  transform: scale(1);
  transition: all 0.3s ease;
  border: none;
  cursor: pointer;
}

.btn-primary:hover {
  transform: scale(1.05);
  box-shadow: 0 25px 50px -12px rgba(59, 130, 246, 0.5);
}

.btn-cv {
  padding: 1rem 2rem;
  background: linear-gradient(135deg, #10b981, #059669);
  color: white;
  font-weight: 600;
  border-radius: 9999px;
  display: flex;
  align-items: center;
  justify-content: center;
  transform: scale(1);
  transition: all 0.3s ease;
  border: none;
  cursor: pointer;
  text-decoration: none;
  position: relative;
  overflow: hidden;
}

.btn-cv::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: left 0.5s;
}

.btn-cv:hover {
  transform: scale(1.05);
  box-shadow: 0 25px 50px -12px rgba(16, 185, 129, 0.5);
  background: linear-gradient(135deg, #059669, #047857);
}

.btn-cv:hover::before {
  left: 100%;
}

.btn-secondary {
  padding: 1rem 2rem;
  border: 2px solid #3b82f6;
  color: #3b82f6;
  font-weight: 600;
  border-radius: 9999px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: transparent;
  cursor: pointer;
  transition: all 0.3s ease;
  transform: scale(1);
}

.btn-secondary:hover {
  background: #3b82f6;
  color: white;
  transform: scale(1.05);
}

/* Social Icons */
.social-icon {
  width: 3rem;
  height: 3rem;
  background: #1f2937;
  border: 1px solid #374151;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #9ca3af;
  transition: all 0.3s ease;
  text-decoration: none;
}

.social-icon:hover {
  border-color: #3b82f6;
  color: #3b82f6;
  transform: scale(1.1);
  background: rgba(59, 130, 246, 0.1);
  box-shadow: 0 10px 25px -5px rgba(59, 130, 246, 0.2);
}

/* Special styling for CV link */
.cv-link {
  position: relative;
  background: linear-gradient(135deg, #1f2937, #374151) !important;
  border: 2px solid #6b7280 !important;
}

.cv-link:hover {
  border-color: #10b981 !important;
  color: #10b981 !important;
  background: rgba(16, 185, 129, 0.1) !important;
  box-shadow: 0 10px 25px -5px rgba(16, 185, 129, 0.3) !important;
}

.cv-link::after {
  content: 'CV';
  position: absolute;
  bottom: -8px;
  right: -8px;
  background: linear-gradient(135deg, #10b981, #059669);
  color: white;
  font-size: 0.6rem;
  font-weight: bold;
  padding: 2px 4px;
  border-radius: 4px;
  opacity: 0;
  transform: scale(0.8);
  transition: all 0.3s ease;
}

.cv-link:hover::after {
  opacity: 1;
  transform: scale(1);
}

/* Profile Image */
.hero-image {
  animation: heroImageFloat 6s ease-in-out infinite;
}

@keyframes heroImageFloat {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
}

.image-container {
  position: relative;
  width: 320px;
  height: 320px;
}

.image-glow {
  position: absolute;
  inset: -20px;
  background: linear-gradient(45deg, #3b82f6, #2563eb, #1d4ed8);
  border-radius: 50%;
  filter: blur(20px);
  opacity: 0.6;
  animation: pulseGlow 2s ease-in-out infinite;
}

@keyframes pulseGlow {
  0%, 100% {
    opacity: 0.6;
    transform: scale(1);
  }
  50% {
    opacity: 0.8;
    transform: scale(1.05);
  }
}

.profile-img {
  position: relative;
  z-index: 2;
  width: 100%;
  height: 100%;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid #3b82f6;
  box-shadow: 
    0 0 50px rgba(59, 130, 246, 0.4),
    0 0 100px rgba(59, 130, 246, 0.2);
}

.image-border {
  position: absolute;
  inset: -8px;
  border: 2px solid transparent;
  border-radius: 50%;
  background: linear-gradient(45deg, #3b82f6, transparent, #3b82f6) border-box;
  mask: linear-gradient(#fff 0 0) padding-box, linear-gradient(#fff 0 0);
  mask-composite: subtract;
  animation: rotateBorder 4s linear infinite;
}

@keyframes rotateBorder {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/* Wave Animation */
.wave {
  animation-name: wave-animation;
  animation-duration: 2.5s;
  animation-iteration-count: infinite;
  transform-origin: 70% 70%;
  display: inline-block;
  font-size: 1.2em;
}

@keyframes wave-animation {
  0% { transform: rotate(0deg) }
  10% { transform: rotate(14deg) }
  20% { transform: rotate(-8deg) }
  30% { transform: rotate(14deg) }
  40% { transform: rotate(-4deg) }
  50% { transform: rotate(10deg) }
  60% { transform: rotate(0deg) }
  100% { transform: rotate(0deg) }
}

/* Scroll Indicator */
.scroll-indicator {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  color: #3b82f6;
  animation: bounce 2s infinite;
}

.scroll-arrow {
  opacity: 0.7;
}

.scroll-text {
  font-size: 0.9rem;
  opacity: 0.8;
  font-weight: 500;
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% {
    transform: translateX(-50%) translateY(0);
  }
  40% {
    transform: translateX(-50%) translateY(-10px);
  }
  60% {
    transform: translateX(-50%) translateY(-5px);
  }
}

/* Name Text Animation */
.name-text {
  line-height: 1.1;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

/* Responsive Design */
@media (max-width: 768px) {
  .image-container {
    width: 280px;
    height: 280px;
  }
  
  .name-text {
    font-size: 2.5rem !important;
  }
  
  .typewrite {
    font-size: 1.5rem !important;
  }
  
  .shape {
    opacity: 0.05;
  }
  
  .action-buttons {
    flex-direction: column;
    width: 100%;
  }
  
  .btn-primary, .btn-cv, .btn-secondary {
    width: 100%;
    justify-content: center;
    padding: 0.875rem 1.5rem;
  }
}

/* Enhanced Animations */
.greeting {
  animation: slideInLeft 0.8s ease-out;
}

.name-container {
  animation: slideInUp 1s ease-out 0.2s both;
}

.typewriter-container {
  animation: slideInUp 1s ease-out 0.4s both;
}

.welcome-msg {
  animation: slideInLeft 1s ease-out 0.6s both;
}

.action-buttons {
  animation: slideInUp 1s ease-out 0.8s both;
}

.social-links {
  animation: slideInUp 1s ease-out 1s both;
}

@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
