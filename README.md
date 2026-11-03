<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>S|R Aura - PRAKRITIC GLOW | Handcrafted Pure Soy Wax & Eco-Glitter Candles</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400..800;1,400..800&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        warmBeige: '#FBF8F3',
                        cream: '#FFFDF9',
                        sand: '#EBE4D8',
                        forestGreen: '#2C3E2E',
                        deepOlive: '#1F2D20',
                        terracotta: '#C86D51',
                        shimmerGold: '#D4AF37',
                        goldHover: '#B59226',
                        softSage: '#E2E8E0',
                        accentGold: '#E6C665'
                    },
                    fontFamily: {
                        serif: ['Playfair Display', 'serif'],
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom Smooth Scrollbar & Animations */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #FBF8F3;
        }
        ::-webkit-scrollbar-thumb {
            background: #2C3E2E;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #D4AF37;
        }
        .glass-header {
            background: rgba(251, 248, 243, 0.90);
            backdrop-filter: blur(12px);
        }
        .cart-slide-over {
            transition: transform 0.35s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .fade-in {
            animation: fadeIn 0.4s ease-out forwards;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(8px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .glitter-badge {
            background: linear-gradient(135deg, #D4AF37 0%, #F3E5AB 50%, #B59226 100%);
        }
        .glitter-text {
            background: linear-gradient(135deg, #2C3E2E 0%, #D4AF37 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    </style>
</head>
<body class="bg-warmBeige text-forestGreen font-sans antialiased selection:bg-shimmerGold selection:text-white">

    <!-- Notification Toast -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 transform translate-y-24 opacity-0 transition-all duration-300 ease-out bg-forestGreen text-cream px-5 py-3.5 rounded-xl shadow-2xl flex items-center space-x-3 pointer-events-none border border-shimmerGold/30">
        <i class="fa-solid fa-sparkles text-shimmerGold text-lg"></i>
        <span id="toast-message" class="text-sm font-medium">Added to your aura collection</span>
    </div>

    <!-- Announcement Bar -->
    <div class="bg-forestGreen text-cream text-xs font-medium py-2.5 px-4 text-center tracking-wide flex justify-center items-center gap-2 border-b border-shimmerGold/20">
        <span class="text-shimmerGold">✨</span>
        <span>100% Homemade Pure Soy Wax Candles with Natural Fragrance & Eco-Glitter</span>
        <span class="hidden md:inline">• Free Shipping on Orders Over ₹999</span>
        <span class="text-shimmerGold">✨</span>
    </div>

    <!-- Sticky Navigation Header -->
    <header class="sticky top-0 z-30 glass-header border-b border-sand/80 transition-all duration-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                
                <!-- Mobile Menu Button -->
                <button id="mobile-menu-btn" class="lg:hidden text-forestGreen hover:text-shimmerGold focus:outline-none p-2">
                    <i class="fa-solid fa-bars text-xl"></i>
                </button>

                <!-- Brand Logo -->
                <a href="#" class="flex flex-col items-center sm:items-start group">
                    <div class="flex items-center gap-2">
                        <span class="w-8 h-8 rounded-full bg-forestGreen/10 flex items-center justify-center text-shimmerGold group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-sparkles text-sm"></i>
                        </span>
                        <span class="font-serif text-2xl md:text-3xl font-bold tracking-tight text-forestGreen">
                            S<span class="text-shimmerGold">|</span>R Aura
                        </span>
                    </div>
                    <span class="text-[9px] font-semibold uppercase tracking-[0.25em] text-shimmerGold ml-10 -mt-1">PRAKRITIC GLOW</span>
                </a>

                <!-- Desktop Navigation Links -->
                <nav class="hidden lg:flex items-center space-x-8 text-sm font-medium">
                    <a href="#shop" class="hover:text-shimmerGold transition-colors py-1">Shop Collections</a>
                    <a href="#craft" class="hover:text-shimmerGold transition-colors py-1">Our Homemade Craft</a>
                    <a href="#scent-quiz" class="hover:text-shimmerGold transition-colors py-1 text-shimmerGold font-semibold flex items-center gap-1.5">
                        <i class="fa-solid fa-wand-magic-sparkles text-xs"></i> Find Your Aura
                    </a>
                    <a href="#reviews" class="hover:text-shimmerGold transition-colors py-1">Reviews</a>
                    <a href="#footer" class="hover:text-shimmerGold transition-colors py-1">Contact Us</a>
                </nav>

                <!-- Action Icons -->
                <div class="flex items-center space-x-5">
                    <!-- Search Bar Toggle -->
                    <div class="relative hidden sm:block">
                        <input type="text" id="search-input" placeholder="Search soy candles, glitter..." class="bg-cream border border-sand rounded-full py-2 pl-9 pr-4 text-xs focus:outline-none focus:border-shimmerGold w-44 lg:w-56 transition-all placeholder:text-gray-400">
                        <i class="fa-solid fa-magnifying-glass absolute left-3.5 top-2.5 text-gray-400 text-xs"></i>
                    </div>

                    <!-- Wishlist -->
                    <button class="relative text-forestGreen hover:text-shimmerGold transition-colors p-2" title="Wishlist">
                        <i class="fa-regular fa-heart text-xl"></i>
                        <span class="absolute top-1 right-1 bg-shimmerGold text-deepOlive text-[10px] w-4 h-4 rounded-full flex items-center justify-center font-bold">2</span>
                    </button>

                    <!-- Cart Trigger Button -->
                    <button id="open-cart-btn" class="relative text-forestGreen hover:text-shimmerGold transition-colors p-2 flex items-center gap-2">
                        <i class="fa-solid fa-bag-shopping text-xl"></i>
                        <span id="cart-count-badge" class="bg-forestGreen text-shimmerGold text-xs font-bold w-5 h-5 rounded-full flex items-center justify-center border border-shimmerGold">0</span>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Drawer Navigation -->
        <div id="mobile-menu" class="hidden lg:hidden border-t border-sand bg-warmBeige px-4 pt-4 pb-6 space-y-3">
            <a href="#shop" class="block text-base font-medium hover:text-shimmerGold py-2">Shop Collections</a>
            <a href="#craft" class="block text-base font-medium hover:text-shimmerGold py-2">Our Homemade Craft</a>
            <a href="#scent-quiz" class="block text-base font-semibold text-shimmerGold py-2">Find Your Aura Quiz</a>
            <a href="#reviews" class="block text-base font-medium hover:text-shimmerGold py-2">Reviews</a>
            <a href="#footer" class="block text-base font-medium hover:text-shimmerGold py-2">Contact Us</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="relative bg-cream py-16 md:py-24 overflow-hidden border-b border-sand">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                
                <div class="lg:col-span-7 space-y-6 text-center lg:text-left z-10">
                    <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-softSage text-xs font-bold tracking-wider uppercase text-forestGreen border border-shimmerGold/30">
                        <i class="fa-solid fa-seedling text-xs text-shimmerGold"></i> 100% Homemade Pure Soy Wax & Natural Fragrances
                    </div>
                    
                    <h1 class="font-serif text-4xl sm:text-5xl lg:text-6xl font-bold text-forestGreen leading-tight">
                        Illuminate Your Home with <span class="italic font-normal text-shimmerGold">Prakritic Glow</span> & Eco-Glitter.
                    </h1>
                    
                    <p class="text-gray-600 text-base sm:text-lg max-w-xl mx-auto lg:mx-0 font-light leading-relaxed">
                        Hand-poured in small homemade batches. Our 100% pure soy candles melt into a enchanting shimmering pool of non-toxic eco-glitter, infused with soothing therapeutic essential fragrances.
                    </p>
                    
                    <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-4">
                        <a href="#shop" class="w-full sm:w-auto bg-forestGreen hover:bg-deepOlive text-cream font-medium px-8 py-4 rounded-xl transition-all shadow-lg shadow-forestGreen/20 flex items-center justify-center gap-2 group border border-shimmerGold/40">
                            Explore Prakritic Collection
                            <i class="fa-solid fa-arrow-right text-xs text-shimmerGold group-hover:translate-x-1 transition-transform"></i>
                        </a>
                        <a href="#scent-quiz" class="w-full sm:w-auto bg-sand/60 hover:bg-sand text-forestGreen font-semibold px-8 py-4 rounded-xl transition-all flex items-center justify-center gap-2 border border-sand">
                            <i class="fa-solid fa-sparkles text-shimmerGold"></i> Find Your Aura Quiz
                        </a>
                    </div>

                    <!-- Brand Pillars Badges -->
                    <div class="pt-8 border-t border-sand grid grid-cols-3 gap-4 text-center sm:text-left">
                        <div class="space-y-1">
                            <i class="fa-solid fa-leaf text-shimmerGold text-lg"></i>
                            <h4 class="text-xs font-semibold text-forestGreen">100% Pure Soy</h4>
                            <p class="text-[11px] text-gray-500">Clean, soot-free burn</p>
                        </div>
                        <div class="space-y-1">
                            <i class="fa-solid fa-hands-holding-circle text-shimmerGold text-lg"></i>
                            <h4 class="text-xs font-semibold text-forestGreen">Homemade Batches</h4>
                            <p class="text-[11px] text-gray-500">Crafted with care & love</p>
                        </div>
                        <div class="space-y-1">
                            <i class="fa-solid fa-sparkles text-shimmerGold text-lg"></i>
                            <h4 class="text-xs font-semibold text-forestGreen">Natural Eco-Glitter</h4>
                            <p class="text-[11px] text-gray-500">Shimmering melt pool</p>
                        </div>
                    </div>
                </div>

                <!-- Hero Image Showcase -->
                <div class="lg:col-span-5 relative">
                    <div class="relative mx-auto max-w-md lg:max-w-none">
                        <div class="aspect-[4/5] rounded-3xl overflow-hidden shadow-2xl relative group border-2 border-shimmerGold/30">
                            <img src="https://images.unsplash.com/photo-1603006905003-be475563bc59?auto=format&fit=crop&w=800&q=80" 
                                 alt="S|R Aura Shimmering Candle" 
                                 class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-700">
                            <div class="absolute inset-0 bg-gradient-to-t from-forestGreen/60 via-transparent to-transparent"></div>
                            
                            <div class="absolute top-4 right-4 bg-forestGreen/90 text-shimmerGold text-xs font-bold px-3 py-1.5 rounded-full border border-shimmerGold/50 shadow-md">
                                ✨ Eco-Glitter Series
                            </div>

                            <div class="absolute bottom-6 left-6 right-6 bg-warmBeige/95 backdrop-blur-md p-4 rounded-2xl border border-sand shadow-lg">
                                <div class="flex items-center justify-between">
                                    <div>
                                        <p class="text-xs font-bold text-shimmerGold uppercase tracking-wider">Bestseller Aura</p>
                                        <h3 class="font-serif font-bold text-forestGreen text-base">Golden Vanilla & Shimmer Spice</h3>
                                    </div>
                                    <span class="text-base font-bold text-forestGreen">₹899</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Product Showcase Section -->
    <section id="shop" class="py-20 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex flex-col md:flex-row md:items-end justify-between mb-10 gap-6">
            <div>
                <span class="text-shimmerGold text-xs font-bold tracking-widest uppercase">Handcrafted Selection</span>
                <h2 class="font-serif text-3xl sm:text-4xl font-bold text-forestGreen mt-1">S|R Aura Candle Editions</h2>
                <p class="text-gray-600 mt-2 text-sm sm:text-base">100% Soy Wax • Premium Fragrances • Natural Eco-Glitter</p>
            </div>
            
            <!-- Category Filter Tabs -->
            <div id="filter-tabs" class="flex flex-wrap gap-2">
                <button data-filter="all" class="filter-btn bg-forestGreen text-cream px-4 py-2 rounded-xl text-xs font-medium transition-all">All Candles</button>
                <button data-filter="glitter" class="filter-btn bg-sand/60 hover:bg-sand text-forestGreen px-4 py-2 rounded-xl text-xs font-medium transition-all">✨ Shimmer & Glitter</button>
                <button data-filter="floral" class="filter-btn bg-sand/60 hover:bg-sand text-forestGreen px-4 py-2 rounded-xl text-xs font-medium transition-all">Floral & Botanical</button>
                <button data-filter="aromatherapy" class="filter-btn bg-sand/60 hover:bg-sand text-forestGreen px-4 py-2 rounded-xl text-xs font-medium transition-all">Mood Aromatherapy</button>
                <button data-filter="sets" class="filter-btn bg-sand/60 hover:bg-sand text-forestGreen px-4 py-2 rounded-xl text-xs font-medium transition-all">Gift Sets</button>
            </div>
        </div>

        <!-- Products Grid -->
        <div id="product-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
            <!-- Product cards dynamically populated by JS -->
        </div>
    </section>

    <!-- Brand Craft & USP Section -->
    <section id="craft" class="py-20 bg-softSage/50 border-y border-sand">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-16">
                <span class="text-shimmerGold text-xs font-bold tracking-widest uppercase block mb-2">Our Homemade Guarantee</span>
                <h2 class="font-serif text-3xl sm:text-4xl font-bold text-forestGreen">Why Choose S|R Aura - PRAKRITIC GLOW</h2>
                <p class="text-gray-600 text-sm sm:text-base mt-2">Every candle is hand-poured in small artisanal batches with natural ingredients.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <!-- Pillar 1 -->
                <div class="bg-cream p-6 rounded-3xl border border-sand text-center space-y-4 shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-14 h-14 mx-auto rounded-2xl bg-forestGreen/10 flex items-center justify-center text-shimmerGold text-2xl">
                        <i class="fa-solid fa-leaf"></i>
                    </div>
                    <h3 class="font-serif font-bold text-forestGreen text-lg">100% Pure Soy Wax</h3>
                    <p class="text-xs text-gray-600 leading-relaxed">Made from non-toxic, eco-friendly natural soy beans ensuring a soot-free, slow, and clean burn.</p>
                </div>

                <!-- Pillar 2 -->
                <div class="bg-cream p-6 rounded-3xl border border-sand text-center space-y-4 shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-14 h-14 mx-auto rounded-2xl bg-forestGreen/10 flex items-center justify-center text-shimmerGold text-2xl">
                        <i class="fa-solid fa-hands-holding-heart"></i>
                    </div>
                    <h3 class="font-serif font-bold text-forestGreen text-lg">100% Homemade</h3>
                    <p class="text-xs text-gray-600 leading-relaxed">Poured with love in small artisanal home batches, giving personal attention to every single jar.</p>
                </div>

                <!-- Pillar 3 -->
                <div class="bg-cream p-6 rounded-3xl border border-sand text-center space-y-4 shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-14 h-14 mx-auto rounded-2xl bg-forestGreen/10 flex items-center justify-center text-shimmerGold text-2xl">
                        <i class="fa-solid fa-sparkles"></i>
                    </div>
                    <h3 class="font-serif font-bold text-forestGreen text-lg">Natural Eco-Glitter</h3>
                    <p class="text-xs text-gray-600 leading-relaxed">Adorned with biodegradable glitter that melts into a magical glowing shimmer pool as it burns.</p>
                </div>

                <!-- Pillar 4 -->
                <div class="bg-cream p-6 rounded-3xl border border-sand text-center space-y-4 shadow-sm hover:shadow-md transition-shadow">
                    <div class="w-14 h-14 mx-auto rounded-2xl bg-forestGreen/10 flex items-center justify-center text-shimmerGold text-2xl">
                        <i class="fa-solid fa-droplet"></i>
                    </div>
                    <h3 class="font-serif font-bold text-forestGreen text-lg">Therapeutic Aromas</h3>
                    <p class="text-xs text-gray-600 leading-relaxed">Infused with natural essential oil blends to soothe stress, enhance mood, and elevate spaces.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Scent Finder Quiz Section -->
    <section id="scent-quiz" class="py-20 bg-warmBeige">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <span class="text-shimmerGold text-xs font-bold tracking-widest uppercase mb-2 block">Interactive Experience</span>
            <h2 class="font-serif text-3xl sm:text-4xl font-bold text-forestGreen mb-4">Find Your Signature Aura</h2>
            <p class="text-gray-600 text-sm sm:text-base max-w-lg mx-auto mb-10">Answer 3 quick questions to discover which PRAKRITIC GLOW fragrance matches your mood.</p>

            <!-- Quiz Box Container -->
            <div id="quiz-container" class="bg-cream rounded-3xl p-6 sm:p-10 shadow-xl border border-sand text-left relative overflow-hidden min-h-[340px] flex flex-col justify-between">
                
                <!-- Step 1 -->
                <div id="quiz-step-1" class="quiz-step">
                    <span class="text-xs font-semibold text-shimmerGold uppercase tracking-wider">Step 1 of 3</span>
                    <h3 class="font-serif text-2xl font-bold text-forestGreen mt-2 mb-6">What vibe do you want in your home right now?</h3>
                    <div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
                        <button onclick="nextQuizStep(1, 'calm')" class="quiz-option p-4 rounded-2xl border border-sand hover:border-shimmerGold hover:bg-softSage/30 transition-all text-left group">
                            <i class="fa-solid fa-spa text-shimmerGold text-xl mb-3 group-hover:scale-110 transition-transform"></i>
                            <h4 class="font-semibold text-forestGreen text-sm">Quiet & Relaxing</h4>
                            <p class="text-xs text-gray-500 mt-1">Deep meditation, calm sleep, or evening reading.</p>
                        </button>
                        <button onclick="nextQuizStep(1, 'glamour')" class="quiz-option p-4 rounded-2xl border border-sand hover:border-shimmerGold hover:bg-softSage/30 transition-all text-left group">
                            <i class="fa-solid fa-sparkles text-shimmerGold text-xl mb-3 group-hover:scale-110 transition-transform"></i>
                            <h4 class="font-semibold text-forestGreen text-sm">Festive & Shimmering</h4>
                            <p class="text-xs text-gray-500 mt-1">Special occasions, hosting guests, or romantic dinners.</p>
                        </button>
                        <button onclick="nextQuizStep(1, 'fresh')" class="quiz-option p-4 rounded-2xl border border-sand hover:border-shimmerGold hover:bg-softSage/30 transition-all text-left group">
                            <i class="fa-solid fa-wind text-shimmerGold text-xl mb-3 group-hover:scale-110 transition-transform"></i>
                            <h4 class="font-semibold text-forestGreen text-sm">Fresh & Energizing</h4>
                            <p class="text-xs text-gray-500 mt-1">Morning focus, yoga sessions, or refreshing your space.</p>
                        </button>
                    </div>
                </div>

                <!-- Step 2 -->
                <div id="quiz-step-2" class="quiz-step hidden">
                    <span class="text-xs font-semibold text-shimmerGold uppercase tracking-wider">Step 2 of 3</span>
                    <h3 class="font-serif text-2xl font-bold text-forestGreen mt-2 mb-6">Select your favorite natural scent note:</h3>
                    <div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
                        <button onclick="nextQuizStep(2, 'vanilla')" class="quiz-option p-4 rounded-2xl border border-sand hover:border-shimmerGold hover:bg-softSage/30 transition-all text-left">
                            <h4 class="font-semibold text-forestGreen text-sm">Warm Vanilla & Amber</h4>
                            <p class="text-xs text-gray-500 mt-1">Rich, sweet, and comforting notes.</p>
                        </button>
                        <button onclick="nextQuizStep(2, 'lavender')" class="quiz-option p-4 rounded-2xl border border-sand hover:border-shimmerGold hover:bg-softSage/30 transition-all text-left">
                            <h4 class="font-semibold text-forestGreen text-sm">Wild Lavender & Rose</h4>
                            <p class="text-xs text-gray-500 mt-1">Soothing floral garden bouquet.</p>
                        </button>
                        <button onclick="nextQuizStep(2, 'sandalwood')" class="quiz-option p-4 rounded-2xl border border-sand hover:border-shimmerGold hover:bg-softSage/30 transition-all text-left">
                            <h4 class="font-semibold text-forestGreen text-sm">Earthy Sandalwood & Cedar</h4>
                            <p class="text-xs text-gray-500 mt-1">Deep grounding natural forest woods.</p>
                        </button>
                    </div>
                </div>

                <!-- Step 3 -->
                <div id="quiz-step-3" class="quiz-step hidden">
                    <span class="text-xs font-semibold text-shimmerGold uppercase tracking-wider">Step 3 of 3</span>
                    <h3 class="font-serif text-2xl font-bold text-forestGreen mt-2 mb-6">Do you prefer Eco-Glitter shimmer in your candle wax?</h3>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <button onclick="showQuizResults(true)" class="quiz-option p-4 rounded-2xl border border-sand hover:border-shimmerGold hover:bg-softSage/30 transition-all text-left">
                            <h4 class="font-semibold text-forestGreen text-sm">✨ Yes! I love the glowing shimmer pool</h4>
                            <p class="text-xs text-gray-500 mt-1">Includes eco-friendly biodegradable glitter detailing.</p>
                        </button>
                        <button onclick="showQuizResults(false)" class="quiz-option p-4 rounded-2xl border border-sand hover:border-shimmerGold hover:bg-softSage/30 transition-all text-left">
                            <h4 class="font-semibold text-forestGreen text-sm">🌿 Natural Minimalistic Pure Soy</h4>
                            <p class="text-xs text-gray-500 mt-1">Classic pure botanical wax aesthetic.</p>
                        </button>
                    </div>
                </div>

                <!-- Quiz Result State -->
                <div id="quiz-results" class="quiz-step hidden text-center py-4">
                    <div class="inline-flex p-3 rounded-full bg-forestGreen/10 text-shimmerGold mb-4">
                        <i class="fa-solid fa-sparkles text-3xl"></i>
                    </div>
                    <h3 class="font-serif text-2xl font-bold text-forestGreen">Your S|R Aura Match Found!</h3>
                    <p class="text-xs text-gray-500 mt-1">Hand-picked matching Prakritic Glow candle:</p>
                    
                    <div id="quiz-recommended-card" class="mt-6 max-w-sm mx-auto bg-warmBeige p-4 rounded-2xl border border-sand flex items-center gap-4 text-left">
                        <!-- Populated dynamically -->
                    </div>

                    <button onclick="resetQuiz()" class="mt-6 text-xs text-shimmerGold hover:underline font-semibold">
                        <i class="fa-solid fa-rotate-left mr-1"></i> Retake Aura Quiz
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Customer Reviews / Social Proof -->
    <section id="reviews" class="py-20 bg-cream">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-14">
                <span class="text-shimmerGold text-xs font-bold tracking-widest uppercase">Love from Our Community</span>
                <h2 class="font-serif text-3xl sm:text-4xl font-bold text-forestGreen mt-2">Prakritic Glow Stories</h2>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Review Card 1 -->
                <div class="bg-warmBeige p-8 rounded-3xl border border-sand flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="space-y-4">
                        <div class="flex text-shimmerGold text-xs space-x-1">
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-gray-700 text-sm italic leading-relaxed">"The glitter shimmer when the soy wax melts is unbelievable! It looks like liquid gold. Plus the sandalwood fragrance calms my entire apartment."</p>
                    </div>
                    <div class="mt-6 flex items-center gap-3 pt-4 border-t border-sand">
                        <div class="w-10 h-10 rounded-full bg-forestGreen/10 font-bold text-forestGreen flex items-center justify-center text-xs">PS</div>
                        <div>
                            <h4 class="text-xs font-bold text-forestGreen">Priya Sharma</h4>
                            <span class="text-[10px] text-gray-400 flex items-center gap-1"><i class="fa-solid fa-circle-check text-emerald-600"></i> Verified Buyer</span>
                        </div>
                    </div>
                </div>

                <!-- Review Card 2 -->
                <div class="bg-warmBeige p-8 rounded-3xl border border-sand flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="space-y-4">
                        <div class="flex text-shimmerGold text-xs space-x-1">
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-gray-700 text-sm italic leading-relaxed">"Knowing these are 100% homemade pure soy candles makes such a difference. No chemical smell, just pure soothing lavender fragrance."</p>
                    </div>
                    <div class="mt-6 flex items-center gap-3 pt-4 border-t border-sand">
                        <div class="w-10 h-10 rounded-full bg-forestGreen/10 font-bold text-forestGreen flex items-center justify-center text-xs">RK</div>
                        <div>
                            <h4 class="text-xs font-bold text-forestGreen">Rohan Kapoor</h4>
                            <span class="text-[10px] text-gray-400 flex items-center gap-1"><i class="fa-solid fa-circle-check text-emerald-600"></i> Verified Buyer</span>
                        </div>
                    </div>
                </div>

                <!-- Review Card 3 -->
                <div class="bg-warmBeige p-8 rounded-3xl border border-sand flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
                    <div class="space-y-4">
                        <div class="flex text-shimmerGold text-xs space-x-1">
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                        </div>
                        <p class="text-gray-700 text-sm italic leading-relaxed">"I ordered the Prakritic Trio Gift set for Diwali and my family loved it! Beautiful packaging and eco-friendly glitter."</p>
                    </div>
                    <div class="mt-6 flex items-center gap-3 pt-4 border-t border-sand">
                        <div class="w-10 h-10 rounded-full bg-forestGreen/10 font-bold text-forestGreen flex items-center justify-center text-xs">AM</div>
                        <div>
                            <h4 class="text-xs font-bold text-forestGreen">Ananya Mehta</h4>
                            <span class="text-[10px] text-gray-400 flex items-center gap-1"><i class="fa-solid fa-circle-check text-emerald-600"></i> Verified Buyer</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Instagram Gallery Feed Mock -->
    <section class="py-12 bg-warmBeige border-t border-sand">
        <div class="max-w-7xl mx-auto px-4 text-center">
            <p class="text-xs font-semibold text-shimmerGold uppercase tracking-widest mb-2">Follow Our Journey</p>
            <h3 class="font-serif text-2xl font-bold text-forestGreen mb-8">@sraura.prakriticglow on Instagram</h3>
            
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-4">
                <div class="relative aspect-square rounded-2xl overflow-hidden group border border-sand">
                    <img src="https://images.unsplash.com/photo-1572635196237-14b3f281503f?auto=format&fit=crop&w=400&q=80" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500" alt="S|R Aura 1">
                    <div class="absolute inset-0 bg-forestGreen/40 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center text-cream">
                        <i class="fa-brands fa-instagram text-2xl text-shimmerGold"></i>
                    </div>
                </div>
                <div class="relative aspect-square rounded-2xl overflow-hidden group border border-sand">
                    <img src="https://images.unsplash.com/photo-1595425970377-c9703cf48b6d?auto=format&fit=crop&w=400&q=80" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500" alt="S|R Aura 2">
                    <div class="absolute inset-0 bg-forestGreen/40 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center text-cream">
                        <i class="fa-brands fa-instagram text-2xl text-shimmerGold"></i>
                    </div>
                </div>
                <div class="relative aspect-square rounded-2xl overflow-hidden group border border-sand">
                    <img src="https://images.unsplash.com/photo-1605651202774-7d573fd3f12d?auto=format&fit=crop&w=400&q=80" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500" alt="S|R Aura 3">
                    <div class="absolute inset-0 bg-forestGreen/40 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center text-cream">
                        <i class="fa-brands fa-instagram text-2xl text-shimmerGold"></i>
                    </div>
                </div>
                <div class="relative aspect-square rounded-2xl overflow-hidden group border border-sand">
                    <img src="https://images.unsplash.com/photo-1612196808214-b7e239e5f6b7?auto=format&fit=crop&w=400&q=80" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500" alt="S|R Aura 4">
                    <div class="absolute inset-0 bg-forestGreen/40 opacity-0 group-hover:opacity-100 transition-opacity flex items-center justify-center text-cream">
                        <i class="fa-brands fa-instagram text-2xl text-shimmerGold"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter Section -->
    <section class="py-16 bg-forestGreen text-cream">
        <div class="max-w-4xl mx-auto px-4 text-center space-y-6">
            <span class="text-shimmerGold text-xs font-semibold tracking-widest uppercase">Join S|R Aura Inner Circle</span>
            <h2 class="font-serif text-3xl sm:text-4xl font-bold">Receive 10% Off Your First Order</h2>
            <p class="text-sand/80 text-sm max-w-md mx-auto font-light">Subscribe for new homemade batch releases, glitter candle care tips, and exclusive discounts.</p>
            
            <form onsubmit="handleNewsletter(event)" class="flex flex-col sm:flex-row items-center justify-center gap-3 max-w-md mx-auto pt-2">
                <input type="email" required placeholder="Enter your email address" class="w-full bg-cream/10 border border-sand/30 rounded-xl px-4 py-3 text-sm text-cream placeholder:text-sand/50 focus:outline-none focus:border-shimmerGold">
                <button type="submit" class="w-full sm:w-auto bg-shimmerGold hover:bg-goldHover text-deepOlive font-bold px-6 py-3 rounded-xl text-sm transition-colors whitespace-nowrap">
                    Subscribe Now
                </button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer id="footer" class="bg-warmBeige border-t border-sand py-12 text-forestGreen text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-4 gap-8">
            <div class="space-y-3">
                <span class="font-serif text-xl font-bold">S<span class="text-shimmerGold">|</span>R Aura</span>
                <p class="text-xs uppercase tracking-widest text-shimmerGold font-bold">PRAKRITIC GLOW</p>
                <p class="text-gray-600 leading-relaxed">Handmade with 100% pure soy wax, soothing natural fragrances, and sparkling eco-glitter.</p>
                <div class="flex space-x-4 pt-2 text-base text-shimmerGold">
                    <a href="#" class="hover:text-forestGreen transition-colors"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#" class="hover:text-forestGreen transition-colors"><i class="fa-brands fa-whatsapp"></i></a>
                    <a href="#" class="hover:text-forestGreen transition-colors"><i class="fa-brands fa-facebook"></i></a>
                </div>
            </div>
            
            <div>
                <h4 class="font-bold uppercase tracking-wider text-xs mb-3 text-forestGreen">Our Collections</h4>
                <ul class="space-y-2 text-gray-600">
                    <li><a href="#shop" class="hover:text-shimmerGold transition-colors">✨ Eco-Glitter Shimmer Series</a></li>
                    <li><a href="#shop" class="hover:text-shimmerGold transition-colors">🌿 100% Pure Soy Botanical Jars</a></li>
                    <li><a href="#shop" class="hover:text-shimmerGold transition-colors">🌸 Floral & Lavender Editions</a></li>
                    <li><a href="#shop" class="hover:text-shimmerGold transition-colors">🎁 Prakritic Gift Sets</a></li>
                </ul>
            </div>

            <div>
                <h4 class="font-bold uppercase tracking-wider text-xs mb-3 text-forestGreen">Customer Service</h4>
                <ul class="space-y-2 text-gray-600">
                    <li><a href="#" class="hover:text-shimmerGold transition-colors">Track Your Order</a></li>
                    <li><a href="#" class="hover:text-shimmerGold transition-colors">Shipping & Returns</a></li>
                    <li><a href="#" class="hover:text-shimmerGold transition-colors">Pure Soy Care & Burning Tips</a></li>
                    <li><a href="#" class="hover:text-shimmerGold transition-colors">FAQ</a></li>
                </ul>
            </div>

            <div>
                <h4 class="font-bold uppercase tracking-wider text-xs mb-3 text-forestGreen">Homemade Studio Contact</h4>
                <p class="text-gray-600 mb-2"><i class="fa-solid fa-envelope text-shimmerGold mr-2"></i> contact@sraura.com</p>
                <p class="text-gray-600 mb-2"><i class="fa-solid fa-phone text-shimmerGold mr-2"></i> +91 98765 43210</p>
                <p class="text-gray-500 mt-3">Handcrafted in India with 100% love & soy wax.</p>
            </div>
        </div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-12 pt-6 border-t border-sand flex flex-col sm:flex-row items-center justify-between text-gray-500 gap-4">
            <p>© 2026 S|R Aura - PRAKRITIC GLOW. All rights reserved.</p>
            <div class="flex space-x-4 text-lg text-gray-400">
                <i class="fa-brands fa-cc-visa"></i>
                <i class="fa-brands fa-cc-mastercard"></i>
                <i class="fa-brands fa-google-pay"></i>
            </div>
        </div>
    </footer>

    <!-- Interactive Cart Drawer (Slide-Over Panel) -->
    <div id="cart-drawer-overlay" class="fixed inset-0 bg-forestGreen/60 z-50 opacity-0 pointer-events-none transition-opacity duration-300"></div>
    <div id="cart-drawer" class="fixed top-0 right-0 h-full w-full max-w-md bg-cream z-50 shadow-2xl cart-slide-over translate-x-full flex flex-col justify-between">
        <!-- Cart Header -->
        <div class="p-5 border-b border-sand flex items-center justify-between bg-warmBeige">
            <div class="flex items-center gap-2">
                <i class="fa-solid fa-sparkles text-shimmerGold"></i>
                <h3 class="font-serif text-xl font-bold text-forestGreen">Your Aura Bag</h3>
            </div>
            <button id="close-cart-btn" class="p-2 text-gray-400 hover:text-forestGreen transition-colors">
                <i class="fa-solid fa-xmark text-xl"></i>
            </button>
        </div>

        <!-- Free Shipping Progress Bar -->
        <div class="bg-softSage/40 p-4 border-b border-sand">
            <div class="flex justify-between text-xs font-semibold mb-1.5" id="shipping-progress-text">
                <span>Free Shipping Goal</span>
                <span id="shipping-needed-text">Add ₹201 more</span>
            </div>
            <div class="w-full bg-sand rounded-full h-2 overflow-hidden">
                <div id="shipping-bar" class="bg-shimmerGold h-full w-3/4 transition-all duration-300"></div>
            </div>
        </div>

        <!-- Cart Items List Container -->
        <div id="cart-items-container" class="flex-1 overflow-y-auto p-5 space-y-4 divide-y divide-sand">
            <!-- Dynamically populated via JavaScript -->
        </div>

        <!-- Cart Summary Footer -->
        <div class="p-5 border-t border-sand bg-warmBeige space-y-4">
            <!-- Promo Code Input -->
            <div class="flex gap-2">
                <input type="text" id="promo-input" placeholder="Promo Code (Try GLOW10)" class="flex-1 bg-cream border border-sand rounded-xl px-3 py-2 text-xs uppercase placeholder:normal-case focus:outline-none focus:border-shimmerGold">
                <button onclick="applyPromo()" class="bg-forestGreen hover:bg-deepOlive text-shimmerGold text-xs font-semibold px-4 py-2 rounded-xl transition-colors">Apply</button>
            </div>

            <!-- Pricing Breakdown -->
            <div class="space-y-1 text-xs">
                <div class="flex justify-between text-gray-600">
                    <span>Subtotal</span>
                    <span id="cart-subtotal" class="font-semibold text-forestGreen">₹0</span>
                </div>
                <div class="flex justify-between text-gray-600">
                    <span>Estimated Shipping</span>
                    <span id="cart-shipping-cost" class="font-semibold text-forestGreen">₹79</span>
                </div>
                <div id="discount-row" class="flex justify-between text-shimmerGold font-semibold hidden">
                    <span>Discount (10%)</span>
                    <span id="cart-discount">-₹0</span>
                </div>
                <div class="flex justify-between text-base font-bold text-forestGreen pt-2 border-t border-sand">
                    <span>Total</span>
                    <span id="cart-total">₹0</span>
                </div>
            </div>

            <!-- Checkout Button -->
            <button onclick="openCheckoutModal()" class="w-full bg-forestGreen hover:bg-deepOlive text-cream font-medium py-3.5 rounded-xl transition-colors shadow-lg flex items-center justify-center gap-2 border border-shimmerGold/30">
                <i class="fa-solid fa-lock text-xs text-shimmerGold"></i>
                <span>Proceed to Checkout</span>
            </button>
        </div>
    </div>

    <!-- Quick View Modal -->
    <div id="quick-view-modal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-forestGreen/60 opacity-0 pointer-events-none transition-opacity duration-300">
        <div class="bg-cream rounded-3xl max-w-3xl w-full max-h-[90vh] overflow-y-auto shadow-2xl border border-sand relative p-6 sm:p-8 transform scale-95 transition-transform duration-300" id="modal-content-box">
            <button onclick="closeQuickView()" class="absolute top-4 right-4 w-9 h-9 rounded-full bg-sand/60 hover:bg-sand flex items-center justify-center text-forestGreen transition-colors">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <div id="modal-body">
                <!-- Dynamically populated product details -->
            </div>
        </div>
    </div>

    <!-- Checkout Modal -->
    <div id="checkout-modal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-forestGreen/70 opacity-0 pointer-events-none transition-opacity duration-300">
        <div class="bg-cream rounded-3xl max-w-lg w-full p-6 sm:p-8 shadow-2xl border border-sand relative space-y-5">
            <button onclick="closeCheckoutModal()" class="absolute top-4 right-4 text-gray-400 hover:text-forestGreen">
                <i class="fa-solid fa-xmark text-xl"></i>
            </button>
            
            <div class="text-center">
                <span class="text-xs font-bold uppercase tracking-widest text-shimmerGold">S|R Aura Express Checkout</span>
                <h3 class="font-serif text-2xl font-bold text-forestGreen mt-1">Complete Your Order</h3>
            </div>

            <form onsubmit="completeOrder(event)" class="space-y-3">
                <div>
                    <label class="block text-xs font-semibold text-forestGreen mb-1">Full Name</label>
                    <input type="text" required placeholder="Enter your name" class="w-full bg-warmBeige border border-sand rounded-xl px-3 py-2 text-xs focus:outline-none focus:border-shimmerGold">
                </div>
                <div>
                    <label class="block text-xs font-semibold text-forestGreen mb-1">Phone Number (For Order Tracking updates)</label>
                    <input type="tel" required placeholder="+91 98765 43210" class="w-full bg-warmBeige border border-sand rounded-xl px-3 py-2 text-xs focus:outline-none focus:border-shimmerGold">
                </div>
                <div>
                    <label class="block text-xs font-semibold text-forestGreen mb-1">Shipping Address</label>
                    <textarea required rows="2" placeholder="Street, Apartment, City, Pincode" class="w-full bg-warmBeige border border-sand rounded-xl px-3 py-2 text-xs focus:outline-none focus:border-shimmerGold"></textarea>
                </div>
                <div>
                    <label class="block text-xs font-semibold text-forestGreen mb-1">Payment Method</label>
                    <select class="w-full bg-warmBeige border border-sand rounded-xl px-3 py-2 text-xs focus:outline-none focus:border-shimmerGold">
                        <option>UPI / GPay / PhonePe / Paytm</option>
                        <option>Credit / Debit Card</option>
                        <option>Cash on Delivery (COD)</option>
                    </select>
                </div>

                <div class="pt-3">
                    <button type="submit" class="w-full bg-forestGreen hover:bg-deepOlive text-cream font-bold py-3 rounded-xl text-xs transition-colors flex items-center justify-center gap-2 border border-shimmerGold/30">
                        <i class="fa-solid fa-check-circle text-shimmerGold"></i>
                        <span>Confirm & Place Order</span>
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- JavaScript Application Logic -->
    <script>
        // S|R Aura Candle Product Database
        const products = [
            {
                id: 1,
                name: "Golden Vanilla & Eco-Glitter Shimmer",
                category: "glitter",
                price: 899,
                rating: 5.0,
                reviewsCount: 142,
                image: "https://images.unsplash.com/photo-1603006905003-be475563bc59?auto=format&fit=crop&w=600&q=80",
                description: "100% Homemade pure soy wax candle adorned with golden eco-glitter that melts into a shimmering pool of warm Madagascar vanilla and amber fragrance.",
                scentNotes: { top: "Warm Madagascar Vanilla", heart: "Smoked Honey & Amber", base: "Golden Cedarwood" },
                burnTime: "45+ Hours",
                waxType: "100% Pure Soy Wax",
                glitterType: "Biodegradable Gold Eco-Glitter"
            },
            {
                id: 2,
                name: "Wild Lavender & French Rose",
                category: "floral",
                price: 799,
                rating: 4.9,
                reviewsCount: 98,
                image: "https://images.unsplash.com/photo-1608571423902-eed4a5ad8108?auto=format&fit=crop&w=600&q=80",
                description: "Hand-poured pure soy wax infused with calming French lavender oil and topped with dried botanical rose petals for serenity.",
                scentNotes: { top: "Wild French Lavender", heart: "Crushed Rose Petals", base: "White Musk" },
                burnTime: "40+ Hours",
                waxType: "100% Pure Soy Wax",
                glitterType: "Botanical Petals"
            },
            {
                id: 3,
                name: "Mysore Sandalwood Aromatherapy Jar",
                category: "aromatherapy",
                price: 949,
                rating: 4.8,
                reviewsCount: 76,
                image: "https://images.unsplash.com/photo-1572635196237-14b3f281503f?auto=format&fit=crop&w=600&q=80",
                description: "Deeply grounding therapeutic sandalwood oil blended with homemade pure soy wax to relieve stress and clear mind aura.",
                scentNotes: { top: "Crisp Bergamot", heart: "Mysore Sandalwood", base: "Earthy Vetiver" },
                burnTime: "50+ Hours",
                waxType: "100% Pure Soy Wax",
                glitterType: "Subtle Gold Mica Dust"
            },
            {
                id: 4,
                name: "Prakritic Trio Gift Set",
                category: "sets",
                price: 1999,
                rating: 5.0,
                reviewsCount: 165,
                image: "https://images.unsplash.com/photo-1543787729-166c4bf294db?auto=format&fit=crop&w=600&q=80",
                description: "Curated gift hamper containing 3 homemade mini soy candles (Golden Vanilla Glitter, Lavender Rose, and Sandalwood Aromatherapy).",
                scentNotes: { top: "3 Bestselling Fragrances", heart: "Vanilla, Lavender & Sandalwood", base: "Warm Essential Oils" },
                burnTime: "25 Hours x 3 Jars",
                waxType: "100% Pure Soy Wax",
                glitterType: "Assorted Eco-Glitter"
            },
            {
                id: 5,
                name: "Emerald Eucalyptus & Mint Shimmer",
                category: "glitter",
                price: 849,
                rating: 4.7,
                reviewsCount: 54,
                image: "https://images.unsplash.com/photo-1595425970377-c9703cf48b6d?auto=format&fit=crop&w=600&q=80",
                description: "Uplifting spearmint and blue gum eucalyptus with emerald green eco-glitter that sparkles brightly as it melts.",
                scentNotes: { top: "Fresh Spearmint", heart: "Blue Gum Eucalyptus", base: "Clean Sage" },
                burnTime: "45+ Hours",
                waxType: "100% Pure Soy Wax",
                glitterType: "Emerald Eco-Glitter"
            },
            {
                id: 6,
                name: "Jasmine & Honey Blossom Soy Jar",
                category: "floral",
                price: 799,
                rating: 4.9,
                reviewsCount: 82,
                image: "https://images.unsplash.com/photo-1605651202774-7d573fd3f12d?auto=format&fit=crop&w=600&q=80",
                description: "Sweet Indian Mogra jasmine blended with golden honey fragrance notes for a divine floral home atmosphere.",
                scentNotes: { top: "Indian Mogra Jasmine", heart: "Wild Honey Blossom", base: "Warm Tonka" },
                burnTime: "40+ Hours",
                waxType: "100% Pure Soy Wax",
                glitterType: "Natural Golden Sparkles"
            },
            {
                id: 7,
                name: "Cinnamon Spice & Warm Amber",
                category: "aromatherapy",
                price: 899,
                rating: 4.8,
                reviewsCount: 61,
                image: "https://images.unsplash.com/photo-1596434300655-e48d3ff3dd5e?auto=format&fit=crop&w=600&q=80",
                description: "Comforting clove, Ceylon cinnamon bark, and amber oil created to induce warm cozy vibes.",
                scentNotes: { top: "Ceylon Cinnamon Bark", heart: "Clove & Star Anise", base: "Warm Golden Amber" },
                burnTime: "45+ Hours",
                waxType: "100% Pure Soy Wax",
                glitterType: "Copper Shimmer Dust"
            },
            {
                id: 8,
                name: "Prakritic Sparkle Celebration Set",
                category: "sets",
                price: 2299,
                rating: 5.0,
                reviewsCount: 48,
                image: "https://images.unsplash.com/photo-1612196808214-b7e239e5f6b7?auto=format&fit=crop&w=600&q=80",
                description: "Festive set of 4 homemade glitter soy candles packaged in a handcrafted wooden box with wooden matches.",
                scentNotes: { top: "Festive Fragrance Selection", heart: "Assorted Floral & Spices", base: "Natural Essential Oils" },
                burnTime: "30 Hours x 4 Jars",
                waxType: "100% Pure Soy Wax",
                glitterType: "Full Shimmer Range"
            }
        ];

        // State
        let cart = [];
        let isPromoApplied = false;

        document.addEventListener('DOMContentLoaded', () => {
            renderProducts('all');
            setupFilterListeners();
            setupCartDrawer();
        });

        // Render Product Cards
        function renderProducts(filter) {
            const grid = document.getElementById('product-grid');
            grid.innerHTML = '';

            const filtered = filter === 'all' ? products : products.filter(p => p.category === filter);

            filtered.forEach(product => {
                const card = document.createElement('div');
                card.className = "group bg-cream rounded-3xl p-4 border border-sand shadow-sm hover:shadow-xl transition-all duration-300 flex flex-col justify-between fade-in";
                
                const isGlitter = product.category === 'glitter' || product.glitterType.includes('Glitter') || product.glitterType.includes('Sparkles');

                card.innerHTML = `
                    <div>
                        <!-- Image Container -->
                        <div class="relative aspect-square rounded-2xl overflow-hidden bg-sand/30 mb-4 cursor-pointer border border-sand" onclick="openQuickView(${product.id})">
                            <img src="${product.image}" alt="${product.name}" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                            
                            ${isGlitter ? `<span class="absolute top-3 left-3 bg-forestGreen text-shimmerGold text-[10px] font-bold px-2.5 py-1 rounded-full border border-shimmerGold/40 flex items-center gap-1"><i class="fa-solid fa-sparkles"></i> Eco-Glitter</span>` : `<span class="absolute top-3 left-3 bg-cream/90 text-forestGreen text-[10px] font-bold px-2.5 py-1 rounded-full border border-sand">100% Soy Wax</span>`}
                            
                            <button onclick="event.stopPropagation(); openQuickView(${product.id})" class="absolute bottom-3 right-3 bg-cream hover:bg-forestGreen hover:text-shimmerGold text-forestGreen text-xs px-3 py-2 rounded-xl font-medium shadow-md transition-all opacity-0 group-hover:opacity-100 flex items-center gap-1.5">
                                <i class="fa-regular fa-eye"></i> Quick View
                            </button>
                        </div>

                        <!-- Info -->
                        <div class="flex items-center space-x-1 text-shimmerGold text-xs mb-1">
                            <i class="fa-solid fa-star"></i>
                            <span class="font-semibold text-forestGreen text-xs ml-1">${product.rating}</span>
                            <span class="text-gray-400 text-[11px]">(${product.reviewsCount})</span>
                        </div>

                        <h3 class="font-serif font-bold text-forestGreen text-lg group-hover:text-shimmerGold transition-colors line-clamp-1">${product.name}</h3>
                        <p class="text-xs text-gray-500 mt-1 line-clamp-2 leading-relaxed">${product.description}</p>
                    </div>

                    <div class="mt-4 pt-4 border-t border-sand flex items-center justify-between">
                        <span class="font-bold text-forestGreen text-base">₹${product.price.toLocaleString('en-IN')}</span>
                        <button onclick="addToCart(${product.id})" class="bg-forestGreen hover:bg-deepOlive text-shimmerGold p-2.5 rounded-xl text-xs font-semibold transition-all flex items-center gap-1.5 border border-shimmerGold/30">
                            <i class="fa-solid fa-plus"></i> Add
                        </button>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        // Setup Filters
        function setupFilterListeners() {
            const buttons = document.querySelectorAll('.filter-btn');
            buttons.forEach(btn => {
                btn.addEventListener('click', (e) => {
                    buttons.forEach(b => {
                        b.classList.remove('bg-forestGreen', 'text-cream');
                        b.classList.add('bg-sand/60', 'text-forestGreen');
                    });
                    e.target.classList.remove('bg-sand/60', 'text-forestGreen');
                    e.target.classList.add('bg-forestGreen', 'text-cream');
                    
                    const filter = e.target.getAttribute('data-filter');
                    renderProducts(filter);
                });
            });

            // Mobile menu toggle
            const mobileBtn = document.getElementById('mobile-menu-btn');
            const mobileMenu = document.getElementById('mobile-menu');
            mobileBtn.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });
        }

        // Cart Handlers
        function setupCartDrawer() {
            const openBtn = document.getElementById('open-cart-btn');
            const closeBtn = document.getElementById('close-cart-btn');
            const overlay = document.getElementById('cart-drawer-overlay');
            const drawer = document.getElementById('cart-drawer');

            const openCart = () => {
                drawer.classList.remove('translate-x-full');
                overlay.classList.remove('opacity-0', 'pointer-events-none');
            };

            const closeCart = () => {
                drawer.classList.add('translate-x-full');
                overlay.classList.add('opacity-0', 'pointer-events-none');
            };

            openBtn.addEventListener('click', openCart);
            closeBtn.addEventListener('click', closeCart);
            overlay.addEventListener('click', closeCart);
        }

        // Cart Actions
        function addToCart(productId, qty = 1) {
            const product = products.find(p => p.id === productId);
            const existingItem = cart.find(item => item.id === productId);

            if (existingItem) {
                existingItem.quantity += qty;
            } else {
                cart.push({ ...product, quantity: qty });
            }

            updateCartUI();
            showToast(`Added ${product.name} to your bag ✨`);
        }

        function updateQuantity(productId, delta) {
            const item = cart.find(i => i.id === productId);
            if (!item) return;

            item.quantity += delta;
            if (item.quantity <= 0) {
                cart = cart.filter(i => i.id !== productId);
            }
            updateCartUI();
        }

        function updateCartUI() {
            const container = document.getElementById('cart-items-container');
            const countBadge = document.getElementById('cart-count-badge');
            
            const totalItemCount = cart.reduce((sum, item) => sum + item.quantity, 0);
            countBadge.innerText = totalItemCount;

            if (cart.length === 0) {
                container.innerHTML = `
                    <div class="text-center py-12 space-y-3">
                        <i class="fa-solid fa-sparkles text-4xl text-sand"></i>
                        <p class="text-sm font-medium text-gray-500">Your Prakritic Glow bag is empty.</p>
                        <a href="#shop" onclick="document.getElementById('close-cart-btn').click()" class="inline-block text-xs font-bold text-shimmerGold hover:underline">Explore Handmade Candles</a>
                    </div>
                `;
            } else {
                container.innerHTML = cart.map(item => `
                    <div class="py-3 flex items-center justify-between gap-3">
                        <img src="${item.image}" alt="${item.name}" class="w-16 h-16 rounded-xl object-cover border border-sand">
                        <div class="flex-1">
                            <h4 class="font-serif font-bold text-xs text-forestGreen">${item.name}</h4>
                            <p class="text-[11px] text-gray-500 mt-0.5">₹${item.price.toLocaleString('en-IN')}</p>
                            <div class="flex items-center gap-2 mt-2">
                                <button onclick="updateQuantity(${item.id}, -1)" class="w-5 h-5 rounded-md bg-sand hover:bg-sand/80 text-forestGreen text-xs flex items-center justify-center">-</button>
                                <span class="text-xs font-bold text-forestGreen">${item.quantity}</span>
                                <button onclick="updateQuantity(${item.id}, 1)" class="w-5 h-5 rounded-md bg-sand hover:bg-sand/80 text-forestGreen text-xs flex items-center justify-center">+</button>
                            </div>
                        </div>
                        <span class="font-bold text-xs text-forestGreen">₹${(item.price * item.quantity).toLocaleString('en-IN')}</span>
                    </div>
                `).join('');
            }

            const subtotal = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            const freeShippingThreshold = 999;
            const shippingCost = subtotal >= freeShippingThreshold || subtotal === 0 ? 0 : 79;
            const discount = isPromoApplied ? subtotal * 0.10 : 0;
            const grandTotal = Math.max(0, subtotal - discount + shippingCost);

            const progressPercent = Math.min(100, (subtotal / freeShippingThreshold) * 100);
            document.getElementById('shipping-bar').style.width = `${progressPercent}%`;
            
            const shippingNeededText = document.getElementById('shipping-needed-text');
            if (subtotal >= freeShippingThreshold) {
                shippingNeededText.innerText = "You unlocked FREE Shipping!";
                shippingNeededText.className = "text-emerald-700 font-bold";
            } else {
                const diff = freeShippingThreshold - subtotal;
                shippingNeededText.innerText = `Add ₹${diff.toLocaleString('en-IN')} more`;
                shippingNeededText.className = "text-forestGreen";
            }

            document.getElementById('cart-subtotal').innerText = `₹${subtotal.toLocaleString('en-IN')}`;
            document.getElementById('cart-shipping-cost').innerText = shippingCost === 0 ? "FREE" : `₹${shippingCost}`;
            
            if (isPromoApplied) {
                document.getElementById('discount-row').classList.remove('hidden');
                document.getElementById('cart-discount').innerText = `-₹${discount.toLocaleString('en-IN')}`;
            }

            document.getElementById('cart-total').innerText = `₹${grandTotal.toLocaleString('en-IN')}`;
        }

        function applyPromo() {
            const input = document.getElementById('promo-input');
            if (input.value.trim().toUpperCase() === 'GLOW10') {
                isPromoApplied = true;
                showToast("10% PRAKRITIC GLOW Discount Applied!");
                updateCartUI();
            } else {
                showToast("Invalid Promo Code (Try GLOW10)");
            }
        }

        // Quick View Modal
        function openQuickView(productId) {
            const product = products.find(p => p.id === productId);
            const modal = document.getElementById('quick-view-modal');
            const modalContent = document.getElementById('modal-content-box');
            const body = document.getElementById('modal-body');

            body.innerHTML = `
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 items-center">
                    <div class="aspect-square rounded-2xl overflow-hidden bg-sand/30 border border-sand relative">
                        <img src="${product.image}" alt="${product.name}" class="w-full h-full object-cover">
                        <span class="absolute top-3 left-3 bg-forestGreen text-shimmerGold text-xs font-bold px-3 py-1 rounded-full border border-shimmerGold/40">
                            ✨ ${product.glitterType}
                        </span>
                    </div>
                    <div class="space-y-4">
                        <span class="text-[10px] font-bold text-shimmerGold uppercase tracking-widest">S|R Aura Handmade Collection</span>
                        <h2 class="font-serif text-2xl font-bold text-forestGreen">${product.name}</h2>
                        
                        <div class="flex items-center space-x-2 text-shimmerGold text-xs">
                            <i class="fa-solid fa-star"></i>
                            <span class="font-bold text-forestGreen">${product.rating}</span>
                            <span class="text-gray-400">(${product.reviewsCount} reviews)</span>
                        </div>
                        
                        <p class="text-2xl font-bold text-forestGreen">₹${product.price.toLocaleString('en-IN')}</p>
                        <p class="text-xs text-gray-600 leading-relaxed">${product.description}</p>
                        
                        <!-- Fragrance Notes -->
                        <div class="bg-warmBeige p-3 rounded-xl border border-sand space-y-1 text-xs">
                            <p><strong class="text-forestGreen">Top Notes:</strong> ${product.scentNotes.top}</p>
                            <p><strong class="text-forestGreen">Heart Notes:</strong> ${product.scentNotes.heart}</p>
                            <p><strong class="text-forestGreen">Base Notes:</strong> ${product.scentNotes.base}</p>
                        </div>

                        <div class="flex items-center gap-4 text-xs text-gray-500 py-1">
                            <span><i class="fa-solid fa-leaf text-shimmerGold mr-1"></i> ${product.waxType}</span>
                            <span><i class="fa-solid fa-clock text-shimmerGold mr-1"></i> ${product.burnTime}</span>
                        </div>

                        <button onclick="addToCart(${product.id}); closeQuickView();" class="w-full bg-forestGreen hover:bg-deepOlive text-cream font-medium py-3 rounded-xl transition-all shadow-md flex items-center justify-center gap-2 border border-shimmerGold/30">
                            <i class="fa-solid fa-bag-shopping text-shimmerGold"></i> Add to Aura Bag
                        </button>
                    </div>
                </div>
            `;

            modal.classList.remove('opacity-0', 'pointer-events-none');
            modalContent.classList.remove('scale-95');
            modalContent.classList.add('scale-100');
        }

        function closeQuickView() {
            const modal = document.getElementById('quick-view-modal');
            const modalContent = document.getElementById('modal-content-box');
            modal.classList.add('opacity-0', 'pointer-events-none');
            modalContent.classList.remove('scale-100');
            modalContent.classList.add('scale-95');
        }

        // Checkout Modal Logic
        function openCheckoutModal() {
            if (cart.length === 0) {
                showToast("Your bag is empty!");
                return;
            }
            document.getElementById('close-cart-btn').click();
            const modal = document.getElementById('checkout-modal');
            modal.classList.remove('opacity-0', 'pointer-events-none');
        }

        function closeCheckoutModal() {
            const modal = document.getElementById('checkout-modal');
            modal.classList.add('opacity-0', 'pointer-events-none');
        }

        function completeOrder(e) {
            e.preventDefault();
            closeCheckoutModal();
            cart = [];
            updateCartUI();
            showToast("✨ Order Placed Successfully! Thank you for choosing S|R Aura.");
        }

        // Quiz Logic
        let quizAnswers = {};
        function nextQuizStep(step, val) {
            quizAnswers[step] = val;
            document.getElementById(`quiz-step-${step}`).classList.add('hidden');
            document.getElementById(`quiz-step-${step + 1}`).classList.remove('hidden');
        }

        function showQuizResults(hasGlitter) {
            document.getElementById('quiz-step-3').classList.add('hidden');
            document.getElementById('quiz-results').classList.remove('hidden');

            const recommended = hasGlitter ? products[0] : products[1]; 
            const cardContainer = document.getElementById('quiz-recommended-card');

            cardContainer.innerHTML = `
                <img src="${recommended.image}" alt="${recommended.name}" class="w-16 h-16 rounded-xl object-cover border border-sand">
                <div class="flex-1">
                    <h4 class="font-serif font-bold text-xs text-forestGreen">${recommended.name}</h4>
                    <p class="text-[11px] text-shimmerGold font-bold">₹${recommended.price.toLocaleString('en-IN')}</p>
                    <button onclick="addToCart(${recommended.id})" class="mt-2 text-[10px] bg-forestGreen text-shimmerGold px-3 py-1.5 rounded-lg font-bold border border-shimmerGold/30">
                        Add Recommended Candle
                    </button>
                </div>
            `;
        }

        function resetQuiz() {
            document.getElementById('quiz-results').classList.add('hidden');
            document.getElementById('quiz-step-1').classList.remove('hidden');
            quizAnswers = {};
        }

        // Toast Helper
        function showToast(message) {
            const toast = document.getElementById('toast');
            const toastMessage = document.getElementById('toast-message');
            toastMessage.innerText = message;
            
            toast.classList.remove('translate-y-24', 'opacity-0');
            setTimeout(() => {
                toast.classList.add('translate-y-24', 'opacity-0');
            }, 3200);
        }

        function handleNewsletter(e) {
            e.preventDefault();
            showToast("Welcome to S|R Aura Inner Circle! 10% code sent to your email.");
            e.target.reset();
        }
    </script>
</body>
</html>
