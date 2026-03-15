<!DOCTYPE html>
<html lang="tr" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>INEXX | Software Engineer & Founder</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Phosphor Icons -->
    <script src="https://unpkg.com/@phosphor-icons/web"></script>
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        dark: '#050505',
                        darker: '#000000',
                        neon: '#00f2fe',
                        neonPurple: '#4facfe',
                        surface: '#111111',
                        surfaceHover: '#1a1a1a'
                    },
                    fontFamily: {
                        sans: ['Inter', 'ui-sans-serif', 'system-ui', 'sans-serif'],
                        mono: ['Fira Code', 'ui-monospace', 'SFMono-Regular', 'monospace'],
                    },
                    animation: {
                        'blob': 'blob 7s infinite',
                        'fade-in-up': 'fadeInUp 0.8s ease-out forwards',
                    },
                    keyframes: {
                        blob: {
                            '0%': { transform: 'translate(0px, 0px) scale(1)' },
                            '33%': { transform: 'translate(30px, -50px) scale(1.1)' },
                            '66%': { transform: 'translate(-20px, 20px) scale(0.9)' },
                            '100%': { transform: 'translate(0px, 0px) scale(1)' },
                        },
                        fadeInUp: {
                            '0%': { opacity: '0', transform: 'translateY(20px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Background Pattern */
        body {
            background-color: #050505;
            background-image: linear-gradient(rgba(255, 255, 255, 0.03) 1px, transparent 1px),
            linear-gradient(90deg, rgba(255, 255, 255, 0.03) 1px, transparent 1px);
            background-size: 30px 30px;
            color: #e5e5e5;
            overflow-x: hidden;
        }

        /* Glassmorphism utilities */
        .glass {
            background: rgba(17, 17, 17, 0.7);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        /* Neon Glow Effects */
        .glow-text {
            text-shadow: 0 0 20px rgba(0, 242, 254, 0.5);
        }
        
        .glow-border:hover {
            box-shadow: 0 0 25px rgba(0, 242, 254, 0.2);
            border-color: rgba(0, 242, 254, 0.5);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #000;
        }
        ::-webkit-scrollbar-thumb {
            background: #333;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #00f2fe;
        }

        /* Utility for delayed animations */
        .delay-100 { animation-delay: 100ms; }
        .delay-200 { animation-delay: 200ms; }
        .delay-300 { animation-delay: 300ms; }
    </style>
</head>
<body class="antialiased selection:bg-neon selection:text-darker min-h-screen flex flex-col">

    <!-- Ambient Background Glows -->
    <div class="fixed inset-0 z-[-1] overflow-hidden pointer-events-none">
        <div class="absolute top-0 left-1/4 w-96 h-96 bg-neonPurple/20 rounded-full mix-blend-screen filter blur-[100px] opacity-50 animate-blob"></div>
        <div class="absolute top-1/4 right-1/4 w-96 h-96 bg-neon/20 rounded-full mix-blend-screen filter blur-[100px] opacity-50 animate-blob animation-delay-2000"></div>
        <div class="absolute -bottom-32 left-1/2 w-96 h-96 bg-purple-500/20 rounded-full mix-blend-screen filter blur-[100px] opacity-50 animate-blob animation-delay-4000"></div>
    </div>

    <!-- Navigation -->
    <nav class="fixed w-full z-50 glass border-b border-white/5 transition-all duration-300" id="navbar">
        <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold tracking-tighter text-white flex items-center gap-2">
                <i class="ph-fill ph-lightning text-neon"></i>
                INEXX
            </a>
            <div class="hidden md:flex gap-8 text-sm font-medium text-gray-400">
                <a href="#about" class="hover:text-neon transition-colors">About</a>
                <a href="#projects" class="hover:text-neon transition-colors">Projects</a>
                <a href="#stack" class="hover:text-neon transition-colors">Tech Stack</a>
            </div>
            <a href="https://github.com/INEXX-max" target="_blank" class="px-5 py-2 rounded-full bg-white/5 hover:bg-white/10 border border-white/10 text-white text-sm font-medium transition-all flex items-center gap-2 glow-border">
                <i class="ph ph-github-logo text-lg"></i>
                GitHub
            </a>
        </div>
    </nav>

    <!-- Hero Section -->
    <main class="flex-grow pt-32 pb-16 px-6">
        <div class="max-w-6xl mx-auto">
            
            <header class="py-20 flex flex-col items-start md:items-center md:text-center animate-fade-in-up">
                <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-neon/10 border border-neon/20 text-neon text-xs font-mono mb-6">
                    <span class="w-2 h-2 rounded-full bg-neon animate-pulse"></span>
                    Founder @ INEXX INTERACTIVE
                </div>
                <h1 class="text-5xl md:text-7xl font-extrabold text-white tracking-tight leading-tight mb-6">
                    Building <span class="text-transparent bg-clip-text bg-gradient-to-r from-neon to-neonPurple glow-text">High-Performance</span><br /> Gaming Ecosystems.
                </h1>
                <p class="text-lg md:text-xl text-gray-400 max-w-2xl leading-relaxed mb-10">
                    I am a software engineer focused on robust architectures. From managing daily Fedora Linux environments to writing a custom C++ game engine, my goal is to build software that scales perfectly.
                </p>
                <div class="flex flex-wrap gap-4">
                    <a href="#projects" class="px-8 py-3 rounded-lg bg-neon text-darker font-bold hover:bg-white transition-colors flex items-center gap-2 shadow-[0_0_20px_rgba(0,242,254,0.3)]">
                        View Projects <i class="ph-bold ph-arrow-down-right"></i>
                    </a>
                    <a href="#stack" class="px-8 py-3 rounded-lg glass text-white font-medium hover:bg-white/10 transition-colors flex items-center gap-2">
                        Tech Stack
                    </a>
                </div>
            </header>

            <!-- Projects Section -->
            <section id="projects" class="py-20 animate-fade-in-up delay-100 opacity-0" style="animation-fill-mode: forwards;">
                <div class="flex items-center gap-4 mb-12">
                    <h2 class="text-3xl font-bold text-white">Featured Projects</h2>
                    <div class="h-px bg-gradient-to-r from-neon/50 to-transparent flex-grow"></div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <!-- Project 1 -->
                    <div class="glass p-6 rounded-2xl glow-border transition-all duration-300 group hover:-translate-y-2 cursor-pointer flex flex-col h-full">
                        <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-neon/20 to-neonPurple/20 flex items-center justify-center mb-6 text-neon border border-neon/20 group-hover:scale-110 transition-transform">
                            <i class="ph-fill ph-game-controller text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-2">XIX Platform</h3>
                        <p class="text-sm text-neon mb-4 font-mono">Next-Gen Game Distribution</p>
                        <p class="text-gray-400 text-sm leading-relaxed mb-6 flex-grow">
                            Architecting a full-stack infrastructure (Steam Competitor) designed to support millions of players while offering better revenue models for developers.
                        </p>
                        <div class="flex gap-2 mt-auto">
                            <span class="px-2 py-1 text-xs rounded bg-white/5 text-gray-300 border border-white/5">React</span>
                            <span class="px-2 py-1 text-xs rounded bg-white/5 text-gray-300 border border-white/5">Node.js</span>
                            <span class="px-2 py-1 text-xs rounded bg-white/5 text-gray-300 border border-white/5">Architecture</span>
                        </div>
                    </div>

                    <!-- Project 2 -->
                    <div class="glass p-6 rounded-2xl glow-border transition-all duration-300 group hover:-translate-y-2 cursor-pointer flex flex-col h-full">
                        <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-yellow-500/20 to-orange-500/20 flex items-center justify-center mb-6 text-yellow-500 border border-yellow-500/20 group-hover:scale-110 transition-transform">
                            <i class="ph-fill ph-trophy text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-2">NEXEN</h3>
                        <p class="text-sm text-yellow-500 mb-4 font-mono">Competitive Matchmaking</p>
                        <p class="text-gray-400 text-sm leading-relaxed mb-6 flex-grow">
                            Developing a high-performance, algorithmic matchmaking system (Faceit Competitor) for fair, latency-optimized competitive gameplay.
                        </p>
                        <div class="flex gap-2 mt-auto">
                            <span class="px-2 py-1 text-xs rounded bg-white/5 text-gray-300 border border-white/5">Algorithms</span>
                            <span class="px-2 py-1 text-xs rounded bg-white/5 text-gray-300 border border-white/5">Java</span>
                            <span class="px-2 py-1 text-xs rounded bg-white/5 text-gray-300 border border-white/5">Spring Boot</span>
                        </div>
                    </div>

                    <!-- Project 3 -->
                    <div class="glass p-6 rounded-2xl glow-border transition-all duration-300 group hover:-translate-y-2 cursor-pointer flex flex-col h-full">
                        <div class="w-12 h-12 rounded-lg bg-gradient-to-br from-purple-500/20 to-pink-500/20 flex items-center justify-center mb-6 text-purple-400 border border-purple-500/20 group-hover:scale-110 transition-transform">
                            <i class="ph-fill ph-cpu text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-2">Custom Game Engine</h3>
                        <p class="text-sm text-purple-400 mb-4 font-mono">Hardware Architecture</p>
                        <p class="text-gray-400 text-sm leading-relaxed mb-6 flex-grow">
                            Writing my own game engine from scratch. Building the foundation to understand low-level hardware interactions and rendering systems.
                        </p>
                        <div class="flex gap-2 mt-auto">
                            <span class="px-2 py-1 text-xs rounded bg-white/5 text-gray-300 border border-white/5">C++</span>
                            <span class="px-2 py-1 text-xs rounded bg-white/5 text-gray-300 border border-white/5">Low-level</span>
                            <span class="px-2 py-1 text-xs rounded bg-white/5 text-gray-300 border border-white/5">Rendering</span>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Tech Stack Section -->
            <section id="stack" class="py-20 animate-fade-in-up delay-200 opacity-0" style="animation-fill-mode: forwards;">
                <div class="flex items-center gap-4 mb-12">
                    <h2 class="text-3xl font-bold text-white">Tech Stack & Arsenal</h2>
                    <div class="h-px bg-gradient-to-r from-neon/50 to-transparent flex-grow"></div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <!-- Backend -->
                    <div class="glass p-8 rounded-2xl border border-white/5">
                        <div class="flex items-center gap-3 mb-6">
                            <i class="ph ph-hard-drives text-2xl text-neon"></i>
                            <h3 class="text-lg font-bold text-white">Backend & Architecture</h3>
                        </div>
                        <div class="flex flex-wrap gap-3">
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300 hover:border-neon/50 transition-colors">Java (Spring Boot)</span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300 hover:border-neon/50 transition-colors">Node.js</span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300 hover:border-neon/50 transition-colors">Python (AI/ML)</span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300 hover:border-neon/50 transition-colors">C++</span>
                        </div>
                    </div>

                    <!-- Frontend -->
                    <div class="glass p-8 rounded-2xl border border-white/5">
                        <div class="flex items-center gap-3 mb-6">
                            <i class="ph ph-browser text-2xl text-neonPurple"></i>
                            <h3 class="text-lg font-bold text-white">Frontend</h3>
                        </div>
                        <div class="flex flex-wrap gap-3">
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300 hover:border-neonPurple/50 transition-colors">React</span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300 hover:border-neonPurple/50 transition-colors">Next.js</span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300 hover:border-neonPurple/50 transition-colors">Tailwind CSS</span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300 hover:border-neonPurple/50 transition-colors">JavaScript / TS</span>
                        </div>
                    </div>

                    <!-- Systems -->
                    <div class="glass p-8 rounded-2xl border border-white/5 md:col-span-2">
                        <div class="flex items-center gap-3 mb-6">
                            <i class="ph ph-terminal-window text-2xl text-green-400"></i>
                            <h3 class="text-lg font-bold text-white">Systems & Environment</h3>
                        </div>
                        <div class="flex flex-wrap gap-3">
                            <span class="px-4 py-2 rounded-lg bg-surface border border-green-400/20 text-sm font-medium text-green-400">
                                <i class="ph-fill ph-linux-logo mr-1"></i> Fedora Linux (Daily Driver)
                            </span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300">System Administration</span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300">Git / GitHub</span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300">IntelliJ IDEA</span>
                            <span class="px-4 py-2 rounded-lg bg-surface border border-white/10 text-sm font-medium text-gray-300">VS Code</span>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="glass border-t border-white/5 mt-auto">
        <div class="max-w-6xl mx-auto px-6 py-8 flex flex-col md:flex-row justify-between items-center gap-4">
            <div class="flex items-center gap-2">
                <i class="ph-fill ph-lightning text-neon"></i>
                <span class="text-white font-bold tracking-tight">INEXX INTERACTIVE</span>
            </div>
            <p class="text-sm text-gray-500">© 2026 INEXX. Hustle & Code.</p>
            <div class="flex gap-4">
                <a href="https://github.com/INEXX-max" target="_blank" class="w-10 h-10 rounded-full bg-surface border border-white/10 flex items-center justify-center text-gray-400 hover:text-white hover:border-white/30 transition-all">
                    <i class="ph-fill ph-github-logo text-xl"></i>
                </a>
                <a href="https://www.linkedin.com/in/muhammed-inan%C3%A7-b3702a3a7" target="_blank" class="w-10 h-10 rounded-full bg-surface border border-white/10 flex items-center justify-center text-gray-400 hover:text-[#0a66c2] hover:border-[#0a66c2]/50 transition-all">
                    <i class="ph-fill ph-linkedin-logo text-xl"></i>
                </a>
            </div>
        </div>
    </footer>

    <!-- Navbar scroll effect script -->
    <script>
        window.addEventListener('scroll', () => {
            const nav = document.getElementById('navbar');
            if (window.scrollY > 20) {
                nav.classList.add('bg-dark/80', 'shadow-lg', 'shadow-neon/5');
            } else {
                nav.classList.remove('bg-dark/80', 'shadow-lg', 'shadow-neon/5');
            }
        });
    </script>
</body>
</html>
