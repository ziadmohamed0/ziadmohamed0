<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ziad Mohamed Fathy - Mechatronics & Embedded Systems Engineer</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        'dark-bg': '#181818',
                    },
                    fontFamily: {
                        'tech': ['Courier New', 'monospace'],
                    },
                    animation: {
                        'fade-in': 'fadeIn 0.6s ease-in-out',
                        'slide-up': 'slideUp 0.6s ease-out',
                        'pulse-slow': 'pulse 3s infinite',
                        'circuit': 'circuit 4s ease-in-out infinite',
                    },
                    keyframes: {
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' },
                        },
                        slideUp: {
                            '0%': { transform: 'translateY(30px)', opacity: '0' },
                            '100%': { transform: 'translateY(0)', opacity: '1' },
                        },
                        circuit: {
                            '0%, 100%': { strokeDashoffset: '0' },
                            '50%': { strokeDashoffset: '20' },
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .circuit-pattern {
            background-image: 
                linear-gradient(90deg, rgba(93, 92, 222, 0.1) 1px, transparent 1px),
                linear-gradient(rgba(93, 92, 222, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #5D5CDE, #00D4FF);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .tech-border {
            position: relative;
        }
        
        .tech-border::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            border: 2px solid transparent;
            background: linear-gradient(45deg, #5D5CDE, #00D4FF, #5D5CDE) border-box;
            -webkit-mask: linear-gradient(#fff 0 0) padding-box, linear-gradient(#fff 0 0);
            -webkit-mask-composite: exclude;
            border-radius: inherit;
        }
        
        .project-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .dark .project-card {
            background: rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .skill-icon {
            transition: all 0.3s ease;
        }
        
        .skill-icon:hover {
            transform: translateY(-5px) scale(1.05);
        }
    </style>
</head>
<body class="bg-white dark:bg-dark-bg text-gray-900 dark:text-white transition-colors duration-300">
    <!-- Navigation -->
    <nav class="fixed top-0 w-full bg-white/80 dark:bg-dark-bg/80 backdrop-blur-md z-50 border-b border-gray-200 dark:border-gray-700">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="font-bold text-xl gradient-text">ZMF</div>
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="hover:text-primary transition-colors">Home</a>
                    <a href="#about" class="hover:text-primary transition-colors">About</a>
                    <a href="#skills" class="hover:text-primary transition-colors">Skills</a>
                    <a href="#projects" class="hover:text-primary transition-colors">Projects</a>
                    <a href="#education" class="hover:text-primary transition-colors">Education</a>
                    <a href="#experience" class="hover:text-primary transition-colors">Experience</a>
                    <a href="#contact" class="hover:text-primary transition-colors">Contact</a>
                </div>
                <button id="mobile-menu-btn" class="md:hidden p-2">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white dark:bg-dark-bg border-t border-gray-200 dark:border-gray-700">
            <div class="px-2 pt-2 pb-3 space-y-1">
                <a href="#home" class="block px-3 py-2 hover:text-primary transition-colors">Home</a>
                <a href="#about" class="block px-3 py-2 hover:text-primary transition-colors">About</a>
                <a href="#skills" class="block px-3 py-2 hover:text-primary transition-colors">Skills</a>
                <a href="#projects" class="block px-3 py-2 hover:text-primary transition-colors">Projects</a>
                <a href="#education" class="block px-3 py-2 hover:text-primary transition-colors">Education</a>
                <a href="#experience" class="block px-3 py-2 hover:text-primary transition-colors">Experience</a>
                <a href="#contact" class="block px-3 py-2 hover:text-primary transition-colors">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="min-h-screen flex items-center justify-center relative overflow-hidden circuit-pattern">
        <!-- Animated Circuit Background -->
        <div class="absolute inset-0 opacity-20">
            <svg class="w-full h-full" viewBox="0 0 1000 1000">
                <path d="M100,100 L200,100 L200,200 L400,200 L400,400 L600,400 L600,300 L800,300" 
                      stroke="#5D5CDE" stroke-width="2" fill="none" 
                      stroke-dasharray="10,5" class="animate-circuit"/>
                <path d="M100,500 L300,500 L300,700 L500,700 L500,600 L700,600 L700,800" 
                      stroke="#00D4FF" stroke-width="2" fill="none" 
                      stroke-dasharray="8,4" class="animate-circuit" style="animation-delay: 1s"/>
                <circle cx="200" cy="100" r="4" fill="#5D5CDE" class="animate-pulse-slow"/>
                <circle cx="400" cy="200" r="4" fill="#00D4FF" class="animate-pulse-slow" style="animation-delay: 0.5s"/>
                <circle cx="600" cy="400" r="4" fill="#5D5CDE" class="animate-pulse-slow" style="animation-delay: 1.5s"/>
            </svg>
        </div>
        
        <div class="text-center z-10 px-4">
            <div class="animate-fade-in">
                <h1 class="text-5xl md:text-7xl font-bold mb-4">
                    <span class="gradient-text">Ziad Mohamed Fathy</span>
                </h1>
                <h2 class="text-2xl md:text-3xl font-light mb-6 text-gray-600 dark:text-gray-300">
                    Mechatronics & Embedded Systems Engineer
                </h2>
                <p class="text-xl md:text-2xl mb-8 font-tech text-primary">
                    Innovating IoT, Robotics, and Embedded Systems
                </p>
                <div class="flex justify-center space-x-4">
                    <a href="#projects" class="bg-primary text-white px-8 py-3 rounded-lg hover:bg-opacity-90 transition-all transform hover:scale-105">
                        View Projects
                    </a>
                    <a href="#contact" class="border border-primary text-primary px-8 py-3 rounded-lg hover:bg-primary hover:text-white transition-all">
                        Get In Touch
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 bg-gray-50 dark:bg-gray-900">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4 gradient-text">About Me</h2>
                <div class="w-24 h-1 bg-primary mx-auto"></div>
            </div>
            
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div class="space-y-6">
                    <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300">
                        I am a passionate Mechatronics and Embedded Systems Engineer with a strong foundation in robotics, IoT, and embedded technologies. My journey in engineering is driven by an insatiable curiosity and a commitment to continuous learning.
                    </p>
                    <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300">
                        As a problem-solver at heart, I thrive on tackling complex challenges and transforming innovative ideas into practical solutions. My expertise spans from low-level embedded programming to high-level robotics systems, always with a focus on creating technology that makes a meaningful impact.
                    </p>
                    <p class="text-lg leading-relaxed text-gray-700 dark:text-gray-300">
                        I believe in the power of self-learning and staying at the forefront of technological advancements. Whether it's mastering a new programming language, exploring cutting-edge robotics frameworks, or diving deep into IoT architectures, I approach each challenge with enthusiasm and determination.
                    </p>
                </div>
                
                <div class="relative">
                    <!-- Robot Avatar Placeholder -->
                    <div class="w-80 h-80 mx-auto relative">
                        <div class="absolute inset-0 bg-gradient-to-br from-primary to-blue-400 rounded-full opacity-20 animate-pulse-slow"></div>
                        <div class="absolute inset-4 bg-white dark:bg-dark-bg rounded-full border-4 border-primary flex items-center justify-center">
                            <i class="fas fa-robot text-8xl text-primary"></i>
                        </div>
                        <!-- Tech Elements -->
                        <div class="absolute top-4 right-4 w-8 h-8 bg-primary rounded-full flex items-center justify-center">
                            <i class="fas fa-microchip text-white text-sm"></i>
                        </div>
                        <div class="absolute bottom-4 left-4 w-8 h-8 bg-blue-400 rounded-full flex items-center justify-center">
                            <i class="fas fa-wifi text-white text-sm"></i>
                        </div>
                        <div class="absolute top-1/2 left-0 w-8 h-8 bg-green-400 rounded-full flex items-center justify-center">
                            <i class="fas fa-cog text-white text-sm animate-spin"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4 gradient-text">Technical Skills</h2>
                <div class="w-24 h-1 bg-primary mx-auto"></div>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Embedded Systems -->
                <div class="tech-border bg-white dark:bg-gray-800 p-6 rounded-lg">
                    <div class="text-center">
                        <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center mx-auto mb-4 skill-icon">
                            <i class="fas fa-microchip text-white text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-4">Embedded Systems</h3>
                        <div class="space-y-2 text-sm">
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">C/C++</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Python</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">STM32</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">ESP32/ESP8266</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Raspberry Pi</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">ARM Cortex-M</div>
                        </div>
                    </div>
                </div>

                <!-- Robotics -->
                <div class="tech-border bg-white dark:bg-gray-800 p-6 rounded-lg">
                    <div class="text-center">
                        <div class="w-16 h-16 bg-blue-500 rounded-full flex items-center justify-center mx-auto mb-4 skill-icon">
                            <i class="fas fa-robot text-white text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-4">Robotics</h3>
                        <div class="space-y-2 text-sm">
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">ROS2 Humble</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">ROS2 Jazzy</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">5-DOF Robotic Arm</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Mobile Robot Simulation</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Sensor Integration</div>
                        </div>
                    </div>
                </div>

                <!-- IoT -->
                <div class="tech-border bg-white dark:bg-gray-800 p-6 rounded-lg">
                    <div class="text-center">
                        <div class="w-16 h-16 bg-green-500 rounded-full flex items-center justify-center mx-auto mb-4 skill-icon">
                            <i class="fas fa-wifi text-white text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-4">IoT</h3>
                        <div class="space-y-2 text-sm">
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">MQTT</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Node-RED</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Mosquitto</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Wireless Protocols</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Cloud Integration</div>
                        </div>
                    </div>
                </div>

                <!-- Hardware -->
                <div class="tech-border bg-white dark:bg-gray-800 p-6 rounded-lg">
                    <div class="text-center">
                        <div class="w-16 h-16 bg-purple-500 rounded-full flex items-center justify-center mx-auto mb-4 skill-icon">
                            <i class="fas fa-memory text-white text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-4">Hardware</h3>
                        <div class="space-y-2 text-sm">
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">PCB Design</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Circuit Analysis</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Hardware Integration</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Sensor Networks</div>
                            <div class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full">Signal Processing</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 bg-gray-50 dark:bg-gray-900">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4 gradient-text">Featured Projects</h2>
                <div class="w-24 h-1 bg-primary mx-auto"></div>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Robotic Arm Project -->
                <div class="project-card rounded-lg p-6 transform hover:scale-105 transition-all duration-300">
                    <div class="w-full h-48 bg-gradient-to-br from-primary to-blue-500 rounded-lg mb-4 flex items-center justify-center">
                        <i class="fas fa-robot text-white text-6xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">5-DOF Robotic Arm</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">
                        Advanced robotic arm with ROS2 integration, featuring precise control, trajectory planning, and real-time manipulation capabilities.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="bg-primary text-white px-2 py-1 rounded text-xs">ROS2</span>
                        <span class="bg-primary text-white px-2 py-1 rounded text-xs">C++</span>
                        <span class="bg-primary text-white px-2 py-1 rounded text-xs">Kinematics</span>
                    </div>
                </div>

                <!-- Smart Home Project -->
                <div class="project-card rounded-lg p-6 transform hover:scale-105 transition-all duration-300">
                    <div class="w-full h-48 bg-gradient-to-br from-green-500 to-blue-500 rounded-lg mb-4 flex items-center justify-center">
                        <i class="fas fa-home text-white text-6xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Smart Home System</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">
                        IoT-enabled home automation system with MQTT communication, sensor monitoring, and mobile app control interface.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="bg-green-500 text-white px-2 py-1 rounded text-xs">IoT</span>
                        <span class="bg-green-500 text-white px-2 py-1 rounded text-xs">MQTT</span>
                        <span class="bg-green-500 text-white px-2 py-1 rounded text-xs">ESP32</span>
                    </div>
                </div>

                <!-- Glove for Deaf Project -->
                <div class="project-card rounded-lg p-6 transform hover:scale-105 transition-all duration-300">
                    <div class="w-full h-48 bg-gradient-to-br from-purple-500 to-pink-500 rounded-lg mb-4 flex items-center justify-center">
                        <i class="fas fa-hand-paper text-white text-6xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Sign Language Glove</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">
                        Wearable device that translates sign language gestures to speech, bridging communication gaps for the deaf community.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="bg-purple-500 text-white px-2 py-1 rounded text-xs">ML</span>
                        <span class="bg-purple-500 text-white px-2 py-1 rounded text-xs">Sensors</span>
                        <span class="bg-purple-500 text-white px-2 py-1 rounded text-xs">Arduino</span>
                    </div>
                </div>

                <!-- Smartwatch Project -->
                <div class="project-card rounded-lg p-6 transform hover:scale-105 transition-all duration-300">
                    <div class="w-full h-48 bg-gradient-to-br from-blue-500 to-cyan-500 rounded-lg mb-4 flex items-center justify-center">
                        <i class="fas fa-clock text-white text-6xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Custom Smartwatch</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">
                        Feature-rich smartwatch with health monitoring, connectivity, and custom firmware for optimal performance.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="bg-blue-500 text-white px-2 py-1 rounded text-xs">Embedded C</span>
                        <span class="bg-blue-500 text-white px-2 py-1 rounded text-xs">BLE</span>
                        <span class="bg-blue-500 text-white px-2 py-1 rounded text-xs">Sensors</span>
                    </div>
                </div>

                <!-- Robot Eyes Project -->
                <div class="project-card rounded-lg p-6 transform hover:scale-105 transition-all duration-300">
                    <div class="w-full h-48 bg-gradient-to-br from-orange-500 to-red-500 rounded-lg mb-4 flex items-center justify-center">
                        <i class="fas fa-eye text-white text-6xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Robotic Vision System</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">
                        Computer vision system for robots with object detection, tracking, and adaptive behavior algorithms.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="bg-orange-500 text-white px-2 py-1 rounded text-xs">OpenCV</span>
                        <span class="bg-orange-500 text-white px-2 py-1 rounded text-xs">Python</span>
                        <span class="bg-orange-500 text-white px-2 py-1 rounded text-xs">AI</span>
                    </div>
                </div>

                <!-- Mobile Robot Project -->
                <div class="project-card rounded-lg p-6 transform hover:scale-105 transition-all duration-300">
                    <div class="w-full h-48 bg-gradient-to-br from-teal-500 to-green-500 rounded-lg mb-4 flex items-center justify-center">
                        <i class="fas fa-cogs text-white text-6xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Mobile Robot Simulation</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">
                        Advanced mobile robot simulation with path planning, obstacle avoidance, and autonomous navigation capabilities.
                    </p>
                    <div class="flex flex-wrap gap-2">
                        <span class="bg-teal-500 text-white px-2 py-1 rounded text-xs">ROS2</span>
                        <span class="bg-teal-500 text-white px-2 py-1 rounded text-xs">Gazebo</span>
                        <span class="bg-teal-500 text-white px-2 py-1 rounded text-xs">SLAM</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="py-20">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4 gradient-text">Education</h2>
                <div class="w-24 h-1 bg-primary mx-auto"></div>
            </div>
            
            <div class="max-w-4xl mx-auto">
                <div class="tech-border bg-white dark:bg-gray-800 rounded-lg p-8">
                    <div class="flex items-start space-x-6">
                        <div class="w-16 h-16 bg-primary rounded-full flex items-center justify-center flex-shrink-0">
                            <i class="fas fa-graduation-cap text-white text-2xl"></i>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-2xl font-bold mb-2">Bachelor of Engineering in Mechatronics</h3>
                            <p class="text-xl text-primary mb-2">Helwan International Technology University</p>
                            <p class="text-gray-600 dark:text-gray-400 mb-4">
                                Comprehensive program covering mechanical engineering, electronics, control systems, and computer programming. 
                                Specialized in robotics, automation, and embedded systems with hands-on laboratory experience.
                            </p>
                            <div class="flex flex-wrap gap-2">
                                <span class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full text-sm">Control Systems</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full text-sm">Robotics</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full text-sm">Embedded Systems</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full text-sm">Automation</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-3 py-1 rounded-full text-sm">Signal Processing</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="py-20 bg-gray-50 dark:bg-gray-900">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4 gradient-text">Experience</h2>
                <div class="w-24 h-1 bg-primary mx-auto"></div>
            </div>
            
            <div class="space-y-8">
                <!-- AI Resident -->
                <div class="tech-border bg-white dark:bg-gray-800 rounded-lg p-6">
                    <div class="flex items-start space-x-6">
                        <div class="w-12 h-12 bg-primary rounded-full flex items-center justify-center flex-shrink-0">
                            <i class="fas fa-brain text-white"></i>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-xl font-bold mb-1">AI Resident</h3>
                            <p class="text-primary mb-2">Alingerr</p>
                            <p class="text-gray-600 dark:text-gray-400 mb-3">
                                Engaged in cutting-edge AI research and development, focusing on machine learning applications 
                                in robotics and embedded systems. Contributed to innovative AI solutions and algorithm optimization.
                            </p>
                            <div class="flex flex-wrap gap-2">
                                <span class="bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-xs">Machine Learning</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-xs">AI Research</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-xs">Algorithm Development</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- NLP Developer -->
                <div class="tech-border bg-white dark:bg-gray-800 rounded-lg p-6">
                    <div class="flex items-start space-x-6">
                        <div class="w-12 h-12 bg-blue-500 rounded-full flex items-center justify-center flex-shrink-0">
                            <i class="fas fa-language text-white"></i>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-xl font-bold mb-1">Arabic NLP Specialist</h3>
                            <p class="text-blue-500 mb-2">Outlier</p>
                            <p class="text-gray-600 dark:text-gray-400 mb-3">
                                Specialized in Arabic Natural Language Processing, developing and optimizing language models, 
                                text processing algorithms, and linguistic analysis tools for Arabic content.
                            </p>
                            <div class="flex flex-wrap gap-2">
                                <span class="bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-xs">NLP</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-xs">Arabic Language</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-xs">Text Processing</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Team Leader -->
                <div class="tech-border bg-white dark:bg-gray-800 rounded-lg p-6">
                    <div class="flex items-start space-x-6">
                        <div class="w-12 h-12 bg-green-500 rounded-full flex items-center justify-center flex-shrink-0">
                            <i class="fas fa-users text-white"></i>
                        </div>
                        <div class="flex-1">
                            <h3 class="text-xl font-bold mb-1">HR Team Leader</h3>
                            <p class="text-green-500 mb-2">Enactus</p>
                            <p class="text-gray-600 dark:text-gray-400 mb-3">
                                Led human resources initiatives for social entrepreneurship projects, managing team development, 
                                recruitment processes, and fostering collaborative environments for innovative social impact solutions.
                            </p>
                            <div class="flex flex-wrap gap-2">
                                <span class="bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-xs">Leadership</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-xs">Team Management</span>
                                <span class="bg-gray-100 dark:bg-gray-700 px-2 py-1 rounded text-xs">Social Impact</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-20">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold mb-4 gradient-text">Get In Touch</h2>
                <div class="w-24 h-1 bg-primary mx-auto mb-8"></div>
                <p class="text-xl text-gray-600 dark:text-gray-400 max-w-3xl mx-auto">
                    Ready to collaborate on innovative projects or discuss opportunities in robotics, IoT, and embedded systems? 
                    Let's connect and build the future together.
                </p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8 max-w-4xl mx-auto">
                <!-- GitHub -->
                <a href="https://github.com/ziadmohamedfathy" target="_blank" 
                   class="tech-border bg-white dark:bg-gray-800 p-6 rounded-lg text-center transform hover:scale-105 transition-all duration-300 group">
                    <div class="w-16 h-16 bg-gray-800 dark:bg-white rounded-full flex items-center justify-center mx-auto mb-4 group-hover:bg-primary transition-colors">
                        <i class="fab fa-github text-white dark:text-gray-800 group-hover:text-white text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">GitHub</h3>
                    <p class="text-gray-600 dark:text-gray-400">View my code repositories and open source contributions</p>
                </a>

                <!-- LinkedIn -->
                <a href="https://linkedin.com/in/ziadmohamedfathy" target="_blank" 
                   class="tech-border bg-white dark:bg-gray-800 p-6 rounded-lg text-center transform hover:scale-105 transition-all duration-300 group">
                    <div class="w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:bg-primary transition-colors">
                        <i class="fab fa-linkedin text-white text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">LinkedIn</h3>
                    <p class="text-gray-600 dark:text-gray-400">Connect with me for professional networking</p>
                </a>

                <!-- Email -->
                <a href="mailto:ziad.mohamed.fathy@example.com" 
                   class="tech-border bg-white dark:bg-gray-800 p-6 rounded-lg text-center transform hover:scale-105 transition-all duration-300 group">
                    <div class="w-16 h-16 bg-red-500 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:bg-primary transition-colors">
                        <i class="fas fa-envelope text-white text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-2">Email</h3>
                    <p class="text-gray-600 dark:text-gray-400">Send me a message for collaboration opportunities</p>
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 dark:bg-black text-white py-8">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="mb-4">&copy; 2024 Ziad Mohamed Fathy. All rights reserved.</p>
            <p class="text-gray-400">Innovating IoT, Robotics, and Embedded Systems</p>
        </div>
    </footer>

    <script>
        // Dark mode handling
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            if (event.matches) {
                document.documentElement.classList.add('dark');
            } else {
                document.documentElement.classList.remove('dark');
            }
        });

        // Mobile menu toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                    // Close mobile menu if open
                    mobileMenu.classList.add('hidden');
                }
            });
        });

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate-slide-up');
                }
            });
        }, observerOptions);

        // Observe all sections
        document.querySelectorAll('section').forEach(section => {
            observer.observe(section);
        });

        // Add navbar background on scroll
        window.addEventListener('scroll', () => {
            const nav = document.querySelector('nav');
            if (window.scrollY > 50) {
                nav.classList.add('bg-white/90', 'dark:bg-dark-bg/90');
            } else {
                nav.classList.remove('bg-white/90', 'dark:bg-dark-bg/90');
            }
        });

        // Typing effect for the tagline
        const tagline = document.querySelector('.font-tech');
        const text = "Innovating IoT, Robotics, and Embedded Systems";
        let index = 0;
        
        function typeEffect() {
            if (index < text.length) {
                tagline.textContent = text.slice(0, index + 1) + '|';
                index++;
                setTimeout(typeEffect, 100);
            } else {
                tagline.textContent = text;
            }
        }
        
        // Start typing effect after page load
        setTimeout(typeEffect, 2000);
    </script>
</body>
</html>
