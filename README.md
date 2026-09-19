<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MS STUDIO | Minecraft Developers</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Press+Start+2P&family=Space+Grotesk:wght@600;700;800&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Plus Jakarta Sans', sans-serif; }
        .font-heading { font-family: 'Space Grotesk', sans-serif; }
        .font-pixel { font-family: 'Press Start 2P', cursive; }
        
        /* Preloader Screen & Top Progress Line Styling */
        #preloader {
            transition: opacity 0.5s ease, visibility 0.5s ease;
        }
        .progress-line {
            width: 0%;
            animation: loadProgress 1.8s ease-in-out forwards;
        }
        @keyframes loadProgress {
            0% { width: 0%; }
            50% { width: 65%; }
            100% { width: 100%; }
        }

        #toast {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        /* Modal Backdrop Transition */
        #review-modal {
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }
    </style>
</head>
<body class="bg-[#0c0d12] text-slate-200 antialiased selection:bg-yellow-500 selection:text-slate-950 relative overflow-x-hidden">

    <!-- Top Running Loader Line -->
    <div class="fixed top-0 left-0 h-1 bg-gradient-to-r from-yellow-500 via-amber-400 to-yellow-300 z-50 progress-line shadow-[0_0_12px_rgba(234,179,8,0.8)]"></div>

    <!-- Opening Screen Overlay / Preloader -->
    <div id="preloader" class="fixed inset-0 z-50 bg-[#0c0d12] flex flex-col items-center justify-center">
        <div class="text-center px-4">
            <div class="w-16 h-16 mx-auto mb-6 rounded-2xl bg-gradient-to-b from-stone-200 to-stone-400 border-4 border-stone-800 p-2 shadow-2xl shadow-yellow-500/20 flex items-center justify-center font-pixel text-slate-900 text-base animate-bounce">
                MS
            </div>
            <h1 class="text-3xl md:text-5xl font-black text-white font-heading tracking-wider mb-2">
                MS <span class="text-yellow-400 font-pixel text-2xl md:text-3xl">STUDIO</span>
            </h1>
            <p class="text-slate-400 text-xs font-mono tracking-widest uppercase">Loading Server Systems...</p>
        </div>
    </div>

    <!-- Ambient Glows -->
    <div class="fixed top-0 left-1/4 w-[500px] h-[500px] bg-yellow-500/10 rounded-full blur-[150px] pointer-events-none"></div>
    <div class="fixed bottom-1/3 right-1/4 w-[500px] h-[500px] bg-amber-600/10 rounded-full blur-[160px] pointer-events-none"></div>

    <!-- Toast Notification -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 transform translate-y-20 opacity-0 pointer-events-none bg-yellow-400 text-slate-950 font-bold px-5 py-3 rounded-xl shadow-2xl flex items-center gap-3 border-2 border-yellow-500">
        <i class="fa-solid fa-circle-check text-lg"></i>
        <span id="toast-msg">Username copied to clipboard!</span>
    </div>

    <!-- Navigation Bar -->
    <nav class="fixed top-0 w-full z-40 bg-[#0c0d12]/85 backdrop-blur-xl border-b border-yellow-500/20">
        <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
            <a href="#" class="text-2xl font-black tracking-tight text-white flex items-center gap-3 font-heading">
                <div class="w-10 h-10 rounded-lg bg-gradient-to-b from-stone-200 to-stone-400 border-2 border-stone-800 p-1 shadow-lg shadow-yellow-500/10 flex items-center justify-center font-pixel text-slate-900 text-xs tracking-tighter">
                    MS
                </div>
                <span class="tracking-wider">MS <span class="text-yellow-400 font-pixel text-lg">STUDIO</span></span>
            </a>
            <div class="hidden md:flex items-center space-x-8 font-medium text-sm text-slate-400">
                <a href="#about" class="hover:text-yellow-400 transition-colors">About Us</a>
                <a href="#services" class="hover:text-yellow-400 transition-colors">Services</a>
                <a href="#pricing" class="hover:text-yellow-400 transition-colors">Pricing</a>
                <a href="#workflow" class="hover:text-yellow-400 transition-colors">Workflow</a>
                <a href="#reviews" class="hover:text-yellow-400 transition-colors">Reviews</a>
                <a href="#stats" class="hover:text-yellow-400 transition-colors">Stats</a>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="bg-yellow-400 hover:bg-yellow-300 text-slate-950 px-5 py-2.5 rounded-xl font-bold transition-all shadow-lg shadow-yellow-500/20 font-heading">
                    Order Now
                </a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="pt-40 pb-20 px-6 max-w-7xl mx-auto text-center relative">
        <div class="inline-flex items-center gap-2.5 px-4 py-2 rounded-full bg-slate-900/90 border border-yellow-500/30 text-yellow-400 text-xs font-semibold tracking-wide uppercase mb-8 shadow-md">
            <span class="w-2 h-2 rounded-full bg-yellow-400 animate-pulse"></span> MS STUDIO • Minecraft Development Agency
        </div>
        
        <h1 class="text-4xl sm:text-6xl md:text-7xl font-extrabold tracking-tight leading-[1.15] mb-6 font-heading text-white">
            Next-Gen Architecture by <br class="hidden sm:inline">
            <span class="bg-gradient-to-r from-yellow-300 via-amber-400 to-yellow-500 bg-clip-text text-transparent drop-shadow-[0_4px_12px_rgba(234,179,8,0.25)]">MS STUDIO</span>
        </h1>
        
        <p class="text-base md:text-lg text-slate-400 max-w-2xl mx-auto mb-10 leading-relaxed font-normal">
            Welcome to <strong class="text-slate-200">MS STUDIO</strong>. Powered by developers <strong> Mash & Shayon</strong>, we craft ultra-optimized, zero-lag Minecraft servers, practice networks, proxy networks, and custom setup configurations.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
            <a href="#pricing" class="w-full sm:w-auto bg-gradient-to-r from-yellow-400 to-amber-500 hover:from-yellow-300 hover:to-amber-400 text-slate-950 px-8 py-4 rounded-xl font-bold text-base transition-all shadow-xl shadow-yellow-500/20 hover:-translate-y-0.5 font-heading">
                Explore Setups & Pricing <i class="fa-solid fa-arrow-right ml-2 text-sm"></i>
            </a>
            <a href="#about" class="w-full sm:w-auto bg-slate-900/80 hover:bg-slate-800 border border-slate-800 text-slate-300 px-8 py-4 rounded-xl font-semibold text-base transition-all">
                Meet Developers
            </a>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="py-20 px-6 max-w-7xl mx-auto">
        <div class="text-center mb-16">
            <h2 class="text-3xl md:text-4xl font-bold text-white mb-3 font-heading">MS STUDIO Developers</h2>
            <p class="text-slate-400 text-sm max-w-md mx-auto">The engineering team bringing your server ideas into reality.</p>
        </div>

        <div class="grid md:grid-cols-2 gap-6">
            <!-- Shayon -->
            <div class="bg-slate-900/40 border border-yellow-500/20 p-8 rounded-2xl hover:border-yellow-500/40 transition-all flex flex-col justify-between">
                <div>
                    <div class="w-12 h-12 bg-yellow-400/10 border border-yellow-500/30 rounded-xl flex items-center justify-center text-yellow-400 text-xl font-bold mb-6">
                        <i class="fa-solid fa-code"></i>
                    </div>
                    <div class="flex items-center justify-between mb-2">
                        <h3 class="text-2xl font-bold text-white font-heading">Shayon</h3>
                        <span class="text-xs font-semibold px-3 py-1 rounded-full bg-slate-800 text-slate-300 border border-slate-700">1+ Year Exp</span>
                    </div>
                    <p class="text-yellow-400 font-medium text-sm mb-4">Server Developer @ MS STUDIO</p>
                    <p class="text-slate-400 text-sm leading-relaxed mb-8">
                        Specializes in technical optimization, bug fixes, custom plugin configurations, and maintaining maximum server TPS.
                    </p>
                </div>
                <button onclick="copyToClipboard('shayon0091')" class="w-full flex items-center justify-between bg-slate-950/80 hover:bg-slate-950 border border-slate-800 hover:border-yellow-400/40 p-3.5 rounded-xl text-slate-300 transition-all group cursor-pointer">
                    <div class="flex items-center gap-3 font-mono text-sm">
                        <i class="fa-brands fa-discord text-indigo-400 text-lg"></i>
                        <span>shayon0091</span>
                    </div>
                    <span class="text-xs font-bold text-slate-500 group-hover:text-yellow-400 transition-colors flex items-center gap-1">
                        <i class="fa-regular fa-copy"></i> Copy Tag
                    </span>
                </button>
            </div>

            <!-- Mash -->
            <div class="bg-slate-900/40 border border-yellow-500/20 p-8 rounded-2xl hover:border-yellow-500/40 transition-all flex flex-col justify-between">
                <div>
                    <div class="w-12 h-12 bg-amber-400/10 border border-amber-500/30 rounded-xl flex items-center justify-center text-amber-400 text-xl font-bold mb-6">
                        <i class="fa-solid fa-server"></i>
                    </div>
                    <div class="flex items-center justify-between mb-2">
                        <h3 class="text-2xl font-bold text-white font-heading">Mash</h3>
                        <span class="text-xs font-semibold px-3 py-1 rounded-full bg-slate-800 text-slate-300 border border-slate-700">3+ Years Exp</span>
                    </div>
                    <p class="text-amber-400 font-medium text-sm mb-4">Server Developer @ MS STUDIO</p>
                    <p class="text-slate-400 text-sm leading-relaxed mb-8">
                        Expert in full network builds, custom setup design, complex plugin setups, and high-tier server architecture.
                    </p>
                </div>
                <button onclick="copyToClipboard('m1shlor4yt')" class="w-full flex items-center justify-between bg-slate-950/80 hover:bg-slate-950 border border-slate-800 hover:border-yellow-400/40 p-3.5 rounded-xl text-slate-300 transition-all group cursor-pointer">
                    <div class="flex items-center gap-3 font-mono text-sm">
                        <i class="fa-brands fa-discord text-indigo-400 text-lg"></i>
                        <span>m1shlor4yt</span>
                    </div>
                    <span class="text-xs font-bold text-slate-500 group-hover:text-yellow-400 transition-colors flex items-center gap-1">
                        <i class="fa-regular fa-copy"></i> Copy Tag
                    </span>
                </button>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-20 bg-slate-900/30 border-y border-slate-800/80 px-6">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-16">
                <h2 class="text-3xl md:text-4xl font-bold text-white mb-3 font-heading">What MS STUDIO Develops</h2>
                <p class="text-slate-400 text-sm">Engineered solutions crafted for modern player retention.</p>
            </div>

            <div class="grid md:grid-cols-2 gap-8">
                <!-- Service 1 -->
                <div class="bg-slate-900/60 border border-slate-800 p-8 rounded-2xl">
                    <div class="w-12 h-12 bg-yellow-400/10 rounded-xl flex items-center justify-center text-yellow-400 text-xl font-bold mb-6">
                        <i class="fa-solid fa-wand-magic-sparkles"></i>
                    </div>
                    <h3 class="text-2xl font-bold text-white mb-3 font-heading">Custom Made Setups</h3>
                    <p class="text-slate-400 text-sm mb-6 leading-relaxed">Built from scratch based on your custom ideas, features, mechanics, and design layout.</p>
                    <div class="space-y-3 font-medium text-sm text-slate-300">
                        <div class="flex items-center gap-3"><i class="fa-solid fa-check text-yellow-400 text-xs"></i> Custom Lifesteal & Survival Setups</div>
                        <div class="flex items-center gap-3"><i class="fa-solid fa-check text-yellow-400 text-xs"></i> Practice & PvP Arena Engines</div>
                        <div class="flex items-center gap-3"><i class="fa-solid fa-check text-yellow-400 text-xs"></i> BungeeCord / Velocity Proxy Routing</div>
                        <div class="flex items-center gap-3"><i class="fa-solid fa-check text-yellow-400 text-xs"></i> Custom Plugin Configurations</div>
                    </div>
                </div>

                <!-- Service 2 -->
                <div class="bg-slate-900/60 border border-slate-800 p-8 rounded-2xl">
                    <div class="w-12 h-12 bg-amber-400/10 rounded-xl flex items-center justify-center text-amber-400 text-xl font-bold mb-6">
                        <i class="fa-solid fa-box-open"></i>
                    </div>
                    <h3 class="text-2xl font-bold text-white mb-3 font-heading">Premade Setups</h3>
                    <p class="text-slate-400 text-sm mb-6 leading-relaxed">Pre-configured, battle-tested server packages designed for instantaneous high-TPS launches.</p>
                    <div class="space-y-3 font-medium text-sm text-slate-300">
                        <div class="flex items-center gap-3"><i class="fa-solid fa-check text-amber-400 text-xs"></i> Ready-to-Deploy Lifesteal & Survival Packs</div>
                        <div class="flex items-center gap-3"><i class="fa-solid fa-check text-amber-400 text-xs"></i> Pre-configured Bedwars & Arcade Modes</div>
                        <div class="flex items-center gap-3"><i class="fa-solid fa-check text-amber-400 text-xs"></i> Instant Proxy Network Options</div>
                        <div class="flex items-center gap-3"><i class="fa-solid fa-check text-amber-400 text-xs"></i> Instant File Access Post-Purchase</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Pricing & Catalog Section -->
    <section id="pricing" class="py-20 px-6 max-w-7xl mx-auto">
        
        <!-- Custom Setups Heading -->
        <div class="flex items-center justify-between mb-8">
            <h3 class="text-2xl font-bold text-white font-heading">Custom Server Setups</h3>
            <span class="text-xs font-semibold text-yellow-400 bg-yellow-400/10 border border-yellow-400/20 px-3.5 py-1.5 rounded-full">MS Custom Tier</span>
        </div>

        <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6 mb-20">
            <!-- Item: Proxy Setup -->
            <div class="bg-slate-900/40 border border-yellow-500/40 p-6 rounded-2xl flex flex-col justify-between relative overflow-hidden">
                <div class="absolute -top-3 -right-3 bg-yellow-400 text-slate-950 font-bold text-[10px] px-3 py-1 rounded-bl-lg uppercase font-heading">Fast Setup</div>
                <div>
                    <h4 class="text-xl font-bold text-white mb-4 font-heading">Proxy Setup</h4>
                    <div class="space-y-3 mb-6">
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-yellow-500/20">
                            <span class="text-xs font-semibold text-yellow-400 uppercase tracking-wider">Fixed Price</span>
                            <span class="font-bold text-yellow-400 font-heading">₹50 Only</span>
                        </div>
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-yellow-400 text-slate-950 hover:bg-yellow-300 rounded-xl font-bold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Order Proxy Setup
                </a>
            </div>

            <!-- Item: Lifesteal -->
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                <div>
                    <h4 class="text-xl font-bold text-white mb-4 font-heading">Lifesteal Setup</h4>
                    <div class="space-y-3 mb-6">
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-slate-800/80">
                            <span class="text-xs font-semibold text-slate-400 uppercase tracking-wider">Basic</span>
                            <span class="font-bold text-white font-heading">₹399</span>
                        </div>
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-yellow-500/20">
                            <span class="text-xs font-semibold text-yellow-400 uppercase tracking-wider">Max Tier</span>
                            <span class="font-bold text-yellow-400 font-heading">₹599</span>
                        </div>
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-slate-800 hover:bg-yellow-400 hover:text-slate-950 rounded-xl text-white font-semibold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Order Custom Setup
                </a>
            </div>

            <!-- Item: Survival -->
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                <div>
                    <h4 class="text-xl font-bold text-white mb-4 font-heading">Survival / SMP Setup</h4>
                    <div class="space-y-3 mb-6">
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-slate-800/80">
                            <span class="text-xs font-semibold text-slate-400 uppercase tracking-wider">Basic</span>
                            <span class="font-bold text-white font-heading">₹399</span>
                        </div>
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-yellow-500/20">
                            <span class="text-xs font-semibold text-yellow-400 uppercase tracking-wider">Max Tier</span>
                            <span class="font-bold text-yellow-400 font-heading">₹599</span>
                        </div>
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-slate-800 hover:bg-yellow-400 hover:text-slate-950 rounded-xl text-white font-semibold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Order Custom Setup
                </a>
            </div>

            <!-- Item: PVP Practice -->
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                <div>
                    <h4 class="text-xl font-bold text-white mb-4 font-heading">PvP Practice Setup</h4>
                    <div class="space-y-3 mb-6">
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-slate-800/80">
                            <span class="text-xs font-semibold text-slate-400 uppercase tracking-wider">Basic</span>
                            <span class="font-bold text-white font-heading">₹550</span>
                        </div>
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-yellow-500/20">
                            <span class="text-xs font-semibold text-yellow-400 uppercase tracking-wider">Max Tier</span>
                            <span class="font-bold text-yellow-400 font-heading">₹850</span>
                        </div>
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-slate-800 hover:bg-yellow-400 hover:text-slate-950 rounded-xl text-white font-semibold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Order Custom Setup
                </a>
            </div>

            <!-- Item: Bedwars -->
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                <div>
                    <h4 class="text-xl font-bold text-white mb-4 font-heading">Bedwars Setup</h4>
                    <div class="space-y-3 mb-6">
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-slate-800/80">
                            <span class="text-xs font-semibold text-slate-400 uppercase tracking-wider">Basic</span>
                            <span class="font-bold text-white font-heading">₹499</span>
                        </div>
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-yellow-500/20">
                            <span class="text-xs font-semibold text-yellow-400 uppercase tracking-wider">Max Tier</span>
                            <span class="font-bold text-yellow-400 font-heading">₹799</span>
                        </div>
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-slate-800 hover:bg-yellow-400 hover:text-slate-950 rounded-xl text-white font-semibold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Order Custom Setup
                </a>
            </div>

            <!-- Item: Arcade -->
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                <div>
                    <h4 class="text-xl font-bold text-white mb-4 font-heading">Arcade Setup</h4>
                    <div class="space-y-3 mb-6">
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-slate-800/80">
                            <span class="text-xs font-semibold text-slate-400 uppercase tracking-wider">Basic</span>
                            <span class="font-bold text-white font-heading">₹450</span>
                        </div>
                        <div class="flex justify-between items-center bg-slate-950/60 p-3 rounded-xl border border-yellow-500/20">
                            <span class="text-xs font-semibold text-yellow-400 uppercase tracking-wider">Max Tier</span>
                            <span class="font-bold text-yellow-400 font-heading">₹750</span>
                        </div>
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-slate-800 hover:bg-yellow-400 hover:text-slate-950 rounded-xl text-white font-semibold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Order Custom Setup
                </a>
            </div>
        </div>

        <!-- Premade Setups Heading -->
        <div class="flex items-center justify-between mb-8">
            <h3 class="text-2xl font-bold text-white font-heading">Premade Server Setups</h3>
            <span class="text-xs font-semibold text-amber-400 bg-amber-400/10 border border-amber-400/20 px-3.5 py-1.5 rounded-full">Instant Delivery</span>
        </div>

        <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6 mb-16">
            <!-- Premade Proxy Item -->
            <div class="bg-slate-900/40 border border-amber-500/40 p-6 rounded-2xl flex flex-col justify-between">
                <div>
                    <h4 class="text-xl font-bold text-white mb-2 font-heading">Proxy Premade</h4>
                    <p class="text-xs text-slate-400 mb-6">Pre-configured Bungee / Velocity proxy network setup.</p>
                    <div class="font-heading text-xl font-bold text-amber-400 bg-slate-950/80 border border-slate-800 p-3 rounded-xl text-center mb-6">
                        ₹50 Only
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-amber-400 text-slate-950 hover:bg-amber-300 rounded-xl font-bold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Buy Proxy Pack
                </a>
            </div>

            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                <div>
                    <h4 class="text-xl font-bold text-white mb-2 font-heading">Lifesteal Premade</h4>
                    <p class="text-xs text-slate-400 mb-6">Plug-and-play package with pre-configured ranks & economy.</p>
                    <div class="font-heading text-xl font-bold text-yellow-400 bg-slate-950/80 border border-slate-800 p-3 rounded-xl text-center mb-6">
                        ₹299 – ₹499
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-slate-800 hover:bg-yellow-400 hover:text-slate-950 rounded-xl text-white font-semibold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Buy Premade Pack
                </a>
            </div>

            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                <div>
                    <h4 class="text-xl font-bold text-white mb-2 font-heading">Survival Premade</h4>
                    <p class="text-xs text-slate-400 mb-6">Clean survival environment with anti-grief protection.</p>
                    <div class="font-heading text-xl font-bold text-yellow-400 bg-slate-950/80 border border-slate-800 p-3 rounded-xl text-center mb-6">
                        ₹299 – ₹599
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-slate-800 hover:bg-yellow-400 hover:text-slate-950 rounded-xl text-white font-semibold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Buy Premade Pack
                </a>
            </div>

            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                <div>
                    <h4 class="text-xl font-bold text-white mb-2 font-heading">PvP Practice Premade</h4>
                    <p class="text-xs text-slate-400 mb-6">Low latency duels configuration with arena maps.</p>
                    <div class="font-heading text-xl font-bold text-yellow-400 bg-slate-950/80 border border-slate-800 p-3 rounded-xl text-center mb-6">
                        ₹399 – ₹650
                    </div>
                </div>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full py-3 bg-slate-800 hover:bg-yellow-400 hover:text-slate-950 rounded-xl text-white font-semibold text-sm flex items-center justify-center gap-2 transition-all">
                    <i class="fa-brands fa-discord"></i> Buy Premade Pack
                </a>
            </div>
        </div>

        <!-- Info Card -->
        <div class="bg-slate-900/60 border border-yellow-500/20 p-8 rounded-2xl grid md:grid-cols-2 gap-8 items-center">
            <div>
                <h4 class="text-xl font-bold text-white mb-3 font-heading">MS STUDIO Support & Orders</h4>
                <p class="text-slate-400 text-sm leading-relaxed mb-4">
                    All studio orders are processed through our Discord ticket platform. Instant payments supported across India.
                </p>
                <div class="flex gap-3">
                    <span class="text-xs font-semibold px-3 py-1.5 rounded-lg bg-slate-800 text-slate-300 border border-slate-700">UPI Payments</span>
                    <span class="text-xs font-semibold px-3 py-1.5 rounded-lg bg-slate-800 text-slate-300 border border-slate-700">QR Scanner</span>
                </div>
            </div>
            <div class="text-right flex justify-end">
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="bg-indigo-600 hover:bg-indigo-500 text-white font-bold px-8 py-4 rounded-xl text-sm transition-all shadow-lg shadow-indigo-600/20 inline-flex items-center gap-2">
                    <i class="fa-brands fa-discord text-lg"></i> Open Support Ticket
                </a>
            </div>
        </div>
    </section>

    <!-- Workflow Section -->
    <section id="workflow" class="py-20 px-6 max-w-7xl mx-auto border-t border-slate-800/80">
        <div class="text-center mb-16">
            <h2 class="text-3xl md:text-4xl font-bold text-white mb-3 font-heading">MS STUDIO Delivery Workflow</h2>
            <p class="text-slate-400 text-sm">A structured 6-step process to bring your server live safely.</p>
        </div>

        <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl relative">
                <span class="text-3xl font-bold text-slate-700 absolute top-5 right-6 font-heading">01</span>
                <h4 class="text-base font-bold text-yellow-400 mb-2">50% Advance Deposit</h4>
                <p class="text-slate-400 text-xs leading-relaxed">Initial deposit to confirm project booking and allocate server development resources.</p>
            </div>
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl relative">
                <span class="text-3xl font-bold text-slate-700 absolute top-5 right-6 font-heading">02</span>
                <h4 class="text-base font-bold text-yellow-400 mb-2">Requirement Planning</h4>
                <p class="text-slate-400 text-xs leading-relaxed">Detailed discussion regarding mechanics, plugins, features, and server aesthetic.</p>
            </div>
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl relative">
                <span class="text-3xl font-bold text-slate-700 absolute top-5 right-6 font-heading">03</span>
                <h4 class="text-base font-bold text-yellow-400 mb-2">Server Development</h4>
                <p class="text-slate-400 text-xs leading-relaxed">Building ranks, economies, crates, custom items, and core server configurations.</p>
            </div>
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl relative">
                <span class="text-3xl font-bold text-slate-700 absolute top-5 right-6 font-heading">04</span>
                <h4 class="text-base font-bold text-yellow-400 mb-2">Optimization & Testing</h4>
                <p class="text-slate-400 text-xs leading-relaxed">Deep testing for memory leaks, lag spikes, exploits, and ensuring 20 TPS stability.</p>
            </div>
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl relative">
                <span class="text-3xl font-bold text-slate-700 absolute top-5 right-6 font-heading">05</span>
                <h4 class="text-base font-bold text-yellow-400 mb-2">Final Payment</h4>
                <p class="text-slate-400 text-xs leading-relaxed">After client preview and approval, remaining 50% payment is completed.</p>
            </div>
            <div class="bg-slate-900/40 border border-slate-800 p-6 rounded-2xl relative">
                <span class="text-3xl font-bold text-slate-700 absolute top-5 right-6 font-heading">06</span>
                <h4 class="text-base font-bold text-yellow-400 mb-2">Delivery & Support</h4>
                <p class="text-slate-400 text-xs leading-relaxed">File transfer along with installation guidance and initial technical support.</p>
            </div>
        </div>
    </section>

    <!-- Reviews / Testimonials Section -->
    <section id="reviews" class="py-20 bg-slate-900/30 border-t border-slate-800/80 px-6">
        <div class="max-w-7xl mx-auto">
            <div class="text-center mb-12">
                <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-yellow-400/10 border border-yellow-400/20 text-yellow-400 text-xs font-semibold uppercase mb-4">
                    <i class="fa-solid fa-star"></i> Client Vouches & Reviews
                </div>
                <h2 class="text-3xl md:text-4xl font-bold text-white mb-3 font-heading">What Our Clients Say</h2>
                <p class="text-slate-400 text-sm max-w-md mx-auto">Real feedback from server owners who built their network with MS STUDIO.</p>
            </div>

            <!-- Action Buttons for Reviews -->
            <div class="flex flex-col sm:flex-row items-center justify-center gap-4 mb-14">
                <button onclick="openReviewModal()" class="w-full sm:w-auto bg-yellow-400 hover:bg-yellow-300 text-slate-950 font-bold px-7 py-3.5 rounded-xl transition-all shadow-lg shadow-yellow-500/20 flex items-center justify-center gap-2 font-heading cursor-pointer">
                    <i class="fa-solid fa-pen-to-square"></i> Write a Review
                </button>
                <a href="https://discord.gg/Ju5UCjJgY" target="_blank" class="w-full sm:w-auto bg-slate-900 hover:bg-slate-800 border border-slate-700 text-slate-200 font-bold px-7 py-3.5 rounded-xl transition-all flex items-center justify-center gap-2 font-heading">
                    <i class="fa-brands fa-discord text-indigo-400"></i> View All Vouches on Discord
                </a>
            </div>

            <!-- Sample Review Cards -->
            <div class="grid md:grid-cols-3 gap-6">
                <!-- Review 1 -->
                <div class="bg-slate-900/60 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                    <div>
                        <div class="flex items-center gap-1 text-yellow-400 text-sm mb-4">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-slate-300 text-xs leading-relaxed italic mb-6">
                            "Mash and Shayon setup our custom Lifesteal server within 2 days! TPS stays strictly at 20.0 even during 40+ player fights. Exceptional work!"
                        </p>
                    </div>
                    <div class="flex items-center justify-between border-t border-slate-800/80 pt-4">
                        <div>
                            <p class="text-sm font-bold text-white font-heading">Aarav M.</p>
                            <p class="text-[10px] text-slate-500 font-mono">Lifesteal Owner</p>
                        </div>
                        <span class="text-[10px] font-semibold px-2.5 py-1 rounded bg-slate-800 text-yellow-400 border border-slate-700">Custom Setup</span>
                    </div>
                </div>

                <!-- Review 2 -->
                <div class="bg-slate-900/60 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                    <div>
                        <div class="flex items-center gap-1 text-yellow-400 text-sm mb-4">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-slate-300 text-xs leading-relaxed italic mb-6">
                            "Bought the premade proxy pack for ₹50. Super fast setup and zero configuration issues on Velocity. Highly recommended!"
                        </p>
                    </div>
                    <div class="flex items-center justify-between border-t border-slate-800/80 pt-4">
                        <div>
                            <p class="text-sm font-bold text-white font-heading">Rohan_PvP</p>
                            <p class="text-[10px] text-slate-500 font-mono">Network Admin</p>
                        </div>
                        <span class="text-[10px] font-semibold px-2.5 py-1 rounded bg-slate-800 text-amber-400 border border-slate-700">Proxy Pack</span>
                    </div>
                </div>

                <!-- Review 3 -->
                <div class="bg-slate-900/60 border border-slate-800 p-6 rounded-2xl flex flex-col justify-between">
                    <div>
                        <div class="flex items-center gap-1 text-yellow-400 text-sm mb-4">
                            <i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i><i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-slate-300 text-xs leading-relaxed italic mb-6">
                            "Shayon helped troubleshoot our plugin crashes late at night. Super helpful team and polite support in tickets!"
                        </p>
                    </div>
                    <div class="flex items-center justify-between border-t border-slate-800/80 pt-4">
                        <div>
                            <p class="text-sm font-bold text-white font-heading">Toxic_Gamer</p>
                            <p class="text-[10px] text-slate-500 font-mono">Survival Owner</p>
                        </div>
                        <span class="text-[10px] font-semibold px-2.5 py-1 rounded bg-slate-800 text-yellow-400 border border-slate-700">Bug Fixes</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Write a Review Modal -->
    <div id="review-modal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-sm flex items-center justify-center p-4 opacity-0 pointer-events-none">
        <div class="bg-[#0c0d12] border border-yellow-500/30 rounded-2xl p-6 md:p-8 max-w-lg w-full shadow-2xl relative">
            <button onclick="closeReviewModal()" class="absolute top-4 right-4 text-slate-400 hover:text-white text-lg cursor-pointer">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <h3 class="text-2xl font-bold text-white font-heading mb-1">Submit Your Review</h3>
            <p class="text-xs text-slate-400 mb-6">Share your experience working with MS STUDIO.</p>

            <form id="reviewForm" onsubmit="handleReviewSubmit(event)" class="space-y-4">
                <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">Discord Username / Name</label>
                    <input type="text" id="reviewerName" required placeholder="e.g. PlayerOne#1234" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-white focus:outline-none focus:border-yellow-400">
                </div>
                <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">Service / Setup Ordered</label>
                    <select id="reviewSetup" required class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-white focus:outline-none focus:border-yellow-400">
                        <option value="Custom Setup">Custom Setup</option>
                        <option value="Premade Pack">Premade Pack</option>
                        <option value="Proxy Setup">Proxy Setup</option>
                        <option value="Optimization / Bug Fix">Optimization / Bug Fix</option>
                    </select>
                </div>
                <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">Star Rating</label>
                    <div class="flex gap-2 text-yellow-400 text-xl cursor-pointer" id="star-rating">
                        <i class="fa-solid fa-star star-btn" onclick="setRating(1)"></i>
                        <i class="fa-solid fa-star star-btn" onclick="setRating(2)"></i>
                        <i class="fa-solid fa-star star-btn" onclick="setRating(3)"></i>
                        <i class="fa-solid fa-star star-btn" onclick="setRating(4)"></i>
                        <i class="fa-solid fa-star star-btn" onclick="setRating(5)"></i>
                    </div>
                </div>
                <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">Your Feedback</label>
                    <textarea id="reviewComment" rows="3" required placeholder="Write a few lines about our work..." class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-2.5 text-sm text-white focus:outline-none focus:border-yellow-400"></textarea>
                </div>
                <button type="submit" class="w-full py-3.5 bg-yellow-400 hover:bg-yellow-300 text-slate-950 font-bold rounded-xl text-sm transition-all shadow-lg shadow-yellow-500/20 font-heading cursor-pointer">
                    Submit Review to Discord
                </button>
            </form>
        </div>
    </div>

    <!-- Stats Section -->
    <section id="stats" class="py-16 bg-slate-900/50 border-y border-slate-800/80 px-6">
        <div class="max-w-7xl mx-auto grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
            <div>
                <p class="text-4xl font-extrabold text-yellow-400 mb-1 font-heading">25+</p>
                <p class="text-slate-400 font-medium text-xs">Projects Completed</p>
            </div>
            <div>
                <p class="text-4xl font-extrabold text-yellow-400 mb-1 font-heading">99.9%</p>
                <p class="text-slate-400 font-medium text-xs">TPS Efficiency</p>
            </div>
            <div>
                <p class="text-4xl font-extrabold text-yellow-400 mb-1 font-heading">3+ Years</p>
                <p class="text-slate-400 font-medium text-xs">Combined Experience</p>
            </div>
            <div>
                <p class="text-4xl font-extrabold text-yellow-400 mb-1 font-heading">100%</p>
                <p class="text-slate-400 font-medium text-xs">Satisfaction Rate</p>
            </div>
        </div>
    </section>

    <!-- Direct Contact Copy Section -->
    <section class="py-20 px-6 max-w-3xl mx-auto text-center">
        <h2 class="text-3xl font-bold text-white mb-3 font-heading">Contact MS STUDIO</h2>
        <p class="text-slate-400 text-sm mb-8">Click on any handle below to copy the Discord tag directly.</p>
        
        <div class="flex flex-col sm:flex-row justify-center gap-4">
            <button onclick="copyToClipboard('shayon0091')" class="bg-slate-900 border border-slate-800 hover:border-yellow-400/50 p-4 rounded-xl flex items-center justify-between gap-6 transition-all group cursor-pointer w-full">
                <div class="flex items-center gap-3">
                    <i class="fa-brands fa-discord text-indigo-400 text-2xl"></i>
                    <div class="text-left">
                        <p class="text-[10px] font-bold text-slate-500 uppercase tracking-wider">Shayon</p>
                        <p class="text-sm font-mono font-bold text-white">shayon0091</p>
                    </div>
                </div>
                <span class="text-xs font-semibold text-slate-500 group-hover:text-yellow-400 transition-colors">Click to Copy</span>
            </button>

            <button onclick="copyToClipboard('m1shlor4yt')" class="bg-slate-900 border border-slate-800 hover:border-amber-400/50 p-4 rounded-xl flex items-center justify-between gap-6 transition-all group cursor-pointer w-full">
                <div class="flex items-center gap-3">
                    <i class="fa-brands fa-discord text-indigo-400 text-2xl"></i>
                    <div class="text-left">
                        <p class="text-[10px] font-bold text-slate-500 uppercase tracking-wider">Mash</p>
                        <p class="text-sm font-mono font-bold text-white">m1shlor4yt</p>
                    </div>
                </div>
                <span class="text-xs font-semibold text-slate-500 group-hover:text-amber-400 transition-colors">Click to Copy</span>
            </button>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-8 border-t border-slate-800/80 text-center text-xs text-slate-500">
        <p>© 2026 MS STUDIO. All rights reserved. Not affiliated with Mojang AB.</p>
    </footer>

    <!-- Scripts -->
    <script>
        // Smooth Loader Hide Script
        window.addEventListener('load', () => {
            setTimeout(() => {
                const preloader = document.getElementById('preloader');
                preloader.style.opacity = '0';
                preloader.style.visibility = 'hidden';
            }, 1800);
        });

        // Copy Username Function
        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(() => {
                const toast = document.getElementById('toast');
                const toastMsg = document.getElementById('toast-msg');
                toastMsg.innerText = `Copied "${text}" to clipboard!`;
                
                toast.classList.remove('translate-y-20', 'opacity-0', 'pointer-events-none');
                
                setTimeout(() => {
                    toast.classList.add('translate-y-20', 'opacity-0', 'pointer-events-none');
                }, 2500);
            }).catch(err => {
                console.error('Failed to copy: ', err);
            });
        }

        // Modal Controls
        function openReviewModal() {
            const modal = document.getElementById('review-modal');
            modal.classList.remove('opacity-0', 'pointer-events-none');
        }

        function closeReviewModal() {
            const modal = document.getElementById('review-modal');
            modal.classList.add('opacity-0', 'pointer-events-none');
        }

        // Star Rating Selection Logic
        let currentRating = 5;
        function setRating(rating) {
            currentRating = rating;
            const stars = document.querySelectorAll('#star-rating .star-btn');
            stars.forEach((star, index) => {
                if (index < rating) {
                    star.classList.add('text-yellow-400');
                    star.classList.remove('text-slate-600');
                } else {
                    star.classList.remove('text-yellow-400');
                    star.classList.add('text-slate-600');
                }
            });
        }

        // Review Submission Handling
        function handleReviewSubmit(e) {
            e.preventDefault();
            const name = document.getElementById('reviewerName').value;
            const setup = document.getElementById('reviewSetup').value;
            const comment = document.getElementById('reviewComment').value;

            closeReviewModal();

            // Toast feedback confirmation
            const toast = document.getElementById('toast');
            const toastMsg = document.getElementById('toast-msg');
            toastMsg.innerText = "Thank you! Redirecting to Discord...";
            toast.classList.remove('translate-y-20', 'opacity-0', 'pointer-events-none');

            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0', 'pointer-events-none');
                // Open Discord to submit review in ticket/vouch channel
                window.open("https://discord.gg/Ju5UCjJgY", "_blank");
            }, 2000);
        }
    </script>
</body>
</html>
