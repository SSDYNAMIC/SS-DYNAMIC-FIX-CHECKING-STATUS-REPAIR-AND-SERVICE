# SS-DYNAMIC-FIX-CHECKING-STATUS-REPAIR-AND-SERVICE
SS DYNAMIC FIX CHECKING STATUS REPAIR AND SERVICE
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SS DYNAMIC FIX - Phone & Laptop Repair Specialist</title>
<script src="https://cdn.tailwindcss.com"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
<style>
    :root {
        --red: #dc2626;
        --red-dark: #b91c1c;
        --black: #0a0a0a;
        --black-light: #1a1a1a;
        --gray: #1f1f1f;
    }
    
    * {
        scroll-behavior: smooth;
    }
    
    body {
        font-family: 'Inter', system-ui, -apple-system, sans-serif;
        background-color: var(--black);
        color: #f5f5f5;
    }
    
    .hero-bg {
        background: linear-gradient(135deg, rgba(10,10,10,0.95) 0%, rgba(220,38,38,0.2) 100%), 
                    url('https://images.unsplash.com/photo-1588702547919-26089e690ecc?q=80&w=2070&auto=format&fit=crop') center/cover;
    }
    
    .glass {
        background: rgba(31, 31, 31, 0.7);
        backdrop-filter: blur(12px);
        border: 1px solid rgba(220, 38, 38, 0.2);
    }
    
    .card-hover {
        transition: all 0.3s ease;
    }
    
    .card-hover:hover {
        transform: translateY(-8px);
        box-shadow: 0 20px 40px rgba(220, 38, 38, 0.3);
    }
    
    .btn-primary {
        background: linear-gradient(135deg, var(--red) 0%, var(--red-dark) 100%);
        transition: all 0.3s ease;
    }
    
    .btn-primary:hover {
        background: linear-gradient(135deg, var(--red-dark) 0%, #991b1b 100%);
        box-shadow: 0 10px 25px rgba(220, 38, 38, 0.4);
        transform: translateY(-2px);
    }
    
    .nav-link {
        position: relative;
    }
    
    .nav-link::after {
        content: '';
        position: absolute;
        width: 0;
        height: 2px;
        bottom: -4px;
        left: 0;
        background: var(--red);
        transition: width 0.3s ease;
    }
    
    .nav-link:hover::after, .nav-link.active::after {
        width: 100%;
    }
    
    .floating-whatsapp {
        position: fixed;
        bottom: 24px;
        right: 24px;
        z-index: 999;
        animation: pulse 2s infinite;
    }
    
    @keyframes pulse {
        0%, 100% { transform: scale(1); }
        50% { transform: scale(1.1); }
    }
    
    .status-badge {
        padding: 4px 12px;
        border-radius: 9999px;
        font-size: 0.75rem;
        font-weight: 600;
    }
    
    .status-received { background: #3b82f6; color: white; }
    .status-diagnosing { background: #f59e0b; color: white; }
    .status-repairing { background: #8b5cf6; color: white; }
    .status-testing { background: #06b6d4; color: white; }
    .status-completed { background: #10b981; color: white; }
    .status-collected { background: #6b7280; color: white; }
    
    .admin-view, .main-view {
        display: none;
    }
    
    .admin-view.active, .main-view.active {
        display: block;
    }
    
    @media (max-width: 390px) {
        .floating-whatsapp {
            bottom: 16px;
            right: 16px;
        }
    }
</style>
</head>
<body>
    <!-- Main Website View -->
    <div id="mainView" class="main-view active">
        <!-- Navigation -->
        <nav class="glass fixed w-full top-0 z-50">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex justify-between items-center h-16">
                    <div class="flex items-center gap-3">
                        <div class="bg-gradient-to-br from-red-600 to-red-800 p-2 rounded-lg">
                            <i class="fas fa-mobile-alt text-white text-xl"></i>
                        </div>
                        <div>
                            <h1 class="text-lg sm:text-xl font-bold text-white">SS DYNAMIC FIX</h1>
                            <p class="text-xs text-gray-400 hidden sm:block">Phone & Laptop Specialist</p>
                        </div>
                    </div>
                    
                    <div class="hidden md:flex items-center gap-6">
                        <a href="#home" class="nav-link text-sm font-medium text-gray-300 hover:text-white">Home</a>
                        <a href="#services" class="nav-link text-sm font-medium text-gray-300 hover:text-white">Services</a>
                        <a href="#check-status" class="nav-link text-sm font-medium text-gray-300 hover:text-white">Check Status</a>
                        <a href="#repair-request" class="nav-link text-sm font-medium text-gray-300 hover:text-white">Request Repair</a>
                        <a href="#about" class="nav-link text-sm font-medium text-gray-300 hover:text-white">About</a>
                        <a href="#contact" class="nav-link text-sm font-medium text-gray-300 hover:text-white">Contact</a>
                        <button onclick="showAdminLogin()" class="btn-primary px-4 py-2 rounded-lg text-sm font-semibold">
                            <i class="fas fa-lock mr-2"></i>Admin
                        </button>
                    </div>
                    
                    <button id="mobileMenuBtn" class="md:hidden text-white p-2">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
            
            <!-- Mobile Menu -->
            <div id="mobileMenu" class="hidden md:hidden glass border-t border-red-900/30">
                <div class="px-4 py-3 space-y-2">
                    <a href="#home" class="block py-2 text-gray-300 hover:text-white">Home</a>
                    <a href="#services" class="block py-2 text-gray-300 hover:text-white">Services</a>
                    <a href="#check-status" class="block py-2 text-gray-300 hover:text-white">Check Status</a>
                    <a href="#repair-request" class="block py-2 text-gray-300 hover:text-white">Request Repair</a>
                    <a href="#about" class="block py-2 text-gray-300 hover:text-white">About</a>
                    <a href="#contact" class="block py-2 text-gray-300 hover:text-white">Contact</a>
                    <button onclick="showAdminLogin()" class="btn-primary w-full px-4 py-2 rounded-lg text-sm font-semibold mt-2">
                        <i class="fas fa-lock mr-2"></i>Admin Login
                    </button>
                </div>
            </div>
        </nav>

        <!-- Hero Section -->
        <section id="home" class="hero-bg min-h-screen flex items-center pt-16">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 w-full">
                <div class="grid md:grid-cols-2 gap-12 items-center">
                    <div class="space-y-6">
                        <div class="inline-block glass px-4 py-2 rounded-full">
                            <span class="text-sm font-semibold text-red-500"><i class="fas fa-circle text-xs animate-pulse mr-2"></i>Expert Repair Services</span>
                        </div>
                        <h2 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold leading-tight">
                            Your Trusted <span class="text-transparent bg-clip-text bg-gradient-to-r from-red-500 to-red-700">Device Repair</span> Center
                        </h2>
                        <p class="text-lg text-gray-300 leading-relaxed">
                            Professional phone & laptop repair services with certified technicians. Fast turnaround, genuine parts, and 90-day warranty on all repairs.
                        </p>
                        <div class="flex flex-wrap gap-4 pt-4">
                            <a href="#repair-request" class="btn-primary px-8 py-4 rounded-lg font-semibold text-white inline-flex items-center gap-2">
                                <i class="fas fa-wrench"></i> Request Repair
                            </a>
                            <a href="#check-status" class="glass px-8 py-4 rounded-lg font-semibold text-white inline-flex items-center gap-2 hover:bg-red-900/20 transition">
                                <i class="fas fa-search"></i> Track Status
                            </a>
                        </div>
                        <div class="grid grid-cols-3 gap-4 pt-8">
                            <div class="text-center">
                                <div class="text-3xl font-bold text-red-500">5K+</div>
                                <div class="text-sm text-gray-400">Devices Fixed</div>
                            </div>
                            <div class="text-center">
                                <div class="text-3xl font-bold text-red-500">4.9★</div>
                                <div class="text-sm text-gray-400">Customer Rating</div>
                            </div>
                            <div class="text-center">
                                <div class="text-3xl font-bold text-red-500">24h</div>
                                <div class="text-sm text-gray-400">Avg Turnaround</div>
                            </div>
                        </div>
                    </div>
                    <div class="hidden md:block">
                        <div class="glass rounded-2xl p-8 space-y-4">
                            <h3 class="text-2xl font-bold mb-4">Why Choose Us?</h3>
                            <div class="space-y-3">
                                <div class="flex items-start gap-3">
                                    <div class="bg-red-600 p-2 rounded-lg mt-1"><i class="fas fa-check"></i></div>
                                    <div>
                                        <div class="font-semibold">Certified Technicians</div>
                                        <div class="text-sm text-gray-400">Apple, Samsung & Microsoft certified</div>
                                    </div>
                                </div>
                                <div class="flex items-start gap-3">
                                    <div class="bg-red-600 p-2 rounded-lg mt-1"><i class="fas fa-shield-alt"></i></div>
                                    <div>
                                        <div class="font-semibold">90-Day Warranty</div>
                                        <div class="text-sm text-gray-400">All repairs covered</div>
                                    </div>
                                </div>
                                <div class="flex items-start gap-3">
                                    <div class="bg-red-600 p-2 rounded-lg mt-1"><i class="fas fa-bolt"></i></div>
                                    <div>
                                        <div class="font-semibold">Same Day Service</div>
                                        <div class="text-sm text-gray-400">Most repairs done in hours</div>
                                    </div>
                                <div class="flex items-start gap-3">
                                    <div class="bg-red-600 p-2 rounded-lg mt-1"><i class="fas fa-dollar-sign"></i></div>
                                    <div>
                                        <div class="font-semibold">Fair Pricing</div>
                                        <div class="text-sm text-gray-400">No hidden costs, free diagnosis</div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="py-20 bg-gradient-to-b from-black to-gray-900">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <span class="text-red-500 font-semibold text-sm uppercase tracking-wider">Our Services</span>
                    <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold mt-2 mb-4">Phone & Laptop Repair Solutions</h2>
                    <p class="text-gray-400 max-w-2xl mx-auto">We specialize in all types of device repairs using genuine parts and latest diagnostic tools</p>
                </div>

                <div class="grid md:grid-cols-2 gap-8 mb-12">
                    <!-- Phone Repair -->
                    <div class="glass rounded-2xl p-8 card-hover">
                        <div class="bg-gradient-to-br from-red-600 to-red-800 w-16 h-16 rounded-xl flex items-center justify-center mb-6">
                            <i class="fas fa-mobile-alt text-3xl"></i>
                        </div>
                        <h3 class="text-2xl font-bold mb-4">Phone Repair Services</h3>
                        <div class="space-y-3">
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Screen & LCD Replacement</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Battery Replacement</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Charging Port Repair</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Water Damage Treatment</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Camera & Speaker Fix</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Software Issues & Unlocking</span>
                            </div>
                        </div>
                        <p class="text-sm text-gray-400 mt-4">iPhone, Samsung, Huawei, Xiaomi, Oppo, Vivo & more</p>
                    </div>

                    <!-- Laptop Repair -->
                    <div class="glass rounded-2xl p-8 card-hover">
                        <div class="bg-gradient-to-br from-red-600 to-red-800 w-16 h-16 rounded-xl flex items-center justify-center mb-6">
                            <i class="fas fa-laptop text-3xl"></i>
                        </div>
                        <h3 class="text-2xl font-bold mb-4">Laptop Repair Services</h3>
                        <div class="space-y-3">
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Screen Replacement</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Keyboard & Trackpad Repair</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Motherboard & Chip Repair</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>SSD/HDD Upgrade & Data Recovery</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>Fan & Overheating Fix</span>
                            </div>
                            <div class="flex items-center gap-3">
                                <i class="fas fa-check-circle text-red-500"></i>
                                <span>OS Installation & Virus Removal</span>
                            </div>
                        <p class="text-sm text-gray-400 mt-4">MacBook, Dell, HP, Lenovo, Asus, Acer & more</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Check Status Section -->
        <section id="check-status" class="py-20 bg-gray-900">
            <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-12">
                    <span class="text-red-500 font-semibold text-sm uppercase tracking-wider">Track Repair</span>
                    <h2 class="text-3xl sm:text-4xl font-bold mt-2 mb-4">Check Your Repair Status</h2>
                    <p class="text-gray-400">Enter your ticket number to see real-time updates</p>
                </div>

                <div class="glass rounded-2xl p-6 sm:p-8">
                    <div class="flex flex-col sm:flex-row gap-4 mb-6">
                        <input type="text" id="ticketSearch" placeholder="Enter Ticket Number (e.g. SSD-123456)" 
                               class="flex-1 px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white">
                        <button onclick="checkStatus()" class="btn-primary px-8 py-3 rounded-lg font-semibold whitespace-nowrap">
                            <i class="fas fa-search mr-2"></i>Check Status
                        </button>
                    </div>
                    
                    <div id="statusResult" class="hidden">
                        <!-- Results will appear here -->
                    </div>
                </div>
            </div>
        </section>

        <!-- Repair Request Form -->
        <section id="repair-request" class="py-20 bg-gradient-to-b from-gray-900 to-black">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-12">
                    <span class="text-red-500 font-semibold text-sm uppercase tracking-wider">Get Started</span>
                    <h2 class="text-3xl sm:text-4xl font-bold mt-2 mb-4">Submit Repair Request</h2>
                    <p class="text-gray-400">Fill out the form and we'll contact you within 1 hour</p>
                </div>

                <div class="glass rounded-2xl p-6 sm:p-8">
                    <form id="repairForm" onsubmit="submitRepair(event)">
                        <div class="grid sm:grid-cols-2 gap-6 mb-6">
                            <div>
                                <label class="block text-sm font-medium mb-2">Full Name *</label>
                                <input type="text" name="name" required 
                                       class="w-full px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white">
                            </div>
                            <div>
                                <label class="block text-sm font-medium mb-2">Phone Number *</label>
                                <input type="tel" name="phone" required 
                                       class="w-full px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white">
                            </div>
                        </div>

                        <div class="grid sm:grid-cols-2 gap-6 mb-6">
                            <div>
                                <label class="block text-sm font-medium mb-2">Email</label>
                                <input type="email" name="email" 
                                       class="w-full px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white">
                            </div>
                            <div>
                                <label class="block text-sm font-medium mb-2">Device Type *</label>
                                <select name="deviceType" required 
                                        class="w-full px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white">
                                    <option value="">Select Device</option>
                                    <option value="Phone">Phone</option>
                                    <option value="Laptop">Laptop</option>
                                    <option value="Tablet">Tablet</option>
                                    <option value="Other">Other</option>
                                </select>
                            </div>
                        </div>

                        <div class="grid sm:grid-cols-2 gap-6 mb-6">
                            <div>
                                <label class="block text-sm font-medium mb-2">Brand & Model *</label>
                                <input type="text" name="model" placeholder="e.g. iPhone 14 Pro" required 
                                       class="w-full px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white">
                            </div>
                            <div>
                                <label class="block text-sm font-medium mb-2">Issue Type *</label>
                                <select name="issueType" required 
                                        class="w-full px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white">
                                    <option value="">Select Issue</option>
                                    <option value="Screen Cracked">Screen Cracked</option>
                                    <option value="Battery Problem">Battery Problem</option>
                                    <option value="Water Damage">Water Damage</option>
                                    <option value="Not Turning On">Not Turning On</option>
                                    <option value="Charging Issue">Charging Issue</option>
                                    <option value="Software Issue">Software Issue</option>
                                    <option value="Other">Other</option>
                                </select>
                            </div>
                        </div>

                        <div class="mb-6">
                            <label class="block text-sm font-medium mb-2">Problem Description *</label>
                            <textarea name="description" rows="4" required 
                                      placeholder="Please describe the issue in detail..."
                                      class="w-full px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white"></textarea>
                        </div>

                        <div class="flex items-center gap-3 mb-6">
                            <input type="checkbox" id="urgent" name="urgent" class="w-4 h-4 accent-red-600">
                            <label for="urgent" class="text-sm">This is urgent - I need same day service if possible</label>
                        </div>

                        <button type="submit" class="btn-primary w-full py-4 rounded-lg font-semibold text-white text-lg">
                            <i class="fas fa-paper-plane mr-2"></i>Submit Request
                        </button>
                    </form>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="py-20 bg-black">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid md:grid-cols-2 gap-12 items-center">
                    <div>
                        <span class="text-red-500 font-semibold text-sm uppercase tracking-wider">About Us</span>
                        <h2 class="text-3xl sm:text-4xl font-bold mt-2 mb-6">SS DYNAMIC TELECOMMUNICATION</h2>
                        <p class="text-gray-300 mb-4 leading-relaxed">
                            Established as a premier device repair center in Alor Gajah, Melaka, SS DYNAMIC FIX has been serving the community with expert phone and laptop repair services.
                        </p>
                        <p class="text-gray-300 mb-6 leading-relaxed">
                            Our certified technicians use genuine parts and professional-grade equipment to ensure your device is repaired to factory standards. We pride ourselves on transparency, quality workmanship, and exceptional customer service.
                        </p>
                        <div class="glass rounded-xl p-6 mb-6">
                            <div class="flex items-start gap-4">
                                <div class="bg-red-600 p-3 rounded-lg">
                                    <i class="fas fa-building text-xl"></i>
                                </div>
                                <div>
                                    <div class="font-semibold mb-2">Company Registration</div>
                                    <div class="text-gray-400">SS DYNAMIC TELECOMMUNICATION</div>
                                    <div class="text-sm text-gray-500">MA0200450</div>
                                </div>
                            </div>
                        </div>
                        <div class="grid grid-cols-2 gap-4">
                            <div class="glass rounded-lg p-4 text-center">
                                <div class="text-3xl font-bold text-red-500 mb-1">10+</div>
                                <div class="text-sm text-gray-400">Years Experience</div>
                            </div>
                            <div class="glass rounded-lg p-4 text-center">
                                <div class="text-3xl font-bold text-red-500 mb-1">5000+</div>
                                <div class="text-sm text-gray-400">Happy Clients</div>
                            </div>
                        </div>
                    </div>
                    <div class="glass rounded-2xl p-8">
                        <h3 class="text-2xl font-bold mb-6">Our Commitment</h3>
                        <div class="space-y-4">
                            <div class="flex gap-4">
                                <div class="bg-red-600/20 p-3 rounded-lg h-fit">
                                    <i class="fas fa-certificate text-red-500"></i>
                                </div>
                                <div>
                                    <div class="font-semibold mb-1">Certified Quality</div>
                                    <div class="text-sm text-gray-400">All technicians certified and trained</div>
                                </div>
                            </div>
                            <div class="flex gap-4">
                                <div class="bg-red-600/20 p-3 rounded-lg h-fit">
                                    <i class="fas fa-tools text-red-500"></i>
                                </div>
                                <div>
                                    <div class="font-semibold mb-1">Genuine Parts</div>
                                    <div class="text-sm text-gray-400">Only OEM or premium quality parts used</div>
                                </div>
                            </div>
                            <div class="flex gap-4">
                                <div class="bg-red-600/20 p-3 rounded-lg h-fit">
                                    <i class="fas fa-clock text-red-500"></i>
                                </div>
                                <div>
                                    <div class="font-semibold mb-1">Fast Turnaround</div>
                                    <div class="text-sm text-gray-400">Most repairs completed same day</div>
                                </div>
                            </div>
                            <div class="flex gap-4">
                                <div class="bg-red-600/20 p-3 rounded-lg h-fit">
                                    <i class="fas fa-hand-holding-usd text-red-500"></i>
                                </div>
                                <div>
                                    <div class="font-semibold mb-1">Best Price Guarantee</div>
                                    <div class="text-sm text-gray-400">Free diagnosis, no fix no fee</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="py-20 bg-gradient-to-b from-black to-gray-900">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-12">
                    <span class="text-red-500 font-semibold text-sm uppercase tracking-wider">Get In Touch</span>
                    <h2 class="text-3xl sm:text-4xl font-bold mt-2 mb-4">Visit Our Service Center</h2>
                    <p class="text-gray-400">We're here to help you 7 days a week</p>
                </div>

                <div class="grid md:grid-cols-3 gap-6">
                    <div class="glass rounded-2xl p-6 text-center card-hover">
                        <div class="bg-gradient-to-br from-red-600 to-red-800 w-14 h-14 rounded-xl flex items-center justify-center mx-auto mb-4">
                            <i class="fas fa-map-marker-alt text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Location</h3>
                        <p class="text-gray-400 text-sm leading-relaxed">
                            NO 2, BANGUNAN TERMINAL BAS<br>
                            KOMPLEKS AG SENTRAL<br>
                            78000 ALOR GAJAH<br>
                            MELAKA
                        </p>
                    </div>

                    <div class="glass rounded-2xl p-6 text-center card-hover">
                        <div class="bg-gradient-to-br from-red-600 to-red-800 w-14 h-14 rounded-xl flex items-center justify-center mx-auto mb-4">
                            <i class="fas fa-phone text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">Call Us</h3>
                        <a href="tel:+601151453147" class="text-red-500 font-semibold hover:text-red-400">
                            +601151453147
                        </a>
                        <p class="text-gray-400 text-sm mt-2">Mon-Sun: 9:00 AM - 9:00 PM</p>
                    </div>

                    <div class="glass rounded-2xl p-6 text-center card-hover">
                        <div class="bg-gradient-to-br from-red-600 to-red-800 w-14 h-14 rounded-xl flex items-center justify-center mx-auto mb-4">
                            <i class="fab fa-whatsapp text-2xl"></i>
                        </div>
                        <h3 class="text-xl font-bold mb-3">WhatsApp</h3>
                        <a href="https://wa.me/601151453147" target="_blank" class="text-red-500 font-semibold hover:text-red-400">
                            Chat With Us
                        </a>
                        <p class="text-gray-400 text-sm mt-2">Quick Response Guaranteed</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="bg-black border-t border-gray-800 py-12">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid md:grid-cols-4 gap-8 mb-8">
                    <div>
                        <div class="flex items-center gap-3 mb-4">
                            <div class="bg-gradient-to-br from-red-600 to-red-800 p-2 rounded-lg">
                                <i class="fas fa-mobile-alt text-white"></i>
                            </div>
                            <div>
                                <h3 class="font-bold text-white">SS DYNAMIC FIX</h3>
                                <p class="text-xs text-gray-500">MA0200450</p>
                            </div>
                        </div>
                        <p class="text-gray-400 text-sm">Your trusted phone & laptop repair specialist in Alor Gajah, Melaka.</p>
                    </div>
                    <div>
                        <h4 class="font-semibold mb-4">Quick Links</h4>
                        <div class="space-y-2 text-sm">
                            <a href="#home" class="block text-gray-400 hover:text-red-500">Home</a>
                            <a href="#services" class="block text-gray-400 hover:text-red-500">Services</a>
                            <a href="#repair-request" class="block text-gray-400 hover:text-red-500">Request Repair</a>
                            <a href="#check-status" class="block text-gray-400 hover:text-red-500">Check Status</a>
                        </div>
                    </div>
                    <div>
                        <h4 class="font-semibold mb-4">Services</h4>
                        <div class="space-y-2 text-sm">
                            <div class="text-gray-400">Phone Repair</div>
                            <div class="text-gray-400">Laptop Repair</div>
                            <div class="text-gray-400">Screen Replacement</div>
                            <div class="text-gray-400">Data Recovery</div>
                        </div>
                    <div>
                        <h4 class="font-semibold mb-4">Business Hours</h4>
                        <div class="space-y-2 text-sm text-gray-400">
                            <div>Monday - Sunday</div>
                            <div class="text-red-500 font-semibold">9:00 AM - 9:00 PM</div>
                            <div class="pt-2">Emergency Service Available</div>
                        </div>
                    </div>
                </div>
                <div class="border-t border-gray-800 pt-8 text-center text-sm text-gray-500">
                    <p>&copy; 2024 SS DYNAMIC TELECOMMUNICATION (MA0200450). All Rights Reserved.</p>
                    <p class="mt-2">NO 2, BANGUNAN TERMINAL BAS KOMPLEKS AG SENTRAL 78000 ALOR GAJAH MELAKA</p>
                </div>
            </div>
        </footer>

        <!-- WhatsApp Floating Button -->
        <a href="https://wa.me/601151453147" target="_blank" class="floating-whatsapp">
            <div class="bg-green-500 hover:bg-green-600 w-14 h-14 rounded-full flex items-center justify-center shadow-2xl transition">
                <i class="fab fa-whatsapp text-white text-2xl"></i>
            </div>
        </a>
    </div>

    <!-- Admin Login Modal -->
    <div id="loginModal" class="hidden fixed inset-0 bg-black/90 backdrop-blur-sm z-[100] flex items-center justify-center p-4">
        <div class="glass rounded-2xl p-8 max-w-md w-full">
            <div class="flex justify-between items-center mb-6">
                <h2 class="text-2xl font-bold">Admin Login</h2>
                <button onclick="closeLoginModal()" class="text-gray-400 hover:text-white">
                    <i class="fas fa-times text-xl"></i>
                </button>
            </div>
            <form onsubmit="adminLogin(event)">
                <div class="mb-4">
                    <label class="block text-sm font-medium mb-2">Username</label>
                    <input type="text" id="adminUser" required 
                           class="w-full px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white">
                </div>
                <div class="mb-6">
                    <label class="block text-sm font-medium mb-2">Password</label>
                    <input type="password" id="adminPass" required 
                           class="w-full px-4 py-3 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white">
                </div>
                <button type="submit" class="btn-primary w-full py-3 rounded-lg font-semibold">
                    <i class="fas fa-sign-in-alt mr-2"></i>Login
                </button>
                <p class="text-xs text-gray-500 mt-4 text-center">Demo: Username: SS DYNAMIC | Password: #01234567890</p>
            </form>
        </div>
    </div>

    <!-- Admin Panel View -->
    <div id="adminView" class="admin-view">
        <nav class="glass fixed w-full top-0 z-50">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex justify-between items-center h-16">
                    <div class="flex items-center gap-3">
                        <div class="bg-gradient-to-br from-red-600 to-red-800 p-2 rounded-lg">
                            <i class="fas fa-cog text-white text-xl"></i>
                        </div>
                        <div>
                            <h1 class="text-lg sm:text-xl font-bold text-white">SS DYNAMIC FIX</h1>
                            <p class="text-xs text-gray-400">Admin Dashboard</p>
                        </div>
                    <button onclick="adminLogout()" class="btn-primary px-4 py-2 rounded-lg text-sm font-semibold">
                        <i class="fas fa-sign-out-alt mr-2"></i>Logout
                    </button>
                </div>
            </div>
        </nav>

        <div class="pt-20 min-h-screen bg-gray-900">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
                <div class="mb-8">
                    <h2 class="text-3xl font-bold mb-2">Repair Management Dashboard</h2>
                    <p class="text-gray-400">Manage all repair requests and update status</p>
                </div>

                <!-- Stats -->
                <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-8">
                    <div class="glass rounded-xl p-6">
                        <div class="text-3xl font-bold text-red-500" id="totalRepairs">0</div>
                        <div class="text-sm text-gray-400">Total Repairs</div>
                    </div>
                    <div class="glass rounded-xl p-6">
                        <div class="text-3xl font-bold text-yellow-500" id="activeRepairs">0</div>
                        <div class="text-sm text-gray-400">In Progress</div>
                    </div>
                    <div class="glass rounded-xl p-6">
                        <div class="text-3xl font-bold text-green-500" id="completedRepairs">0</div>
                        <div class="text-sm text-gray-400">Completed</div>
                    </div>
                    <div class="glass rounded-xl p-6">
                        <div class="text-3xl font-bold text-blue-500" id="urgentRepairs">0</div>
                        <div class="text-sm text-gray-400">Urgent Cases</div>
                    </div>
                </div>

                <!-- Repairs Table -->
                <div class="glass rounded-2xl p-6">
                    <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4 mb-6">
                        <h3 class="text-xl font-bold">All Repair Requests</h3>
                        <input type="text" id="adminSearch" onkeyup="filterRepairs()" placeholder="Search tickets..." 
                               class="px-4 py-2 bg-black/50 border border-gray-700 rounded-lg focus:border-red-500 focus:outline-none text-white w-full sm:w-auto">
                    </div>
                    
                    <div class="overflow-x-auto">
                        <table class="w-full">
                            <thead>
                                <tr class="border-b border-gray-700 text-left text-sm text-gray-400">
                                    <th class="pb-3 px-2">Ticket #</th>
                                    <th class="pb-3 px-2">Customer</th>
                                    <th class="pb-3 px-2">Device</th>
                                    <th class="pb-3 px-2 hidden md:table-cell">Issue</th>
                                    <th class="pb-3 px-2">Status</th>
                                    <th class="pb-3 px-2">Actions</th>
                                </tr>
                            </thead>
                            <tbody id="repairsTable">
                                <tr>
                                    <td colspan="6" class="text-center py-8 text-gray-500">No repair requests yet</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Success Toast -->
    <div id="toast" class="hidden fixed top-20 right-4 glass px-6 py-4 rounded-lg z-[200] max-w-md">
        <div class="flex items-start gap-3">
            <i class="fas fa-check-circle text-green-500 text-xl mt-1"></i>
            <div>
                <div class="font-semibold" id="toastTitle">Success!</div>
                <div class="text-sm text-gray-400" id="toastMessage"></div>
            </div>
        </div>
    </div>

<script>
    // Initialize localStorage
    if (!localStorage.getItem('ss_repairs')) {
        localStorage.setItem('ss_repairs', JSON.stringify([]));
    }

    // Mobile menu toggle
    document.getElementById('mobileMenuBtn').addEventListener('click', () => {
        document.getElementById('mobileMenu').classList.toggle('hidden');
    });

    // Close mobile menu on link click
    document.querySelectorAll('#mobileMenu a').forEach(link => {
        link.addEventListener('click', () => {
            document.getElementById('mobileMenu').classList.add('hidden');
        });
    });

    // Generate ticket number
    function generateTicket() {
        return 'SSD-' + Date.now().toString().slice(-6);
    }

    // Submit repair request
    function submitRepair(e) {
        e.preventDefault();
        const form = e.target;
        const formData = new FormData(form);
        
        const repair = {
            ticket: generateTicket(),
            name: formData.get('name'),
            phone: formData.get('phone'),
            email: formData.get('email'),
            deviceType: formData.get('deviceType'),
            model: formData.get('model'),
            issueType: formData.get('issueType'),
            description: formData.get('description'),
            urgent: formData.get('urgent') === 'on',
            status: 'Received',
            date: new Date().toISOString(),
            notes: []
        };

        const repairs = JSON.parse(localStorage.getItem('ss_repairs'));
        repairs.unshift(repair);
        localStorage.setItem('ss_repairs', JSON.stringify(repairs));
        
        showToast('Request Submitted!', `Your ticket number is ${repair.ticket}. We will contact you soon.`);
        form.reset();
        
        setTimeout(() => {
            document.getElementById('ticketSearch').value = repair.ticket;
            document.getElementById('check-status').scrollIntoView({ behavior: 'smooth' });
            checkStatus();
        }, 2000);
    }

    // Check status
    function checkStatus() {
        const ticketNum = document.getElementById('ticketSearch').value.trim().toUpperCase();
        const resultDiv = document.getElementById('statusResult');
        
        if (!ticketNum) {
            resultDiv.innerHTML = '<div class="text-red-500 text-center py-4">Please enter a ticket number</div>';
            resultDiv.classList.remove('hidden');
            return;
        }

        const repairs = JSON.parse(localStorage.getItem('ss_repairs'));
        const repair = repairs.find(r => r.ticket === ticketNum);

        if (repair) {
            const statusClass = `status-${repair.status.toLowerCase().replace(' ', '')}`;
            const urgentBadge = repair.urgent ? '<span class="bg-red-600 text-white text-xs px-3 py-1 rounded-full ml-2">URGENT</span>' : '';
            
            resultDiv.innerHTML = `
                <div class="glass rounded-xl p-6 space-y-4">
                    <div class="flex justify-between items-start">
                        <div>
                            <div class="text-sm text-gray-400 mb-1">Ticket Number</div>
                            <div class="text-2xl font-bold text-red-500">${repair.ticket}</div>
                        </div>
                        <div class="text-right">
                            <span class="status-badge ${statusClass}">${repair.status}</span>${urgentBadge}
                        </div>
                    </div>
                    <div class="grid sm:grid-cols-2 gap-4 pt-4 border-t border-gray-700">
                        <div>
                            <div class="text-sm text-gray-400 mb-1">Customer</div>
                            <div class="font-semibold">${repair.name}</div>
                        </div>
                        <div>
                            <div class="text-sm text-gray-400 mb-1">Device</div>
                            <div class="font-semibold">${repair.deviceType} - ${repair.model}</div>
                        </div>
                        <div>
                            <div class="text-sm text-gray-400 mb-1">Issue</div>
                            <div class="font-semibold">${repair.issueType}</div>
                        </div>
                        <div>
                            <div class="text-sm text-gray-400 mb-1">Submitted</div>
                            <div class="font-semibold">${new Date(repair.date).toLocaleDateString()}</div>
                        </div>
                    </div>
                    ${repair.notes.length > 0 ? `
                        <div class="pt-4 border-t border-gray-700">
                            <div class="text-sm text-gray-400 mb-2">Updates</div>
                            <div class="space-y-2">
                                ${repair.notes.map(note => `
                                    <div class="text-sm bg-black/30 p-3 rounded-lg">
                                        <div class="text-gray-500 text-xs mb-1">${new Date(note.date).toLocaleString()}</div>
                                        <div>${note.text}</div>
                                    </div>
                                `).join('')}
                            </div>
                        </div>
                    ` : ''}
                </div>
            `;
        } else {
            resultDiv.innerHTML = `
                <div class="text-center py-8">
                    <i class="fas fa-exclamation-circle text-yellow-500 text-4xl mb-4"></i>
                    <div class="text-lg font-semibold mb-2">Ticket Not Found</div>
                    <div class="text-gray-400 text-sm">Please check your ticket number and try again</div>
                </div>
            `;
        }
        resultDiv.classList.remove('hidden');
    }

    // Admin login
    function showAdminLogin() {
        document.getElementById('loginModal').classList.remove('hidden');
    }

    function closeLoginModal() {
        document.getElementById('loginModal').classList.add('hidden');
    }

    function adminLogin(e) {
        e.preventDefault();
        const user = document.getElementById('adminUser').value;
        const pass = document.getElementById('adminPass').value;

        if (user === 'SS DYNAMIC' && pass === '#01234567890') {
            document.getElementById('mainView').classList.remove('active');
            document.getElementById('adminView').classList.add('active');
            document.getElementById('loginModal').classList.add('hidden');
            loadAdminDashboard();
            window.scrollTo(0, 0);
        } else {
            showToast('Login Failed', 'Invalid username or password', true);
        }
    }

    function adminLogout() {
        document.getElementById('adminView').classList.remove('active');
        document.getElementById('mainView').classList.add('active');
        document.getElementById('adminUser').value = '';
        document.getElementById('adminPass').value = '';
        window.scrollTo(0, 0);
    }

    // Load admin dashboard
    function loadAdminDashboard() {
        const repairs = JSON.parse(localStorage.getItem('ss_repairs'));
        
        // Update stats
        document.getElementById('totalRepairs').textContent = repairs.length;
        document.getElementById('activeRepairs').textContent = repairs.filter(r => !['Completed', 'Collected'].includes(r.status)).length;
        document.getElementById('completedRepairs').textContent = repairs.filter(r => r.status === 'Completed').length;
        document.getElementById('urgentRepairs').textContent = repairs.filter(r => r.urgent).length;

        renderRepairsTable(repairs);
    }

    // Render repairs table
    function renderRepairsTable(repairs) {
        const tbody = document.getElementById('repairsTable');
        
        if (repairs.length === 0) {
            tbody.innerHTML = '<tr><td colspan="6" class="text-center py-8 text-gray-500">No repair requests yet</td></tr>';
            return;
        }

        tbody.innerHTML = repairs.map(repair => {
            const statusClass = `status-${repair.status.toLowerCase().replace(' ', '')}`;
            const urgentIcon = repair.urgent ? '<i class="fas fa-exclamation-triangle text-red-500 ml-2"></i>' : '';
            
            return `
                <tr class="border-b border-gray-800 hover:bg-gray-800/50">
                    <td class="py-4 px-2">
                        <div class="font-mono text-red-500 font-semibold">${repair.ticket}</div>
                        <div class="text-xs text-gray-500">${new Date(repair.date).toLocaleDateString()}</div>
                    </td>
                    <td class="py-4 px-2">
                        <div class="font-semibold">${repair.name}${urgentIcon}</div>
                        <div class="text-xs text-gray-400">${repair.phone}</div>
                    </td>
                    <td class="py-4 px-2">
                        <div class="font-semibold">${repair.deviceType}</div>
                        <div class="text-xs text-gray-400">${repair.model}</div>
                    </td>
                    <td class="py-4 px-2 hidden md:table-cell">
                        <div class="text-sm">${repair.issueType}</div>
                    </td>
                    <td class="py-4 px-2">
                        <span class="status-badge ${statusClass}">${repair.status}</span>
                    </td>
                    <td class="py-4 px-2">
                        <button onclick="updateStatus('${repair.ticket}')" class="bg-red-600 hover:bg-red-700 px-3 py-1 rounded text-xs font-semibold">
                            Update
                        </button>
                    </td>
                </tr>
            `;
        }).join('');
    }

    // Update status
    function updateStatus(ticket) {
        const repairs = JSON.parse(localStorage.getItem('ss_repairs'));
        const repair = repairs.find(r => r.ticket === ticket);
        
        if (!repair) return;

        const statuses = ['Received', 'Diagnosing', 'Repairing', 'Testing', 'Completed', 'Collected'];
        const currentIndex = statuses.indexOf(repair.status);
        
        const newStatus = prompt(`Update status for ${ticket}\n\nCurrent: ${repair.status}\n\nOptions:\n${statuses.map((s, i) => `${i + 1}. ${s}`).join('\n')}\n\nEnter number (1-6):`);
        
        if (newStatus && newStatus >= 1 && newStatus <= 6) {
            repair.status = statuses[newStatus - 1];
            const note = prompt('Add a note for customer (optional):');
            if (note) {
                repair.notes.unshift({ date: new Date().toISOString(), text: note });
            }
            localStorage.setItem('ss_repairs', JSON.stringify(repairs));
            loadAdminDashboard();
            showToast('Status Updated', `Ticket ${ticket} is now ${repair.status}`);
        }
    }

    // Filter repairs
    function filterRepairs() {
        const search = document.getElementById('adminSearch').value.toLowerCase();
        const repairs = JSON.parse(localStorage.getItem('ss_repairs'));
        const filtered = repairs.filter(r => 
            r.ticket.toLowerCase().includes(search) ||
            r.name.toLowerCase().includes(search) ||
            r.model.toLowerCase().includes(search) ||
            r.phone.includes(search)
        );
        renderRepairsTable(filtered);
    }

    // Toast notification
    function showToast(title, message, isError = false) {
        const toast = document.getElementById('toast');
        document.getElementById('toastTitle').textContent = title;
        document.getElementById('toastMessage').textContent = message;
        
        if (isError) {
            toast.querySelector('i').className = 'fas fa-exclamation-circle text-red-500 text-xl mt-1';
        } else {
            toast.querySelector('i').className = 'fas fa-check-circle text-green-500 text-xl mt-1';
        }
        
        toast.classList.remove('hidden');
        setTimeout(() => toast.classList.add('hidden'), 4000);
    }

    // Smooth scroll for nav links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({ behavior: 'smooth', block: 'start' });
            }
        });
    });
</script>
<script>(function(){document.addEventListener("click",function(e){var a=e.target.closest("[data-product-id]");if(!a)return;e.preventDefault();var pid=a.getAttribute("data-product-id");if(pid)parent.postMessage({type:"ecto-artifact-link-click",productId:pid},"*")})})();</script>
</body>
