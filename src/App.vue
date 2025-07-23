<template>
  <div class="min-h-screen transition-colors duration-300" :class="darkMode ? 'dark bg-dark-900' : 'bg-white'">
    <!-- Header/Navigation -->
    <header class="fixed top-0 left-0 right-0 backdrop-blur-sm border-b z-50 transition-colors duration-300" 
            :class="darkMode ? 'bg-dark-900/90 border-dark-700' : 'bg-white/90 border-gray-200'">
      <nav class="section-container">
        <div class="flex items-center justify-between h-16">
          <div class="flex items-center">
            <!-- Logo or brand could go here -->
          </div>
          <div class="hidden md:block">
            <div class="ml-10 flex items-baseline space-x-8">
              <a href="#about" class="px-3 py-2 text-sm font-medium transition-colors hover:text-primary-400" 
                 :class="darkMode ? 'text-gray-300' : 'text-gray-700'">
                About
              </a>
              <a href="#experience" class="px-3 py-2 text-sm font-medium transition-colors hover:text-primary-400" 
                 :class="darkMode ? 'text-gray-300' : 'text-gray-700'">
                Experience
              </a>
              <a href="#skills" class="px-3 py-2 text-sm font-medium transition-colors hover:text-primary-400" 
                 :class="darkMode ? 'text-gray-300' : 'text-gray-700'">
                Skills
              </a>
              <a href="#contact" class="px-3 py-2 text-sm font-medium transition-colors hover:text-primary-400" 
                 :class="darkMode ? 'text-gray-300' : 'text-gray-700'">
                Contact
              </a>
            </div>
          </div>
          <div class="flex items-center space-x-4">
            <!-- Dark Mode Toggle -->
            <button
              @click="toggleDarkMode"
              class="p-2 rounded-lg transition-colors duration-300 hover:bg-opacity-20"
              :class="darkMode ? 'text-gray-300 hover:bg-white' : 'text-gray-700 hover:bg-gray-200'"
              :title="darkMode ? 'Switch to light mode' : 'Switch to dark mode'"
            >
              <Sun v-if="darkMode" class="h-5 w-5" />
              <Moon v-else class="h-5 w-5" />
            </button>
            <button 
              @click="mobileMenuOpen = !mobileMenuOpen"
              class="md:hidden inline-flex items-center justify-center p-2 rounded-md transition-colors focus:outline-none focus:ring-2 focus:ring-inset focus:ring-primary-500"
              :class="darkMode ? 'text-gray-300 hover:text-primary-400 hover:bg-dark-800' : 'text-gray-700 hover:text-primary-600 hover:bg-gray-100'"
            >
              <Menu class="h-6 w-6" />
            </button>
          </div>
        </div>
        <!-- Mobile menu -->
        <div v-if="mobileMenuOpen" class="md:hidden">
          <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 border-t transition-colors duration-300"
               :class="darkMode ? 'bg-dark-900 border-dark-700' : 'bg-white border-gray-200'">
            <a href="#about" @click="mobileMenuOpen = false" 
               class="block px-3 py-2 text-base font-medium transition-colors hover:text-primary-400"
               :class="darkMode ? 'text-gray-300' : 'text-gray-700'">About</a>
            <a href="#experience" @click="mobileMenuOpen = false" 
               class="block px-3 py-2 text-base font-medium transition-colors hover:text-primary-400"
               :class="darkMode ? 'text-gray-300' : 'text-gray-700'">Experience</a>
            <a href="#skills" @click="mobileMenuOpen = false" 
               class="block px-3 py-2 text-base font-medium transition-colors hover:text-primary-400"
               :class="darkMode ? 'text-gray-300' : 'text-gray-700'">Skills</a>
            <a href="#contact" @click="mobileMenuOpen = false" 
               class="block px-3 py-2 text-base font-medium transition-colors hover:text-primary-400"
               :class="darkMode ? 'text-gray-300' : 'text-gray-700'">Contact</a>
          </div>
        </div>
      </nav>
    </header>

    <!-- Hero Section -->
    <section class="pt-20 pb-16 lg:pt-28 lg:pb-24 gradient-bg">
      <div class="section-container">
        <div class="text-center animate-fade-in">
          <h1 class="text-5xl lg:text-7xl font-jetbrains font-bold text-white mb-8 tracking-wide">
            José Quirós Montenegro
          </h1>
          <p class="text-2xl lg:text-3xl text-white/90 mb-16 font-light tracking-wider">
            Software Engineer / Java Developer
          </p>
          <div class="flex flex-col sm:flex-row gap-6 justify-center">
            <a href="#contact" class="btn-primary bg-white text-primary-700 hover:bg-gray-50 shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
              <Mail class="w-5 h-5 mr-2" />
              Get In Touch
            </a>
            <a href="/ResumeJoseQuiros.pdf" download="Jose_Quiros_Resume.pdf" class="btn-secondary bg-green-600 border-green-600 text-white hover:bg-green-700 hover:border-green-700 shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
              <Download class="w-5 h-5 mr-2" />
              Download CV
            </a>
            <a href="https://www.linkedin.com/in/josé-alberto-quirós-montenegro" target="_blank" class="btn-secondary bg-blue-600 border-blue-600 text-white hover:bg-blue-700 hover:border-blue-700 shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
              <Linkedin class="w-5 h-5 mr-2" />
              LinkedIn
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section-padding transition-colors duration-300" :class="darkMode ? 'bg-dark-800' : 'bg-gray-50'">
      <div class="section-container">
        <div class="text-center mb-16 animate-slide-up">
          <h2 class="text-3xl lg:text-4xl font-bold mb-6 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
            About Me
          </h2>
          <div class="w-24 h-1 bg-primary-600 mx-auto mb-8"></div>
        </div>
        <div class="max-w-4xl mx-auto">
          <div class="rounded-2xl shadow-lg p-8 lg:p-12 animate-slide-up transition-colors duration-300" 
               :class="darkMode ? 'bg-dark-700' : 'bg-white'">
            <div class="grid md:grid-cols-2 gap-12 items-center">
              <div>
                <h3 class="text-2xl font-bold mb-6 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  Backend Developer
                </h3>
                <p class="leading-relaxed mb-6 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                  I'm a backend developer with 3 years of experience specialized in building, maintaining, 
                  and optimizing scalable applications. My expertise includes Java, Spring Boot, .NET, and RESTful web services.
                </p>
                <p class="leading-relaxed mb-6 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                  I have a strong understanding of software development best practices and skills to analyze and 
                  resolve production issues, providing support to critical systems and ensuring reliable performance under pressure.
                </p>
                <div class="flex items-center transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                  <MapPin class="w-5 h-5 mr-2 text-primary-600" />
                  <span>Turrialba, Cartago, Costa Rica</span>
                </div>
              </div>
              <div class="space-y-6">
                <div class="rounded-xl p-6 transition-colors duration-300" :class="darkMode ? 'bg-primary-900/30' : 'bg-primary-50'">
                  <div class="flex items-center mb-4">
                    <GraduationCap class="w-6 h-6 text-primary-600 mr-3" />
                    <h4 class="text-lg font-semibold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                      Education
                    </h4>
                  </div>
                  <div>
                    <h5 class="font-semibold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                      Bachelor of Business Informatics
                    </h5>
                    <p class="transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                      University of Costa Rica
                    </p>
                    <p class="text-sm transition-colors duration-300" :class="darkMode ? 'text-gray-400' : 'text-gray-500'">
                      2017 - 2022
                    </p>
                  </div>
                </div>
                <div class="rounded-xl p-6 transition-colors duration-300" :class="darkMode ? 'bg-green-900/30' : 'bg-green-50'">
                  <div class="flex items-center mb-4">
                    <Award class="w-6 h-6 text-green-600 mr-3" />
                    <h4 class="text-lg font-semibold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                      Certifications
                    </h4>
                  </div>
                  <div>
                    <h5 class="font-semibold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                      Scrum Foundation Professional Certificate
                    </h5>
                    <p class="transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                      CertiProf
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="section-padding transition-colors duration-300" :class="darkMode ? 'bg-dark-900' : 'bg-white'">
      <div class="section-container">
        <div class="text-center mb-16 animate-fade-in-up">
          <h2 class="text-3xl lg:text-4xl font-bold mb-6 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
            Professional Experience
          </h2>
          <div class="w-24 h-1 bg-primary-600 mx-auto mb-8 pulse-glow"></div>
        </div>
        <div class="max-w-4xl mx-auto">
          <div class="space-y-12">
            <!-- Experience Item 1 -->
            <div class="experience-card rounded-2xl shadow-lg p-8 animate-fade-in-left animate-stagger-1 transition-colors duration-300" 
                 :class="darkMode ? 'bg-dark-800' : 'bg-white'">
              <div class="flex flex-col lg:flex-row lg:items-center lg:justify-between mb-6">
                <div>
                  <h3 class="text-xl font-bold mb-2 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                    Backend Developer
                  </h3>
                  <p class="text-primary-600 font-semibold mb-2">NearLinx</p>
                </div>
                <div class="flex items-center transition-colors duration-300" :class="darkMode ? 'text-gray-400' : 'text-gray-500'">
                  <Calendar class="w-4 h-4 mr-2 icon-float" />
                  <span>Jan 2025 - Present</span>
                </div>
              </div>
              <p class="leading-relaxed mb-4 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                Designed and implemented backend features using Java Spring Boot and SQL, resolving bugs and 
                writing unit/integration tests to ensure code quality.
              </p>
              <div class="mb-6">
                <h4 class="font-semibold mb-3 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  Key Responsibilities:
                </h4>
                <ul class="list-disc list-inside space-y-2 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                  <li>Refactored stored procedures and optimized database queries to improve performance</li>
                  <li>Led database cleanup and normalization initiatives</li>
                  <li>Applied SQL best practices and consistent conventions</li>
                  <li>Utilized Cursor with various AI models for development and migration tasks</li>
                </ul>
              </div>
              <div class="flex flex-wrap gap-3">
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">Java Spring Boot</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">SQL Server</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">JUnit</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">Azure DevOps</span>
              </div>
            </div>

            <!-- Experience Item 2 -->
            <div class="experience-card rounded-2xl shadow-lg p-8 animate-fade-in-right animate-stagger-2 transition-colors duration-300" 
                 :class="darkMode ? 'bg-dark-800' : 'bg-white'">
              <div class="flex flex-col lg:flex-row lg:items-center lg:justify-between mb-6">
                <div>
                  <h3 class="text-xl font-bold mb-2 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                    Support Software Developer
                  </h3>
                  <p class="text-primary-600 font-semibold mb-2">NearLinx</p>
                </div>
                <div class="flex items-center transition-colors duration-300" :class="darkMode ? 'text-gray-400' : 'text-gray-500'">
                  <Calendar class="w-4 h-4 mr-2 icon-float" />
                  <span>Nov 2023 - Dec 2024</span>
                </div>
              </div>
              <p class="leading-relaxed mb-4 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                Diagnosed and resolved production issues, including application bugs and data errors.
              </p>
              <div class="mb-6">
                <h4 class="font-semibold mb-3 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  Key Achievements:
                </h4>
                <ul class="list-disc list-inside space-y-2 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                  <li>Fixed data inconsistencies and generated missing records</li>
                  <li>Automated recurring billing and provisioning tasks with Python and SQL</li>
                  <li>Contributed to performance investigations</li>
                </ul>
              </div>
              <div class="flex flex-wrap gap-3">
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">Java Spring Boot</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">Python</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">SQL Server</span>
              </div>
            </div>

            <!-- Experience Item 3 -->
            <div class="experience-card rounded-2xl shadow-lg p-8 animate-fade-in-left animate-stagger-3 transition-colors duration-300" 
                 :class="darkMode ? 'bg-dark-800' : 'bg-white'">
              <div class="flex flex-col lg:flex-row lg:items-center lg:justify-between mb-6">
                <div>
                  <h3 class="text-xl font-bold mb-2 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                    Software Developer
                  </h3>
                  <p class="text-primary-600 font-semibold mb-2">NearLinx</p>
                </div>
                <div class="flex items-center transition-colors duration-300" :class="darkMode ? 'text-gray-400' : 'text-gray-500'">
                  <Calendar class="w-4 h-4 mr-2 icon-float" />
                  <span>Dec 2022 - Nov 2023</span>
                </div>
              </div>
              <p class="leading-relaxed mb-6 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                Developed a web application using a low-code platform, enhancing its capabilities through custom JavaScript and SQL scripts. 
                Managed user support requests, ensuring SLA compliance. Collaborated directly with clients to analyze problems and deliver appropriate solutions.
              </p>
              <div class="flex flex-wrap gap-3">
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">Low-code platform</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">Microsoft SQL Server</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">GitLab</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">JavaScript</span>
              </div>
            </div>

            <!-- Experience Item 4 -->
            <div class="experience-card rounded-2xl shadow-lg p-8 animate-fade-in-right animate-stagger-4 transition-colors duration-300" 
                 :class="darkMode ? 'bg-dark-800' : 'bg-white'">
              <div class="flex flex-col lg:flex-row lg:items-center lg:justify-between mb-6">
                <div>
                  <h3 class="text-xl font-bold mb-2 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                    Full Stack Developer
                  </h3>
                  <p class="text-primary-600 font-semibold mb-2">NearLinx</p>
                </div>
                <div class="flex items-center transition-colors duration-300" :class="darkMode ? 'text-gray-400' : 'text-gray-500'">
                  <Calendar class="w-4 h-4 mr-2 icon-float" />
                  <span>Jul 2022 - Dec 2022</span>
                </div>
              </div>
              <p class="leading-relaxed mb-4 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                Built RESTful APIs with ASP.NET and developed responsive front-end interfaces using Vue.js.
              </p>
              <div class="mb-6">
                <h4 class="font-semibold mb-3 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  Technologies used:
                </h4>
                <ul class="list-disc list-inside space-y-2 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
                  <li>Database access management via Entity Framework and LINQ</li>
                  <li>Unit/integration testing implementation with NUnit, Moq, and Jest</li>
                  <li>CI/CD pipeline configuration with GitHub Actions for Azure deployments</li>
                </ul>
              </div>
              <div class="flex flex-wrap gap-3">
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">ASP.NET</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">Vue.js</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">Entity Framework</span>
                <span class="tech-badge-animated px-3 py-2 rounded-full text-sm font-medium border transition-all duration-300" :class="darkMode ? 'bg-primary-900/50 text-primary-300 border-primary-700' : 'bg-primary-100 text-primary-800 border-primary-200'">GitHub Actions</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section-padding transition-colors duration-300" :class="darkMode ? 'bg-dark-800' : 'bg-gray-50'">
      <div class="section-container">
        <div class="text-center mb-16 animate-slide-up">
          <h2 class="text-3xl lg:text-4xl font-bold mb-6 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
            Technical Skills
          </h2>
          <div class="w-24 h-1 bg-primary-600 mx-auto mb-8"></div>
        </div>
        <div class="max-w-6xl mx-auto">
          <!-- Skills Grid -->
          <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6 mb-12">
            <!-- Backend Skills -->
            <div class="rounded-2xl shadow-lg p-6 card-hover animate-slide-in-left transition-colors duration-300" 
                 :class="darkMode ? 'bg-dark-700' : 'bg-white'">
              <div class="flex items-center mb-4">
                <Server class="w-8 h-8 text-primary-600 mr-3" />
                <h3 class="text-lg font-bold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  Backend
                </h3>
              </div>
              <div class="space-y-3">
                <div v-for="skill in backendSkills" :key="skill" 
                     class="px-3 py-2 rounded-lg text-center font-medium transition-colors duration-300"
                     :class="darkMode ? 'bg-primary-900/30 text-primary-300' : 'bg-primary-100 text-primary-800'">
                  {{ skill }}
                </div>
              </div>
            </div>

            <!-- Database Skills -->
            <div class="rounded-2xl shadow-lg p-6 card-hover animate-slide-up transition-colors duration-300" 
                 :class="darkMode ? 'bg-dark-700' : 'bg-white'">
              <div class="flex items-center mb-4">
                <Database class="w-8 h-8 text-primary-600 mr-3" />
                <h3 class="text-lg font-bold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  Databases
                </h3>
              </div>
              <div class="space-y-3">
                <div v-for="skill in databaseSkills" :key="skill" 
                     class="px-3 py-2 rounded-lg text-center font-medium transition-colors duration-300"
                     :class="darkMode ? 'bg-blue-900/30 text-blue-300' : 'bg-blue-100 text-blue-800'">
                  {{ skill }}
                </div>
              </div>
            </div>

            <!-- Tools Skills -->
            <div class="rounded-2xl shadow-lg p-6 card-hover animate-slide-in-right transition-colors duration-300" 
                 :class="darkMode ? 'bg-dark-700' : 'bg-white'">
              <div class="flex items-center mb-4">
                <Settings class="w-8 h-8 text-primary-600 mr-3" />
                <h3 class="text-lg font-bold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  Tools
                </h3>
              </div>
              <div class="space-y-3">
                <div v-for="skill in toolsSkills" :key="skill" 
                     class="px-3 py-2 rounded-lg text-center font-medium transition-colors duration-300"
                     :class="darkMode ? 'bg-green-900/30 text-green-300' : 'bg-green-100 text-green-800'">
                  {{ skill }}
                </div>
              </div>
            </div>

            <!-- Frameworks & Libraries -->
            <div class="rounded-2xl shadow-lg p-6 card-hover animate-slide-in-left transition-colors duration-300" 
                 :class="darkMode ? 'bg-dark-700' : 'bg-white'">
              <div class="flex items-center mb-4">
                <Code class="w-8 h-8 text-primary-600 mr-3" />
                <h3 class="text-lg font-bold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  Frameworks
                </h3>
              </div>
              <div class="space-y-3">
                <div v-for="skill in frameworkSkills" :key="skill" 
                     class="px-3 py-2 rounded-lg text-center font-medium transition-colors duration-300"
                     :class="darkMode ? 'bg-purple-900/30 text-purple-300' : 'bg-purple-100 text-purple-800'">
                  {{ skill }}
                </div>
              </div>
            </div>
          </div>

          <!-- Additional Skills -->
          <div class="rounded-2xl shadow-lg p-8 animate-slide-up transition-colors duration-300" 
               :class="darkMode ? 'bg-dark-700' : 'bg-white'">
            <h3 class="text-xl font-bold mb-6 text-center transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
              Additional Competencies
            </h3>
            <div class="grid md:grid-cols-2 gap-8">
              <div>
                <h4 class="font-semibold mb-4 flex items-center transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  <Globe class="w-5 h-5 mr-2 text-primary-600" />
                  Languages
                </h4>
                <div class="space-y-3">
                  <div class="flex justify-between items-center">
                    <span class="transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-700'">Spanish</span>
                    <span class="px-3 py-1 bg-green-100 text-green-800 text-sm rounded-full dark:bg-green-900/30 dark:text-green-300">Native</span>
                  </div>
                  <div class="flex justify-between items-center">
                    <span class="transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-700'">English</span>
                    <span class="px-3 py-1 bg-blue-100 text-blue-800 text-sm rounded-full dark:bg-blue-900/30 dark:text-blue-300">Intermediate</span>
                  </div>
                </div>
              </div>
              <div>
                <h4 class="font-semibold mb-4 flex items-center transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  <Users class="w-5 h-5 mr-2 text-primary-600" />
                  Methodologies
                </h4>
                <div class="flex flex-wrap gap-2">
                  <span v-for="method in methodologies" :key="method"
                        class="px-3 py-1 rounded-full text-sm font-medium transition-colors duration-300"
                        :class="darkMode ? 'bg-primary-900/50 text-primary-300 border border-primary-700' : 'bg-primary-100 text-primary-800 border border-primary-200'">
                    {{ method }}
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section-padding transition-colors duration-300" :class="darkMode ? 'bg-dark-900' : 'bg-gray-50'">
      <div class="section-container">
        <div class="text-center mb-16 animate-slide-up">
          <h2 class="text-3xl lg:text-4xl font-bold mb-6 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
            Contact
          </h2>
          <div class="w-24 h-1 bg-primary-600 mx-auto mb-8"></div>
          <p class="text-xl max-w-2xl mx-auto transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-600'">
            Interested in working together? I'd love to hear about your project.
          </p>
        </div>
        <div class="max-w-4xl mx-auto">
          <div class="grid md:grid-cols-2 gap-12">
            <div class="animate-slide-in-left">
              <h3 class="text-2xl font-bold mb-8 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                Contact Information
              </h3>
              <div class="space-y-6">
                <div class="flex items-center">
                  <div class="flex items-center justify-center w-12 h-12 bg-primary-100 dark:bg-primary-900/50 rounded-lg mr-4">
                    <Mail class="w-6 h-6 text-primary-600" />
                  </div>
                  <div>
                    <h4 class="font-semibold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">Email</h4>
                    <a href="mailto:jqm.25@hotmail.es" class="text-primary-600 hover:text-primary-700 transition-colors">
                      jqm.25@hotmail.es
                    </a>
                  </div>
                </div>
                <div class="flex items-center">
                  <div class="flex items-center justify-center w-12 h-12 bg-primary-100 dark:bg-primary-900/50 rounded-lg mr-4">
                    <Phone class="w-6 h-6 text-primary-600" />
                  </div>
                  <div>
                    <h4 class="font-semibold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">Phone</h4>
                    <a href="tel:+50685584070" class="text-primary-600 hover:text-primary-700 transition-colors">
                      +506 8558-4070
                    </a>
                  </div>
                </div>
                <div class="flex items-center">
                  <div class="flex items-center justify-center w-12 h-12 bg-primary-100 dark:bg-primary-900/50 rounded-lg mr-4">
                    <MapPin class="w-6 h-6 text-primary-600" />
                  </div>
                  <div>
                    <h4 class="font-semibold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">Location</h4>
                    <p class="text-primary-600">Turrialba, Cartago, Costa Rica</p>
                  </div>
                </div>
                <div class="flex items-center">
                  <div class="flex items-center justify-center w-12 h-12 bg-primary-100 dark:bg-primary-900/50 rounded-lg mr-4">
                    <Linkedin class="w-6 h-6 text-primary-600" />
                  </div>
                  <div>
                    <h4 class="font-semibold transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">LinkedIn</h4>
                    <a 
                      href="https://www.linkedin.com/in/josé-alberto-quirós-montenegro" 
                      target="_blank"
                      class="text-primary-600 hover:text-primary-700 transition-colors"
                    >
                      View Profile
                    </a>
                  </div>
                </div>
              </div>
            </div>
            <div class="animate-slide-in-right">
              <div class="rounded-2xl shadow-lg p-8 transition-colors duration-300" :class="darkMode ? 'bg-dark-800' : 'bg-white'">
                <h3 class="text-xl font-bold mb-6 transition-colors duration-300" :class="darkMode ? 'text-white' : 'text-gray-900'">
                  Send a Message
                </h3>
                <form @submit.prevent="handleSubmit" class="space-y-6">
                  <div>
                    <label for="subject" class="block text-sm font-medium mb-2 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-700'">
                      Subject
                    </label>
                    <input
                      type="text"
                      id="subject"
                      v-model="form.subject"
                      required
                      class="w-full px-4 py-3 border rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-colors duration-300"
                      :class="darkMode ? 'bg-dark-700 border-dark-600 text-white placeholder-gray-400' : 'bg-white border-gray-300 text-gray-900 placeholder-gray-500'"
                      placeholder="What's this about?"
                    />
                  </div>
                  <div>
                    <label for="message" class="block text-sm font-medium mb-2 transition-colors duration-300" :class="darkMode ? 'text-gray-300' : 'text-gray-700'">
                      Message
                    </label>
                    <textarea
                      id="message"
                      v-model="form.message"
                      required
                      rows="6"
                      class="w-full px-4 py-3 border rounded-lg focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-colors duration-300"
                      :class="darkMode ? 'bg-dark-700 border-dark-600 text-white placeholder-gray-400' : 'bg-white border-gray-300 text-gray-900 placeholder-gray-500'"
                      placeholder="Tell me about your project or inquiry..."
                    ></textarea>
                  </div>
                  <button type="submit" class="w-full btn-primary">
                    <Send class="w-5 h-5 mr-2" />
                    Send Message
                  </button>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="py-8 transition-colors duration-300" :class="darkMode ? 'bg-dark-800 text-white' : 'bg-dark-800 text-white'">
      <div class="section-container">
        <div class="text-center">
          <div class="flex justify-center space-x-6 mb-6">
            <a 
              href="mailto:jqm.25@hotmail.es" 
              class="text-gray-400 hover:text-white transition-colors"
              title="Email"
            >
              <Mail class="w-5 h-5" />
            </a>
            <a 
              href="https://www.linkedin.com/in/josé-alberto-quirós-montenegro" 
              target="_blank"
              class="text-gray-400 hover:text-white transition-colors"
              title="LinkedIn"
            >
              <Linkedin class="w-5 h-5" />
            </a>
          </div>
          <p class="text-gray-400 text-sm">
            © {{ currentYear }} José Quirós Montenegro
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { ref, computed, onMounted } from 'vue'
import { 
  Menu, Mail, Linkedin, MapPin, Phone, Send,
  Calendar, GraduationCap, Award, Server, Database, 
  Code, Settings, Globe, Users, Sun, Moon, Download
} from 'lucide-vue-next'

