# Weed-coin
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>$WEED • WeedCoin</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&amp;display=swap');
        
        :root {
            --leaf: #22c55e;
        }
        
        .tail-container {
            font-family: 'Press Start 2P', system-ui;
        }
        
        .hero-bg {
            background: radial-gradient(circle at 50% 20%, #14532d 0%, #052e16 70%);
        }
        
        .leaf-float {
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-30px) rotate(8deg); }
        }
        
        .neon-text {
            text-shadow: 
                0 0 10px #22c55e,
                0 0 20px #22c55e,
                0 0 40px #15803d;
        }
        
        .token-card {
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        
        .token-card:hover {
            transform: scale(1.08) rotate(2deg);
            box-shadow: 0 0 60px -10px #22c55e;
        }
        
        .roadmap-dot {
            box-shadow: 0 0 0 8px rgba(34, 197, 94, 0.3);
        }
        
        .smoke {
            position: absolute;
            width: 20px;
            height: 20px;
            background: rgba(163, 163, 163, 0.15);
            border-radius: 50%;
            animation: smoke-rise 8s linear infinite;
            pointer-events: none;
        }
    </style>
</head>
<body class="tail-container bg-[#052e16] text-white overflow-x-hidden">
    <!-- NAVBAR -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-black/80 backdrop-blur-xl border-b border-emerald-900">
        <div class="max-w-7xl mx-auto px-6 py-5 flex items-center justify-between">
            <!-- Logo -->
            <div class="flex items-center gap-3">
                <div class="w-12 h-12 bg-emerald-500 rounded-2xl flex items-center justify-center text-4xl shadow-[0_0_30px_#22c55e] leaf-float">
                    🌿
                </div>
                <div>
                    <span class="text-3xl font-bold tracking-tighter neon-text">WEED</span>
                    <span class="text-emerald-400 text-xl">COIN</span>
                </div>
            </div>

            <!-- Menu -->
            <div class="hidden md:flex items-center gap-8 text-sm uppercase tracking-widest">
                <a href="#about" class="hover:text-emerald-400 transition-colors">About</a>
                <a href="#tokenomics" class="hover:text-emerald-400 transition-colors">Tokenomics</a>
                <a href="#roadmap" class="hover:text-emerald-400 transition-colors">Roadmap</a>
                <a href="#buy" class="hover:text-emerald-400 transition-colors">How to Buy</a>
                <a href="#community" class="hover:text-emerald-400 transition-colors">Community</a>
            </div>

            <div class="flex items-center gap-4">
                <button onclick="connectWallet()" 
                        class="px-8 py-3 bg-emerald-500 hover:bg-emerald-600 text-black font-bold rounded-3xl text-sm tracking-widest transition-all active:scale-95 shadow-[0_0_20px_#22c55e]">
                    CONNECT WALLET
                </button>
                <button onclick="window.location.reload()" 
                        class="px-6 py-3 border border-emerald-500 hover:bg-emerald-950 rounded-3xl text-sm flex items-center gap-2">
                    <i class="fa-solid fa-rotate"></i>
                </button>
            </div>
        </div>
    </nav>

    <!-- HERO -->
    <section id="hero" class="hero-bg min-h-screen flex items-center pt-20 relative overflow-hidden">
        <!-- Background floating leaves -->
        <div class="absolute inset-0 pointer-events-none">
            <div class="absolute top-20 left-10 text-8xl opacity-10 leaf-float" style="animation-delay: 0s;">🌿</div>
            <div class="absolute top-40 right-20 text-7xl opacity-10 leaf-float" style="animation-delay: 2s;">🍃</div>
            <div class="absolute bottom-40 left-1/3 text-9xl opacity-10 leaf-float" style="animation-delay: 4s;">🌱</div>
            <div class="absolute bottom-60 right-1/4 text-6xl opacity-10 leaf-float" style="animation-delay: 1.5s;">🍂</div>
        </div>

        <div class="max-w-5xl mx-auto px-6 text-center relative z-10">
            <div class="inline-flex items-center gap-3 bg-black/60 px-6 py-2 rounded-3xl border border-emerald-700 mb-8">
                <div class="w-3 h-3 bg-emerald-400 rounded-full animate-pulse"></div>
                <span class="text-emerald-400 text-xs tracking-[4px] font-bold">LIVE ON SOLANA • $WEED</span>
            </div>

            <h1 class="text-8xl md:text-[10rem] leading-none font-black tracking-tighter neon-text mb-6">
                WEED<br>COIN
            </h1>
            
            <p class="text-3xl md:text-5xl text-emerald-300 mb-8 font-light">
                Get <span class="line-through opacity-50">high</span> on gains
            </p>

            <div class="flex flex-col md:flex-row gap-6 justify-center items-center">
                <a href="#buy" 
                   class="group relative px-16 py-6 bg-white text-black font-black text-2xl rounded-3xl flex items-center gap-4 hover:scale-105 transition-all shadow-2xl shadow-emerald-500/50">
                    <span>BUY $WEED NOW</span>
                    <span class="text-4xl group-active:rotate-12 transition-transform">🌿</span>
                </a>
                
                <a href="https://dexscreener.com" target="_blank"
                   class="px-10 py-6 border-2 border-white/70 hover:border-emerald-400 text-xl font-medium rounded-3xl flex items-center gap-3 transition-all">
                    <i class="fa-solid fa-chart-line"></i>
                    LIVE CHART
                </a>
            </div>

            <div class="mt-20 grid grid-cols-3 gap-8 max-w-md mx-auto text-center">
                <div>
                    <div class="text-emerald-400 text-4xl font-bold">$420M</div>
                    <div class="text-xs tracking-widest text-emerald-700">MARKET CAP</div>
                </div>
                <div>
                    <div class="text-emerald-400 text-4xl font-bold">69K</div>
                    <div class="text-xs tracking-widest text-emerald-700">HOLDERS</div>
                </div>
                <div>
                    <div class="text-emerald-400 text-4xl font-bold">420%</div>
                    <div class="text-xs tracking-widest text-emerald-700">ATH ROI</div>
                </div>
            </div>

            <div class="mt-16 text-xs uppercase tracking-[6px] text-emerald-600 flex items-center justify-center gap-8">
                <div class="flex items-center gap-2">
                    <i class="fa-brands fa-solana"></i>
                    SOLANA
                </div>
                <div>•••</div>
                <div>CA: 7xK...9pQd</div>
            </div>
        </div>

        <!-- Scroll prompt -->
        <div class="absolute bottom-12 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 text-xs tracking-widest">
            <div class="animate-bounce">↓</div>
            <span>SCROLL FOR THE