// Reactive data
const mobileMenuOpen = ref(false)
const darkMode = ref(false)
const form = ref({
  subject: '',
  message: ''
})

// Skills data - New simplified format
const backendSkills = ref([
  'Java', 'Spring Boot', '.NET Core', 'ASP.NET', 'Python', 'REST APIs', 'Microservices'
])

const databaseSkills = ref([
  'SQL Server', 'MySQL', 'T-SQL', 'Entity Framework', 'LINQ'
])

const toolsSkills = ref([
  'Git', 'Azure DevOps', 'Visual Studio', 'Postman', 'Cursor AI', 'Docker'
])

const frameworkSkills = ref([
  'Spring Boot', 'Vue.js', 'Entity Framework', 'NUnit', 'Jest', 'Cypress'
])

const methodologies = ref([
  'Scrum', 'Kanban', 'Agile', 'CI/CD', 'Testing', 'TDD'
])

// Computed
const currentYear = computed(() => new Date().getFullYear())

// Methods
const toggleDarkMode = () => {
  darkMode.value = !darkMode.value
  localStorage.setItem('darkMode', darkMode.value.toString())
}

const handleSubmit = () => {
  // Create mailto link with form data
  const subject = encodeURIComponent(form.value.subject)
  const body = encodeURIComponent(form.value.message)
  
  window.location.href = `mailto:jqm.25@hotmail.es?subject=${subject}&body=${body}`
  
  // Reset form
  form.value = {
    subject: '',
    message: ''
  }
}

// Lifecycle
onMounted(() => {
  // Load dark mode preference
  const savedDarkMode = localStorage.getItem('darkMode')
  if (savedDarkMode !== null) {
    darkMode.value = savedDarkMode === 'true'
  } else {
    // Check system preference
    darkMode.value = window.matchMedia('(prefers-color-scheme: dark)').matches
  }

  // Add smooth scrolling for navigation links
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault()
      const target = document.querySelector(this.getAttribute('href'))
      if (target) {
        target.scrollIntoView({
          behavior: 'smooth',
          block: 'start'
        })
      }
    })
  })
})
</script>

<style scoped>
.tech-badge-dark {
  @apply inline-flex items-center px-3 py-1 rounded-full text-sm font-medium border transition-colors duration-300;
}
</style> 