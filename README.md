<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>LAUREL & CREST | Institutional Real Estate Investment & Deal Arena</title>
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Playfair+Display:ital,wght@0,500;0,600;0,700;1,400&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  
  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>
  <!-- Chart.js for financial projections -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <!-- Canvas Confetti for voting feedback -->
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['"Plus Jakarta Sans"', 'sans-serif'],
            serif: ['"Playfair Display"', 'serif'],
            mono: ['"JetBrains Mono"', 'monospace'],
          },
          colors: {
            laurel: {
              50: '#f2f7f4',
              100: '#e1ede6',
              200: '#c5dcd0',
              300: '#9ec2b1',
              400: '#72a28d',
              500: '#518570',
              600: '#3d6a59',
              700: '#325548',
              800: '#2a453b',
              900: '#1b2f28',
              950: '#0f1c18',
            },
            sand: {
              50: '#fbfaf8',
              100: '#f5f3ee',
              200: '#eae5db',
              300: '#dbd3c2',
              400: '#c7bca5',
              500: '#b4a488',
            },
            champagne: '#D8C39D',
          },
          boxShadow: {
            'subtle': '0 4px 20px -2px rgba(27, 47, 40, 0.05)',
            'card': '0 12px 36px -4px rgba(27, 47, 40, 0.08), 0 4px 12px -2px rgba(0,0,0,0.03)',
            'float': '0 20px 40px -8px rgba(15, 28, 24, 0.16)',
            'pill': '0 8px 24px -3px rgba(0, 0, 0, 0.07)',
          }
        }
      }
    }
  </script>

  <style>
    /* Custom Scrollbars */
    ::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    ::-webkit-scrollbar-track {
      background: #f1f3f2;
    }
    ::-webkit-scrollbar-thumb {
      background: #c5dcd0;
      border-radius: 999px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #72a28d;
    }

    .glass-panel {
      background: rgba(255, 255, 255, 0.88);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
    }
    
    .glass-dark {
      background: rgba(27, 47, 40, 0.92);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
    }

    .smooth-transition {
      transition: all 0.3s cubic-bezier(0.16, 1, 0.3, 1);
    }

    .badge-shimmer {
      background: linear-gradient(90deg, rgba(255,255,255,0) 0%, rgba(255,255,255,0.4) 50%, rgba(255,255,255,0) 100%);
      background-size: 200% 100%;
      animation: shimmer 3s infinite;
    }

    @keyframes shimmer {
      0% { background-position: -200% 0; }
      100% { background-position: 200% 0; }
    }
  </style>
</head>

<body class="bg-[#F6F8F7] text-gray-800 font-sans antialiased selection:bg-laurel-200 selection:text-laurel-950">

  <!-- Top Announcement Bar -->
  <div class="bg-laurel-950 text-sand-200 text-xs py-2 px-4 border-b border-laurel-800">
    <div class="max-w-7xl mx-auto flex justify-between items-center">
      <div class="flex items-center space-x-2">
        <span class="inline-flex items-center px-2 py-0.5 rounded-full text-[10px] font-semibold bg-laurel-700 text-emerald-300">
          Q3 DEAL COMPARISON OPEN
        </span>
        <span class="hidden sm:inline text-sand-300">Institutional Syndicate Arena: Benchmark & vote on Austin Multifamily vs Savannah Logistics</span>
      </div>
      <div class="flex items-center space-x-4 text-sand-400 font-mono text-[11px]">
        <span>AUM: <strong class="text-white">$1.84B</strong></span>
        <span class="hidden md:inline">|</span>
        <span class="hidden md:inline">Avg Realized IRR: <strong class="text-emerald-400">19.4%</strong></span>
        <a href="#investor-portal" class="text-sand-200 hover:text-white underline font-sans ml-2">LP Portal &rarr;</a>
      </div>
    </div>
  </div>

  <!-- Main Navigation -->
  <header class="sticky top-0 z-40 glass-panel border-b border-gray-200/80 shadow-xs">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
      
      <!-- Brand Logo with Laurel Icon -->
      <a href="#" class="flex items-center gap-3 group">
        <div class="w-11 h-11 rounded-2xl bg-laurel-900 text-sand-200 flex items-center justify-center shadow-md group-hover:scale-105 transition-transform duration-300 border border-laurel-700/50">
          <!-- Laurel Wreath SVG -->
          <svg class="w-7 h-7 text-champagne" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2C12 2 10.5 5 8.5 7C6.5 9 3 9.5 3 9.5C3 9.5 4.5 12 6.5 13C8.5 14 10 12.5 10 12.5C10 12.5 8 15 6 17C4 19 2 20 2 20C2 20 5 20.5 8 19C11 17.5 11.5 15 11.5 15C11.5 15 11.8 18 12 22C12.2 18 12.5 15 12.5 15C12.5 15 13 17.5 16 19C19 20.5 22 20 22 20C22 20 20 19 18 17C16 15 14 12.5 14 12.5C14 12.5 15.5 14 17.5 13C19.5 12 21 9.5 21 9.5C21 9.5 17.5 9 15.5 7C13.5 5 12 2 12 2Z" opacity="0.95"/>
          </svg>
        </div>
        <div>
          <span class="font-serif text-xl tracking-tight font-bold text-laurel-950 block leading-tight">LAUREL & CREST</span>
          <span class="text-[10px] tracking-[0.2em] font-semibold text-laurel-600 uppercase block">Private Real Estate Capital</span>
        </div>
      </a>

      <!-- Desktop Navigation Menu -->
      <nav class="hidden md:flex items-center space-x-1 lg:space-x-2">
        <a href="#arena-section" class="px-3.5 py-2 text-sm font-semibold text-laurel-950 bg-laurel-100/60 rounded-xl hover:bg-laurel-100 transition-colors flex items-center gap-1.5">
          <i data-lucide="scale" class="w-4 h-4 text-laurel-700"></i>
          Deal Arena (A/B)
        </a>
        <a href="#portfolio-section" class="px-3.5 py-2 text-sm font-medium text-gray-600 hover:text-laurel-900 rounded-xl hover:bg-gray-100/70 transition-colors">
          Portfolio
        </a>
        <a href="#calculator-section" class="px-3.5 py-2 text-sm font-medium text-gray-600 hover:text-laurel-900 rounded-xl hover:bg-gray-100/70 transition-colors">
          Yield Modeler
        </a>
        <a href="#thesis-section" class="px-3.5 py-2 text-sm font-medium text-gray-600 hover:text-laurel-900 rounded-xl hover:bg-gray-100/70 transition-colors">
          Investment Thesis
        </a>
        <a href="#advisory-chat" class="px-3.5 py-2 text-sm font-medium text-gray-600 hover:text-laurel-900 rounded-xl hover:bg-gray-100/70 transition-colors flex items-center gap-1">
          <i data-lucide="sparkles" class="w-3.5 h-3.5 text-laurel-600"></i>
          AI Deal Analyst
        </a>
      </nav>

      <!-- Action CTA Buttons -->
      <div class="hidden sm:flex items-center space-x-3">
        <button onclick="openOverviewModal()" class="px-4 py-2 text-xs font-semibold text-laurel-900 bg-white border border-gray-300 rounded-xl shadow-xs hover:border-laurel-500 hover:bg-gray-50 transition-all flex items-center gap-2">
          <i data-lucide="layout-grid" class="w-3.5 h-3.5"></i>
          Executive Summary
        </button>
        <a href="#arena-section" class="px-5 py-2.5 text-xs font-semibold uppercase tracking-wider text-white bg-laurel-900 rounded-xl shadow-md hover:bg-laurel-800 active:scale-95 transition-all">
          Vote on Deals
        </a>
      </div>

      <!-- Mobile Menu Button -->
      <button id="mobileMenuBtn" class="md:hidden p-2 rounded-xl text-gray-700 hover:bg-gray-100" aria-label="Toggle Navigation">
        <i data-lucide="menu" class="w-6 h-6"></i>
      </button>
    </div>

    <!-- Mobile Dropdown -->
    <div id="mobileMenu" class="hidden md:hidden border-t border-gray-200 bg-white px-4 pt-3 pb-6 space-y-3">
      <a href="#arena-section" class="block px-3 py-2 text-base font-semibold text-laurel-900 bg-laurel-50 rounded-lg">Deal Arena (A/B Vote)</a>
      <a href="#portfolio-section" class="block px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 rounded-lg">Active Portfolio</a>
      <a href="#calculator-section" class="block px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 rounded-lg">Yield Modeler</a>
      <a href="#thesis-section" class="block px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 rounded-lg">Investment Thesis</a>
      <a href="#advisory-chat" class="block px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 rounded-lg">AI Deal Intelligence</a>
      <div class="pt-2 flex flex-col gap-2">
        <button onclick="openOverviewModal()" class="w-full py-2.5 text-center text-sm font-semibold border border-gray-300 rounded-xl">View Overview</button>
        <a href="#arena-section" class="w-full py-2.5 text-center text-sm font-semibold text-white bg-laurel-900 rounded-xl">Participate in Deal Arena</a>
      </div>
    </div>
  </header>

  <!-- Hero Section with Live Stats -->
  <section class="relative pt-12 pb-8 overflow-hidden">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
      <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-white border border-laurel-200 shadow-xs mb-6">
        <div class="w-2 h-2 rounded-full bg-emerald-500 animate-ping"></div>
        <span class="text-xs font-semibold text-laurel-900">Institutional Syndicate Stage • Series IV Selection</span>
      </div>

      <h1 class="font-serif text-3xl sm:text-5xl lg:text-6xl font-bold text-laurel-950 tracking-tight max-w-4xl mx-auto leading-[1.15]">
        Evaluate, Compare & Co-Invest in <span class="italic font-normal text-laurel-700 underline decoration-champagne underline-offset-8">Generational Assets</span>
      </h1>
      
      <p class="mt-5 text-base sm:text-lg text-gray-600 max-w-2xl mx-auto font-normal leading-relaxed">
        Use our interactive Deal Arena below to benchmark two prime acquisition targets. Review underwriting artifacts, run sensitivity analyses, and cast your allocation vote.
      </p>

      <!-- Key Trust Metrics -->
      <div class="mt-8 grid grid-cols-2 sm:grid-cols-4 gap-3 sm:gap-4 max-w-4xl mx-auto">
        <div class="bg-white p-4 rounded-2xl border border-gray-200/80 shadow-xs">
          <div class="text-2xl sm:text-3xl font-bold text-laurel-950 font-serif">19.4%</div>
          <div class="text-xs text-gray-500 font-medium mt-1">Historic Target IRR</div>
        </div>
        <div class="bg-white p-4 rounded-2xl border border-gray-200/80 shadow-xs">
          <div class="text-2xl sm:text-3xl font-bold text-laurel-950 font-serif">$1.84B</div>
          <div class="text-xs text-gray-500 font-medium mt-1">Total Assets Transacted</div>
        </div>
        <div class="bg-white p-4 rounded-2xl border border-gray-200/80 shadow-xs">
          <div class="text-2xl sm:text-3xl font-bold text-laurel-950 font-serif">96.8%</div>
          <div class="text-xs text-gray-500 font-medium mt-1">Average Portfolio Occupancy</div>
        </div>
        <div class="bg-white p-4 rounded-2xl border border-gray-200/80 shadow-xs">
          <div class="text-2xl sm:text-3xl font-bold text-laurel-950 font-serif">2.25x</div>
          <div class="text-xs text-gray-500 font-medium mt-1">Target Equity Multiple</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ========================================================================= -->
  <!-- MAIN ARENA COMPARISON SECTION (MATCHING & EXTENDING THE IMAGE UI DESIGN) -->
  <!-- ========================================================================= -->
  <section id="arena-section" class="py-10 relative">
    <div class="max-w-5xl mx-auto px-4 sm:px-6">

      <!-- Arena Main Card Container with Outer Styled Border -->
      <div class="relative bg-white rounded-3xl p-4 sm:p-7 border border-laurel-300 shadow-card transition-all duration-300">
        
        <!-- Floating Overview Widget in Top Right (As in Reference Image) -->
        <button onclick="openOverviewModal()" class="absolute -top-3 sm:-top-4 right-4 sm:right-8 z-20 glass-dark text-white px-4 py-2.5 rounded-2xl shadow-float flex items-center gap-2.5 border border-laurel-700/60 hover:bg-laurel-900 transition-transform active:scale-95 group">
          <i data-lucide="menu" class="w-4 h-4 text-emerald-400 group-hover:rotate-90 transition-transform"></i>
          <span class="text-xs font-semibold tracking-wide">Overview</span>
          <span class="w-2 h-2 rounded-full bg-emerald-400"></span>
        </button>

        <!-- Laurel Header & Top Option Pill Selector (Option A / Option B) -->
        <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 pb-6 border-b border-gray-100">
          
          <div class="flex items-center gap-3">
            <!-- Laurel Wreath Badge -->
            <div class="w-9 h-9 rounded-xl bg-laurel-100 flex items-center justify-center text-laurel-900">
              <svg class="w-5 h-5 text-laurel-900" viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 2C12 2 10.5 5 8.5 7C6.5 9 3 9.5 3 9.5C3 9.5 4.5 12 6.5 13C8.5 14 10 12.5 10 12.5C10 12.5 8 15 6 17C4 19 2 20 2 20C2 20 5 20.5 8 19C11 17.5 11.5 15 11.5 15C11.5 15 11.8 18 12 22C12.2 18 12.5 15 12.5 15C12.5 15 13 17.5 16 19C19 20.5 22 20 22 20C22 20 20 19 18 17C16 15 14 12.5 14 12.5C14 12.5 15.5 14 17.5 13C19.5 12 21 9.5 21 9.5C21 9.5 17.5 9 15.5 7C13.5 5 12 2 12 2Z"/>
              </svg>
            </div>
            <div>
              <h2 class="text-lg font-bold text-laurel-950">Syndicate Decision Matrix</h2>
              <p class="text-xs text-gray-500">Compare asset underwritings, pro-forma models, and cash flow stability</p>
            </div>
          </div>

          <!-- Option A / Option B Pill Switcher (From Reference Image) -->
          <div class="bg-gray-100/90 p-1 rounded-2xl flex items-center self-start sm:self-auto border border-gray-200/60 shadow-inner">
            <button id="tabOptionA" onclick="switchOptionTab('A')" class="px-5 py-2 rounded-xl text-xs font-bold transition-all duration-200 bg-white text-laurel-950 shadow-xs">
              Option A
            </button>
            <button id="tabOptionB" onclick="switchOptionTab('B')" class="px-5 py-2 rounded-xl text-xs font-semibold text-gray-500 hover:text-gray-900 transition-all duration-200">
              Option B
            </button>
            <button id="tabCompareBoth" onclick="switchOptionTab('BOTH')" class="px-3 py-2 rounded-xl text-xs font-semibold text-laurel-700 hover:text-laurel-950 transition-all duration-200 hidden md:block">
              Split View
            </button>
          </div>
        </div>

        <!-- Dynamic Option Content Area -->
        <div class="mt-6">

          <!-- OPTION A CARD CONTAINER -->
          <div id="contentOptionA" class="space-y-6">
            
            <!-- Asset Artifact Header -->
            <div class="flex flex-wrap items-center justify-between gap-2 text-xs">
              <div class="flex items-center gap-2 text-laurel-700 font-semibold bg-laurel-50 px-3 py-1.5 rounded-lg border border-laurel-200">
                <i data-lucide="layers" class="w-4 h-4"></i>
                <span>Option A Deal Memo & Underwriting Artifact</span>
              </div>
              <span class="text-gray-400 font-mono text-[11px]">Asset ID: #LC-AUSTIN-MF74 • Class A+ Multifamily</span>
            </div>

            <!-- Asset Spotlight Title & Pitch -->
            <div>
              <div class="flex items-center gap-2 mb-1">
                <span class="px-2 py-0.5 rounded text-[10px] font-bold bg-amber-100 text-amber-900 uppercase tracking-wider">Sunbelt Growth Core</span>
                <span class="text-xs text-gray-400 font-mono">Austin, TX Innovation Corridor</span>
              </div>
              <h3 class="text-2xl font-serif font-bold text-laurel-950">The Travis Ridge Luxury Residences & Retail</h3>
              <p class="mt-2 text-sm text-gray-600 leading-relaxed">
                Now let's review the finalized debt term sheet and lease-up momentum for <span class="font-semibold text-laurel-900">Travis Ridge</span>. Featuring 340 institutional multifamily units with 18,000 sq.ft ground retail, locked with an in-place agency loan at 5.4% fixed.
              </p>
            </div>

            <!-- Pro-forma Metrics Grid -->
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 bg-gray-50/90 p-4 rounded-2xl border border-gray-200">
              <div class="p-3 bg-white rounded-xl shadow-2xs border border-gray-100">
                <span class="text-[11px] font-medium text-gray-500 uppercase tracking-wider block">Target IRR (Net)</span>
                <span class="text-xl font-bold text-emerald-700 font-serif">20.2%</span>
                <span class="text-[10px] text-gray-400 block mt-0.5">5-Year Hold</span>
              </div>
              <div class="p-3 bg-white rounded-xl shadow-2xs border border-gray-100">
                <span class="text-[11px] font-medium text-gray-500 uppercase tracking-wider block">Entry Cap Rate</span>
                <span class="text-xl font-bold text-laurel-950 font-serif">6.75%</span>
                <span class="text-[10px] text-emerald-600 block mt-0.5">+85bps to submarket</span>
              </div>
              <div class="p-3 bg-white rounded-xl shadow-2xs border border-gray-100">
                <span class="text-[11px] font-medium text-gray-500 uppercase tracking-wider block">Avg Cash-on-Cash</span>
                <span class="text-xl font-bold text-laurel-950 font-serif">8.4%</span>
                <span class="text-[10px] text-gray-400 block mt-0.5">Paid Quarterly</span>
              </div>
              <div class="p-3 bg-white rounded-xl shadow-2xs border border-gray-100">
                <span class="text-[11px] font-medium text-gray-500 uppercase tracking-wider block">Equity Multiple</span>
                <span class="text-xl font-bold text-laurel-900 font-serif">2.34x</span>
                <span class="text-[10px] text-gray-400 block mt-0.5">Base Underwriting</span>
              </div>
            </div>

            <!-- Visual Asset Card & Highlights -->
            <div class="grid md:grid-cols-12 gap-5 items-center">
              <div class="md:col-span-5 relative rounded-2xl overflow-hidden shadow-md group h-56">
                <img src="https://images.unsplash.com/photo-1545324418-cc1a3fa10c00?auto=format&fit=crop&w=800&q=80" alt="Austin Multifamily Asset" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent"></div>
                <div class="absolute bottom-3 left-3 text-white">
                  <p class="text-xs font-semibold">Phase II Pre-Leasing: 89%</p>
                  <p class="text-[11px] text-gray-300">Target Closing: Nov 15, 2024</p>
                </div>
              </div>
              
              <div class="md:col-span-7 space-y-3">
                <h4 class="text-xs font-bold text-laurel-900 uppercase tracking-wider">Key Investment Highlights:</h4>
                <ul class="space-y-2 text-xs text-gray-600">
                  <li class="flex items-start gap-2">
                    <i data-lucide="check-circle-2" class="w-4 h-4 text-emerald-600 shrink-0 mt-0.5"></i>
                    <span><strong>100% Bonus Depreciation Qualified:</strong> Optimized cost segregation study yields ~64% first-year passive tax shield.</span>
                  </li>
                  <li class="flex items-start gap-2">
                    <i data-lucide="check-circle-2" class="w-4 h-4 text-emerald-600 shrink-0 mt-0.5"></i>
                    <span><strong>Employment Catalyst:</strong> 4 miles from upcoming $1.2B semiconductor campus expansion with 4,500 direct engineering jobs.</span>
                  </li>
                  <li class="flex items-start gap-2">
                    <i data-lucide="check-circle-2" class="w-4 h-4 text-emerald-600 shrink-0 mt-0.5"></i>
                    <span><strong>Downside Debt Protection:</strong> 10-year interest-only bridge term through Fannie Mae DUS lender.</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <!-- OPTION B CARD CONTAINER -->
          <div id="contentOptionB" class="space-y-6 hidden">
            
            <!-- Asset Artifact Header -->
            <div class="flex flex-wrap items-center justify-between gap-2 text-xs">
              <div class="flex items-center gap-2 text-laurel-700 font-semibold bg-laurel-50 px-3 py-1.5 rounded-lg border border-laurel-200">
                <i data-lucide="layers" class="w-4 h-4"></i>
                <span>Option B Deal Memo & Underwriting Artifact</span>
              </div>
              <span class="text-gray-400 font-mono text-[11px]">Asset ID: #LC-SAV-LOG92 • Class A Port Logistics</span>
            </div>

            <!-- Asset Spotlight Title & Pitch -->
            <div>
              <div class="flex items-center gap-2 mb-1">
                <span class="px-2 py-0.5 rounded text-[10px] font-bold bg-blue-100 text-blue-900 uppercase tracking-wider">Industrial NNN Logistics</span>
                <span class="text-xs text-gray-400 font-mono">Savannah Port Hub, GA</span>
              </div>
              <h3 class="text-2xl font-serif font-bold text-laurel-950">Atlantic Intermodal Logistics Center (520k SF)</h3>
              <p class="mt-2 text-sm text-gray-600 leading-relaxed">
                Examine the long-term stable yield profile of <span class="font-semibold text-laurel-900">Atlantic Intermodal Hub</span>. 100% triple-net (NNN) leased to an investment-grade Fortune 100 logistics tenant with 3.5% contractual annual rent escalators and 12.5 years WALT.
              </p>
            </div>

            <!-- Pro-forma Metrics Grid -->
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 bg-gray-50/90 p-4 rounded-2xl border border-gray-200">
              <div class="p-3 bg-white rounded-xl shadow-2xs border border-gray-100">
                <span class="text-[11px] font-medium text-gray-500 uppercase tracking-wider block">Target IRR (Net)</span>
                <span class="text-xl font-bold text-emerald-700 font-serif">17.8%</span>
                <span class="text-[10px] text-gray-400 block mt-0.5">7-Year Hold</span>
              </div>
              <div class="p-3 bg-white rounded-xl shadow-2xs border border-gray-100">
                <span class="text-[11px] font-medium text-gray-500 uppercase tracking-wider block">In-Place Cap Rate</span>
                <span class="text-xl font-bold text-laurel-950 font-serif">7.40%</span>
                <span class="text-[10px] text-emerald-600 block mt-0.5">Strong Day-1 Yield</span>
              </div>
              <div class="p-3 bg-white rounded-xl shadow-2xs border border-gray-100">
                <span class="text-[11px] font-medium text-gray-500 uppercase tracking-wider block">Avg Cash-on-Cash</span>
                <span class="text-xl font-bold text-laurel-950 font-serif">9.8%</span>
                <span class="text-[10px] text-emerald-600 block mt-0.5">Bond-like Cash Flow</span>
              </div>
              <div class="p-3 bg-white rounded-xl shadow-2xs border border-gray-100">
                <span class="text-[11px] font-medium text-gray-500 uppercase tracking-wider block">Equity Multiple</span>
                <span class="text-xl font-bold text-laurel-900 font-serif">2.18x</span>
                <span class="text-[10px] text-gray-400 block mt-0.5">Zero Capex Drag</span>
              </div>
            </div>

            <!-- Visual Asset Card & Highlights -->
            <div class="grid md:grid-cols-12 gap-5 items-center">
              <div class="md:col-span-5 relative rounded-2xl overflow-hidden shadow-md group h-56">
                <img src="https://images.unsplash.com/photo-1586528116311-ad8dd3c8310d?auto=format&fit=crop&w=800&q=80" alt="Industrial Logistics Asset" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                <div class="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent"></div>
                <div class="absolute bottom-3 left-3 text-white">
                  <p class="text-xs font-semibold">100% Leased • 12.5 Yr WALT</p>
                  <p class="text-[11px] text-gray-300">Tenant Credit: AA- Rated</p>
                </div>
              </div>
              
              <div class="md:col-span-7 space-y-3">
                <h4 class="text-xs font-bold text-laurel-900 uppercase tracking-wider">Key Investment Highlights:</h4>
                <ul class="space-y-2 text-xs text-gray-600">
                  <li class="flex items-start gap-2">
                    <i data-lucide="check-circle-2" class="w-4 h-4 text-emerald-600 shrink-0 mt-0.5"></i>
                    <span><strong>Absolute NNN Lease Structure:</strong> Zero landlord operating expense responsibilities; tenant covers taxes, insurance & structural maintenance.</span>
                  </li>
                  <li class="flex items-start gap-2">
                    <i data-lucide="check-circle-2" class="w-4 h-4 text-emerald-600 shrink-0 mt-0.5"></i>
                    <span><strong>Critical Port Proximity:</strong> Located 6.2 miles from the Garden City Terminal (fastest growing container gateway in the US).</span>
                  </li>
                  <li class="flex items-start gap-2">
                    <i data-lucide="check-circle-2" class="w-4 h-4 text-emerald-600 shrink-0 mt-0.5"></i>
                    <span><strong>Built-In Inflation Hedge:</strong> 3.50% annual compounding rental rate bumps locked in master agreement.</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <!-- SPLIT / DUAL VIEW CONTAINER (On desktop) -->
          <div id="contentOptionBoth" class="hidden">
            <div class="grid md:grid-cols-2 gap-6">
              <div class="p-4 rounded-2xl border border-laurel-300 bg-laurel-50/30">
                <div class="flex justify-between items-center mb-3">
                  <span class="text-xs font-bold text-laurel-900">OPTION A: Multifamily</span>
                  <span class="text-xs font-mono font-bold text-emerald-700">20.2% IRR</span>
                </div>
                <h4 class="font-serif font-bold text-base mb-1">Travis Ridge Luxury Residences</h4>
                <p class="text-xs text-gray-600 mb-3">High capital appreciation potential with value-add unit finishes in Austin, TX.</p>
                <div class="text-[11px] font-mono space-y-1 text-gray-700 bg-white p-3 rounded-xl border border-gray-200">
                  <div class="flex justify-between"><span>Entry Cap:</span><strong>6.75%</strong></div>
                  <div class="flex justify-between"><span>Target Hold:</span><strong>5 Years</strong></div>
                  <div class="flex justify-between"><span>Equity Multiple:</span><strong>2.34x</strong></div>
                </div>
              </div>

              <div class="p-4 rounded-2xl border border-blue-200 bg-blue-50/30">
                <div class="flex justify-between items-center mb-3">
                  <span class="text-xs font-bold text-blue-900">OPTION B: Port Logistics</span>
                  <span class="text-xs font-mono font-bold text-emerald-700">17.8% IRR</span>
                </div>
                <h4 class="font-serif font-bold text-base mb-1">Atlantic Intermodal Center</h4>
                <p class="text-xs text-gray-600 mb-3">High recurring quarterly cash flow with long-term Fortune 100 tenant in Savannah, GA.</p>
                <div class="text-[11px] font-mono space-y-1 text-gray-700 bg-white p-3 rounded-xl border border-gray-200">
                  <div class="flex justify-between"><span>Day-1 Cap:</span><strong>7.40%</strong></div>
                  <div class="flex justify-between"><span>WALT:</span><strong>12.5 Years</strong></div>
                  <div class="flex justify-between"><span>Cash-on-Cash:</span><strong>9.8%</strong></div>
                </div>
              </div>
            </div>
          </div>

        </div>

        <!-- ================================================================= -->
        <!-- VOTING PILL INTERACTION (EXACT LAYOUT FROM REFERENCE IMAGE) -->
        <!-- ================================================================= -->
        <div class="mt-8 pt-4 border-t border-gray-100">
          
          <!-- Outer Voting Card Box (matching image style) -->
          <div class="relative bg-white/95 rounded-3xl p-3 sm:p-5 border border-gray-200 shadow-md">
            
            <!-- Voting Action Bar -->
            <div class="flex flex-col sm:flex-row items-center justify-between gap-3">
              
              <!-- Option A is Better Button -->
              <button id="voteBtnA" onclick="castVote('A')" class="w-full sm:flex-1 py-3 px-5 rounded-2xl border border-gray-200 bg-white hover:bg-laurel-50 hover:border-laurel-400 font-semibold text-sm text-gray-800 transition-all shadow-xs flex items-center justify-center gap-2 group active:scale-98">
                <span class="w-6 h-6 rounded-full bg-gray-100 text-gray-700 flex items-center justify-center text-xs font-bold group-hover:bg-laurel-800 group-hover:text-white transition-colors">A</span>
                <span>A is better</span>
              </button>

              <!-- Central Laurel Wreath Emblem (matching image) -->
              <div class="shrink-0 p-2 text-laurel-900 hover:rotate-12 transition-transform cursor-pointer" title="Laurel Syndicate Governance">
                <svg class="w-8 h-8 text-laurel-900" viewBox="0 0 24 24" fill="currentColor">
                  <path d="M12 2C12 2 10.5 5 8.5 7C6.5 9 3 9.5 3 9.5C3 9.5 4.5 12 6.5 13C8.5 14 10 12.5 10 12.5C10 12.5 8 15 6 17C4 19 2 20 2 20C2 20 5 20.5 8 19C11 17.5 11.5 15 11.5 15C11.5 15 11.8 18 12 22C12.2 18 12.5 15 12.5 15C12.5 15 13 17.5 16 19C19 20.5 22 20 22 20C22 20 20 19 18 17C16 15 14 12.5 14 12.5C14 12.5 15.5 14 17.5 13C19.5 12 21 9.5 21 9.5C21 9.5 17.5 9 15.5 7C13.5 5 12 2 12 2Z"/>
                </svg>
              </div>

              <!-- Option B is Better Button -->
              <button id="voteBtnB" onclick="castVote('B')" class="w-full sm:flex-1 py-3 px-5 rounded-2xl border border-gray-200 bg-white hover:bg-laurel-50 hover:border-laurel-400 font-semibold text-sm text-gray-800 transition-all shadow-xs flex items-center justify-center gap-2 group active:scale-98">
                <span>B is better</span>
                <span class="w-6 h-6 rounded-full bg-gray-100 text-gray-700 flex items-center justify-center text-xs font-bold group-hover:bg-laurel-800 group-hover:text-white transition-colors">B</span>
              </button>
            </div>

            <!-- Live Syndicate Voting Progress Bar (Appears upon vote) -->
            <div id="votingResults" class="mt-4 pt-3 border-t border-gray-100 hidden">
              <div class="flex justify-between text-xs font-semibold mb-1">
                <span class="text-laurel-800" id="resultLabelA">Option A (Multifamily): 58%</span>
                <span class="text-blue-800" id="resultLabelB">Option B (Logistics): 42%</span>
              </div>
              <div class="w-full h-2.5 bg-gray-100 rounded-full overflow-hidden flex">
                <div id="barOptionA" class="bg-laurel-700 h-full transition-all duration-700" style="width: 58%"></div>
                <div id="barOptionB" class="bg-blue-600 h-full transition-all duration-700" style="width: 42%"></div>
              </div>
              <p class="text-[11px] text-gray-400 mt-2 text-center" id="voteAckText">
                ✓ Your investor preference has been registered in Syndicate Batch #449.
              </p>
            </div>

            <!-- Interactive AI Chat / Vote Prompt Input Box (Inspired by Reference Image Bottom UI) -->
            <div class="mt-4 bg-gray-50/80 rounded-2xl p-3 border border-gray-200/80 focus-within:border-laurel-600 focus-within:bg-white transition-all">
              <div class="flex items-center gap-3">
                <div class="flex items-center gap-1 text-gray-400">
                  <button type="button" onclick="triggerFileUpload()" class="p-1.5 hover:text-laurel-800 hover:bg-gray-200/60 rounded-lg transition-colors" title="Attach Underwriting File">
                    <i data-lucide="paperclip" class="w-4 h-4"></i>
                  </button>
                  <button type="button" onclick="triggerCloudSync()" class="p-1.5 hover:text-laurel-800 hover:bg-gray-200/60 rounded-lg transition-colors" title="Sync with RealPage / CoStar">
                    <i data-lucide="cloud-upload" class="w-4 h-4"></i>
                  </button>
                </div>

                <input id="aiChatInput" type="text" placeholder="Vote on the design above first, or ask AI Co-Pilot to simulate tax shields..." class="w-full bg-transparent text-xs sm:text-sm text-gray-800 placeholder-gray-400 focus:outline-hidden py-1" onkeydown="handleChatKeyPress(event)" />

                <button id="aiSubmitBtn" onclick="submitChatPrompt()" class="w-8 h-8 rounded-xl bg-laurel-900 text-white flex items-center justify-center shrink-0 hover:bg-laurel-800 transition-all shadow-xs" title="Send Query">
                  <i data-lucide="arrow-up" class="w-4 h-4"></i>
                </button>
              </div>

              <!-- Quick AI Query Chips -->
              <div class="mt-2.5 pt-2 border-t border-gray-200/60 flex flex-wrap gap-1.5 text-[11px]">
                <span class="text-gray-400 py-0.5">Quick Prompts:</span>
                <button onclick="fillChatPrompt('Compare 5-year post-tax distributions for $250k investment')" class="px-2 py-0.5 rounded-md bg-white border border-gray-200 text-gray-600 hover:text-laurel-800 hover:border-laurel-300 transition-all">
                  💰 Post-Tax Distributions
                </button>
                <button onclick="fillChatPrompt('Stress test Option A if interest rates rise +100bps at refinancing')" class="px-2 py-0.5 rounded-md bg-white border border-gray-200 text-gray-600 hover:text-laurel-800 hover:border-laurel-300 transition-all">
                  📈 Refi Stress Test
                </button>
                <button onclick="fillChatPrompt('Generate comparative sensitivity matrix on entry cap rates')" class="px-2 py-0.5 rounded-md bg-white border border-gray-200 text-gray-600 hover:text-laurel-800 hover:border-laurel-300 transition-all">
                  📊 Sensitivity Matrix
                </button>
              </div>
            </div>

          </div>
        </div>

        <!-- Bottom Tab Navigation Bar (Inspired by Reference Image "Chat / Preview / designarena.ai" bar) -->
        <div class="mt-6 pt-4 border-t border-gray-100 flex flex-col sm:flex-row items-center justify-between gap-4">
          
          <!-- Chat vs Preview Switcher -->
          <div class="flex items-center gap-6">
            <button onclick="switchMode('CHAT')" id="modeChatBtn" class="flex flex-col items-center text-xs font-semibold text-laurel-800 group">
              <i data-lucide="message-square" class="w-5 h-5 mb-0.5 text-laurel-800"></i>
              <span>Deal Chat</span>
            </button>
            <button onclick="switchMode('PREVIEW')" id="modePreviewBtn" class="flex flex-col items-center text-xs font-medium text-gray-400 hover:text-gray-700 group">
              <i data-lucide="eye" class="w-5 h-5 mb-0.5 text-gray-400 group-hover:text-gray-700"></i>
              <span>Pro-Forma Preview</span>
            </button>
          </div>

          <!-- URL Pill Simulator (Inspired by reference bottom bar) -->
          <div class="flex items-center gap-2 bg-gray-100/90 py-1.5 px-3.5 rounded-full border border-gray-200 text-xs text-gray-600 font-mono shadow-inner">
            <button onclick="navigateHistory('back')" class="hover:text-black"><i data-lucide="chevron-left" class="w-3.5 h-3.5"></i></button>
            <i data-lucide="shield-check" class="w-3.5 h-3.5 text-laurel-700"></i>
            <span class="font-sans font-medium text-gray-800 text-[11px]">syndicate.laurelcrest.com/arena/q3-options</span>
            <button onclick="refreshData()" class="hover:text-black ml-1" title="Reload Underwriting"><i data-lucide="rotate-cw" class="w-3.5 h-3.5"></i></button>
          </div>

          <!-- Syndicate Actions Dropdown Button -->
          <div class="flex items-center gap-2">
            <button onclick="openDueDiligenceModal()" class="px-3.5 py-1.5 bg-laurel-100 text-laurel-900 rounded-xl text-xs font-bold hover:bg-laurel-200 transition-all flex items-center gap-1.5">
              <i data-lucide="download" class="w-3.5 h-3.5"></i>
              Download OM (PDF)
            </button>
            <button onclick="openInvestorModal()" class="w-8 h-8 rounded-xl bg-gray-100 flex items-center justify-center text-gray-600 hover:bg-gray-200" title="More syndicate actions">
              <i data-lucide="more-horizontal" class="w-4 h-4"></i>
            </button>
          </div>

        </div>

      </div>
    </div>
  </section>

  <!-- ========================================================================= -->
  <!-- AI CHAT & SPREADSHEET ARTIFACT OUTPUT SECTION -->
  <!-- ========================================================================= -->
  <section id="advisory-chat" class="py-12 bg-sand-50 border-t border-b border-gray-200/80">
    <div class="max-w-5xl mx-auto px-4 sm:px-6">
      <div class="flex items-center justify-between mb-6">
        <div>
          <div class="flex items-center gap-2">
            <span class="w-2.5 h-2.5 rounded-full bg-emerald-500"></span>
            <h3 class="text-xl font-serif font-bold text-laurel-950">AI Syndicate Deal Analyst</h3>
          </div>
          <p class="text-xs text-gray-500 mt-0.5">Real-time LLM trained on 15+ years of institutional commercial real estate transactions</p>
        </div>
        <button onclick="clearChatLog()" class="text-xs text-gray-400 hover:text-gray-700 flex items-center gap-1">
          <i data-lucide="trash-2" class="w-3 h-3"></i> Clear Log
        </button>
      </div>

      <!-- Interactive Chat Feed -->
      <div id="chatFeed" class="space-y-4">
        
        <!-- System Welcome Message -->
        <div class="flex items-start gap-3 bg-white p-4 sm:p-5 rounded-2xl border border-gray-200 shadow-xs">
          <div class="w-8 h-8 rounded-xl bg-laurel-900 text-champagne flex items-center justify-center shrink-0">
            <i data-lucide="bot" class="w-4 h-4"></i>
          </div>
          <div class="space-y-2 text-xs sm:text-sm text-gray-700 flex-1">
            <div class="flex items-center justify-between">
              <span class="font-bold text-laurel-900">Laurel Capital Intelligence Engine</span>
              <span class="text-[10px] text-gray-400 font-mono">Live Pro-Forma v4.2</span>
            </div>
            <p>
              Welcome. Both <span class="font-semibold text-laurel-800">Option A (Austin Multifamily)</span> and <span class="font-semibold text-blue-800">Option B (Savannah Industrial Logistics)</span> have cleared investment committee review.
            </p>
            <p class="text-gray-500 text-xs">
              💡 <em>Pro tip: Vote above to register your allocation preference, or click any quick prompt to model IRR sensitivity, debt covenants, or waterfall splits.</em>
            </p>
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- ========================================================================= -->
  <!-- REAL-TIME YIELD & INVESTMENT CALCULATOR -->
  <!-- ========================================================================= -->
  <section id="calculator-section" class="py-16 bg-white">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="text-center max-w-2xl mx-auto mb-12">
        <span class="text-xs font-bold uppercase tracking-wider text-laurel-700 bg-laurel-50 px-3 py-1 rounded-full border border-laurel-200">Interactive Modeler</span>
        <h2 class="text-3xl font-serif font-bold text-laurel-950 mt-3">Simulate Your Co-Investment Yields</h2>
        <p class="text-sm text-gray-500 mt-2">Adjust capital allocation and target strategy to see projected returns and cumulative cash distributions.</p>
      </div>

      <div class="grid lg:grid-cols-12 gap-8 items-start">
        
        <!-- Controls Column -->
        <div class="lg:col-span-5 bg-[#F9FBFA] p-6 rounded-3xl border border-gray-200 space-y-6">
          
          <!-- Capital Slider -->
          <div>
            <div class="flex justify-between items-center mb-2">
              <label class="text-xs font-bold text-laurel-950 uppercase tracking-wide">Investment Capital</label>
              <span id="capitalDisplay" class="text-lg font-serif font-bold text-laurel-800">$250,000</span>
            </div>
            <input id="capitalSlider" type="range" min="50000" max="2000000" step="25000" value="250000" class="w-full accent-laurel-800 cursor-pointer h-2 bg-gray-200 rounded-lg" oninput="updateCalculator()">
            <div class="flex justify-between text-[10px] text-gray-400 mt-1 font-mono">
              <span>$50,000</span>
              <span>$1,000,000</span>
              <span>$2,000,000+</span>
            </div>
          </div>

          <!-- Strategy Selection -->
          <div>
            <label class="text-xs font-bold text-laurel-950 uppercase tracking-wide block mb-2">Target Strategy Asset</label>
            <div class="grid grid-cols-2 gap-2">
              <button id="calcStrategyA" onclick="setCalcStrategy('A')" class="p-3 text-left rounded-xl border-2 border-laurel-700 bg-white transition-all">
                <span class="block text-xs font-bold text-laurel-900">Option A</span>
                <span class="block text-[11px] text-gray-500">Austin Multifamily (20.2% IRR)</span>
              </button>
              <button id="calcStrategyB" onclick="setCalcStrategy('B')" class="p-3 text-left rounded-xl border border-gray-200 bg-white hover:border-gray-300 transition-all">
                <span class="block text-xs font-bold text-gray-800">Option B</span>
                <span class="block text-[11px] text-gray-500">Savannah Logistics (17.8% IRR)</span>
              </button>
            </div>
          </div>

          <!-- Hold Period -->
          <div>
            <div class="flex justify-between items-center mb-2">
              <label class="text-xs font-bold text-laurel-950 uppercase tracking-wide">Holding Period</label>
              <span id="holdDisplay" class="text-sm font-bold text-laurel-900">5 Years</span>
            </div>
            <div class="flex gap-2">
              <button onclick="setHoldPeriod(3)" class="hold-btn flex-1 py-2 rounded-xl text-xs font-semibold bg-white border border-gray-200 hover:border-laurel-400">3 Yrs</button>
              <button onclick="setHoldPeriod(5)" class="hold-btn active flex-1 py-2 rounded-xl text-xs font-semibold bg-laurel-900 text-white border border-laurel-900">5 Yrs</button>
              <button onclick="setHoldPeriod(7)" class="hold-btn flex-1 py-2 rounded-xl text-xs font-semibold bg-white border border-gray-200 hover:border-laurel-400">7 Yrs</button>
              <button onclick="setHoldPeriod(10)" class="hold-btn flex-1 py-2 rounded-xl text-xs font-semibold bg-white border border-gray-200 hover:border-laurel-400">10 Yrs</button>
            </div>
          </div>

          <!-- Reinvestment Toggle -->
          <div class="pt-4 border-t border-gray-200 flex items-center justify-between">
            <div>
              <span class="text-xs font-bold text-laurel-950 block">Quarterly Cash Flow Compounding</span>
              <span class="text-[11px] text-gray-400">Auto-reinvest quarterly dividends into REIT Fund</span>
            </div>
            <label class="relative inline-flex items-center cursor-pointer">
              <input type="checkbox" id="reinvestToggle" onchange="updateCalculator()" class="sr-only peer">
              <div class="w-11 h-6 bg-gray-200 peer-focus:outline-hidden rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-laurel-800"></div>
            </label>
          </div>

        </div>

        <!-- Results & Chart Display Column -->
        <div class="lg:col-span-7 bg-white p-6 rounded-3xl border border-gray-200 shadow-card flex flex-col justify-between">
          
          <div>
            <div class="grid grid-cols-3 gap-3 pb-6 border-b border-gray-100">
              <div>
                <span class="text-[11px] text-gray-400 font-medium uppercase block">Projected Total Return</span>
                <span id="projTotalReturn" class="text-2xl sm:text-3xl font-serif font-bold text-laurel-950">$585,000</span>
                <span id="projMultiple" class="text-[10px] text-emerald-600 font-bold block mt-0.5">2.34x Equity Multiple</span>
              </div>
              <div>
                <span class="text-[11px] text-gray-400 font-medium uppercase block">Total Net Profit</span>
                <span id="projNetProfit" class="text-2xl sm:text-3xl font-serif font-bold text-emerald-700">+$335,000</span>
                <span class="text-[10px] text-gray-400 block mt-0.5">Post Fees</span>
              </div>
              <div>
                <span class="text-[11px] text-gray-400 font-medium uppercase block">Quarterly Distribution</span>
                <span id="projQuarterly" class="text-2xl sm:text-3xl font-serif font-bold text-laurel-900">$5,250</span>
                <span class="text-[10px] text-gray-400 block mt-0.5">Avg Annual Yield</span>
              </div>
            </div>

            <!-- Chart Canvas -->
            <div class="mt-6 relative h-60 w-full">
              <canvas id="returnsChart"></canvas>
            </div>
          </div>

          <div class="mt-6 pt-4 border-t border-gray-100 flex flex-col sm:flex-row items-center justify-between gap-3">
            <span class="text-xs text-gray-400">Past performance does not guarantee future results. SEC Reg D 506(c).</span>
            <button onclick="openInvestorModal()" class="px-5 py-2.5 rounded-xl bg-laurel-900 hover:bg-laurel-800 text-white text-xs font-bold transition-all shadow-md">
              Request Full Pro-Forma Deck &rarr;
            </button>
          </div>

        </div>

      </div>
    </div>
  </section>

  <!-- ========================================================================= -->
  <!-- PORTFOLIO SECTION -->
  <!-- ========================================================================= -->
  <section id="portfolio-section" class="py-16 bg-[#F6F8F7]">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="flex flex-col md:flex-row md:items-end justify-between mb-10">
        <div>
          <span class="text-xs font-bold uppercase tracking-wider text-laurel-700 bg-laurel-100 px-3 py-1 rounded-full">Track Record</span>
          <h2 class="text-3xl sm:text-4xl font-serif font-bold text-laurel-950 mt-2">Historic Asset Portfolio</h2>
          <p class="text-sm text-gray-500 mt-1">Institutional real estate assets under management across major high-growth US submarkets.</p>
        </div>
        <div class="mt-4 md:mt-0 flex gap-2">
          <button onclick="filterPortfolio('ALL')" class="port-filter active px-3.5 py-1.5 rounded-xl text-xs font-semibold bg-laurel-900 text-white">All Assets</button>
          <button onclick="filterPortfolio('MULTIFAMILY')" class="port-filter px-3.5 py-1.5 rounded-xl text-xs font-semibold bg-white text-gray-600 hover:bg-gray-100">Multifamily</button>
          <button onclick="filterPortfolio('INDUSTRIAL')" class="port-filter px-3.5 py-1.5 rounded-xl text-xs font-semibold bg-white text-gray-600 hover:bg-gray-100">Industrial Logistics</button>
          <button onclick="filterPortfolio('MEDICAL')" class="port-filter px-3.5 py-1.5 rounded-xl text-xs font-semibold bg-white text-gray-600 hover:bg-gray-100">Medical Office</button>
        </div>
      </div>

      <!-- Grid of Properties -->
      <div id="portfolioGrid" class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
        
        <!-- Asset Card 1 -->
        <div class="portfolio-item MULTIFAMILY bg-white rounded-3xl overflow-hidden border border-gray-200/80 shadow-subtle hover:shadow-card transition-all duration-300 group">
          <div class="relative h-52 overflow-hidden">
            <img src="https://images.unsplash.com/photo-1545324418-cc1a3fa10c00?auto=format&fit=crop&w=700&q=80" alt="The Travis Ridge" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
            <span class="absolute top-3 left-3 bg-laurel-950/80 backdrop-blur-md text-white text-[11px] font-semibold px-2.5 py-1 rounded-lg">Austin, TX</span>
            <span class="absolute top-3 right-3 bg-amber-500 text-white text-[10px] font-bold px-2 py-1 rounded-md uppercase">Option A Arena</span>
          </div>
          <div class="p-5">
            <div class="text-xs font-mono text-laurel-700 font-bold mb-1">MULTIFAMILY • 340 UNITS</div>
            <h4 class="text-lg font-serif font-bold text-laurel-950">The Travis Ridge Residences</h4>
            <div class="mt-4 pt-4 border-t border-gray-100 grid grid-cols-3 gap-2 text-center">
              <div>
                <span class="text-[10px] text-gray-400 block uppercase">Target IRR</span>
                <span class="text-sm font-bold text-emerald-700 font-serif">20.2%</span>
              </div>
              <div>
                <span class="text-[10px] text-gray-400 block uppercase">Cap Rate</span>
                <span class="text-sm font-bold text-gray-800 font-serif">6.75%</span>
              </div>
              <div>
                <span class="text-[10px] text-gray-400 block uppercase">Min Ticket</span>
                <span class="text-sm font-bold text-gray-800 font-serif">$50k</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Asset Card 2 -->
        <div class="portfolio-item INDUSTRIAL bg-white rounded-3xl overflow-hidden border border-gray-200/80 shadow-subtle hover:shadow-card transition-all duration-300 group">
          <div class="relative h-52 overflow-hidden">
            <img src="https://images.unsplash.com/photo-1586528116311-ad8dd3c8310d?auto=format&fit=crop&w=700&q=80" alt="Atlantic Logistics" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
            <span class="absolute top-3 left-3 bg-laurel-950/80 backdrop-blur-md text-white text-[11px] font-semibold px-2.5 py-1 rounded-lg">Savannah, GA</span>
            <span class="absolute top-3 right-3 bg-blue-600 text-white text-[10px] font-bold px-2 py-1 rounded-md uppercase">Option B Arena</span>
          </div>
          <div class="p-5">
            <div class="text-xs font-mono text-blue-700 font-bold mb-1">INDUSTRIAL LOGISTICS • 520K SF</div>
            <h4 class="text-lg font-serif font-bold text-laurel-950">Atlantic Intermodal Center</h4>
            <div class="mt-4 pt-4 border-t border-gray-100 grid grid-cols-3 gap-2 text-center">
              <div>
                <span class="text-[10px] text-gray-400 block uppercase">Target IRR</span>
                <span class="text-sm font-bold text-emerald-700 font-serif">17.8%</span>
              </div>
              <div>
                <span class="text-[10px] text-gray-400 block uppercase">Day-1 Cap</span>
                <span class="text-sm font-bold text-gray-800 font-serif">7.40%</span>
              </div>
              <div>
                <span class="text-[10px] text-gray-400 block uppercase">Min Ticket</span>
                <span class="text-sm font-bold text-gray-800 font-serif">$50k</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Asset Card 3 -->
        <div class="portfolio-item MEDICAL bg-white rounded-3xl overflow-hidden border border-gray-200/80 shadow-subtle hover:shadow-card transition-all duration-300 group">
          <div class="relative h-52 overflow-hidden">
            <img src="https://images.unsplash.com/photo-1519494026892-80bbd2d6fd0d?auto=format&fit=crop&w=700&q=80" alt="Bayfront Life Science" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
            <span class="absolute top-3 left-3 bg-laurel-950/80 backdrop-blur-md text-white text-[11px] font-semibold px-2.5 py-1 rounded-lg">Raleigh, NC</span>
            <span class="absolute top-3 right-3 bg-emerald-700 text-white text-[10px] font-bold px-2 py-1 rounded-md uppercase">Fully Funded</span>
          </div>
          <div class="p-5">
            <div class="text-xs font-mono text-emerald-800 font-bold mb-1">LIFE SCIENCES & MEDICAL • 180K SF</div>
            <h4 class="text-lg font-serif font-bold text-laurel-950">Research Triangle BioCenter</h4>
            <div class="mt-4 pt-4 border-t border-gray-100 grid grid-cols-3 gap-2 text-center">
              <div>
                <span class="text-[10px] text-gray-400 block uppercase">Realized IRR</span>
                <span class="text-sm font-bold text-emerald-700 font-serif">21.8%</span>
              </div>
              <div>
                <span class="text-[10px] text-gray-400 block uppercase">Occupancy</span>
                <span class="text-sm font-bold text-gray-800 font-serif">100%</span>
              </div>
              <div>
                <span class="text-[10px] text-gray-400 block uppercase">Hold Period</span>
                <span class="text-sm font-bold text-gray-800 font-serif">4.2 Yrs</span>
              </div>
            </div>
          </div>
        </div>

      </div>

    </div>
  </section>

  <!-- ========================================================================= -->
  <!-- THESIS & INSTITUTIONAL GOVERNANCE -->
  <!-- ========================================================================= -->
  <section id="thesis-section" class="py-16 bg-laurel-950 text-sand-100">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="grid lg:grid-cols-12 gap-10 items-center">
        
        <div class="lg:col-span-5 space-y-5">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-laurel-900 border border-laurel-700 text-champagne text-xs font-semibold">
            <svg class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C12 2 10.5 5 8.5 7C6.5 9 3 9.5 3 9.5C3 9.5 4.5 12 6.5 13C8.5 14 10 12.5 10 12.5C10 12.5 8 15 6 17C4 19 2 20 2 20C2 20 5 20.5 8 19C11 17.5 11.5 15 11.5 15C11.5 15 11.8 18 12 22C12.2 18 12.5 15 12.5 15C12.5 15 13 17.5 16 19C19 20.5 22 20 22 20C22 20 20 19 18 17C16 15 14 12.5 14 12.5C14 12.5 15.5 14 17.5 13C19.5 12 21 9.5 21 9.5C21 9.5 17.5 9 15.5 7C13.5 5 12 2 12 2Z"/></svg>
            Laurel Crest Underwriting Framework
          </div>
          <h2 class="text-3xl sm:text-4xl font-serif font-bold text-white tracking-tight">
            Asymmetric Upside with Strict Capital Preservation
          </h2>
          <p class="text-sand-300 text-sm leading-relaxed">
            We originate direct off-market transactions in resilient supply-constrained growth corridors. By combining proprietary data scrapers with veteran field execution, we ensure every deal in the Arena is stress-tested against severe macro shocks.
          </p>
          <div class="space-y-3 pt-2">
            <div class="flex items-center gap-3 text-sm">
              <i data-lucide="check" class="w-5 h-5 text-emerald-400 shrink-0"></i>
              <span>GP co-invests minimum 10% cash in every syndicate</span>
            </div>
            <div class="flex items-center gap-3 text-sm">
              <i data-lucide="check" class="w-5 h-5 text-emerald-400 shrink-0"></i>
              <span>Quarterly audited financial statements by Big 4 firms</span>
            </div>
            <div class="flex items-center gap-3 text-sm">
              <i data-lucide="check" class="w-5 h-5 text-emerald-400 shrink-0"></i>
              <span>Preferred return hurdle of 8.0% prior to GP promote</span>
            </div>
          </div>
        </div>

        <div class="lg:col-span-7 grid sm:grid-cols-2 gap-4">
          <div class="p-6 rounded-2xl bg-laurel-900/60 border border-laurel-800 space-y-3">
            <div class="w-10 h-10 rounded-xl bg-laurel-800 flex items-center justify-center text-champagne">
              <i data-lucide="shield-alert" class="w-5 h-5"></i>
            </div>
            <h4 class="font-bold text-white text-base">Defensive Debt Structures</h4>
            <p class="text-xs text-sand-300 leading-relaxed">Low-leverage (under 60% LTV) with fixed-rate or long-dated interest rate caps to immunize against yield curve volatility.</p>
          </div>

          <div class="p-6 rounded-2xl bg-laurel-900/60 border border-laurel-800 space-y-3">
            <div class="w-10 h-10 rounded-xl bg-laurel-800 flex items-center justify-center text-champagne">
              <i data-lucide="calculator" class="w-5 h-5"></i>
            </div>
            <h4 class="font-bold text-white text-base">Cost Segregation & Tax Alpha</h4>
            <p class="text-xs text-sand-300 leading-relaxed">Engineered accelerated depreciation schedules delivering substantial tax offsets for high-earning LPs.</p>
          </div>

          <div class="p-6 rounded-2xl bg-laurel-900/60 border border-laurel-800 space-y-3">
            <div class="w-10 h-10 rounded-xl bg-laurel-800 flex items-center justify-center text-champagne">
              <i data-lucide="trending-up" class="w-5 h-5"></i>
            </div>
            <h4 class="font-bold text-white text-base">In-House Asset Management</h4>
            <p class="text-xs text-sand-300 leading-relaxed">No third-party operator friction. Our dedicated operational teams oversee capital expenditures and tenant relations.</p>
          </div>

          <div class="p-6 rounded-2xl bg-laurel-900/60 border border-laurel-800 space-y-3">
            <div class="w-10 h-10 rounded-xl bg-laurel-800 flex items-center justify-center text-champagne">
              <i data-lucide="lock" class="w-5 h-5"></i>
            </div>
            <h4 class="font-bold text-white text-base">Transparent Voting Arena</h4>
            <p class="text-xs text-sand-300 leading-relaxed">LP Advisory Committee votes on refinancing dates, exit timelines, and 1031 roll-over syndications.</p>
          </div>
        </div>

      </div>

    </div>
  </section>

  <!-- ========================================================================= -->
  <!-- OVERVIEW SLIDE-OVER MODAL (TRIGGERED BY THE TOP-RIGHT OVERVIEW PILL) -->
  <!-- ========================================================================= -->
  <div id="overviewModal" class="fixed inset-0 z-50 hidden bg-black/60 backdrop-blur-xs flex items-center justify-center p-4">
    <div class="bg-white rounded-3xl max-w-2xl w-full max-h-[90vh] overflow-y-auto p-6 sm:p-8 shadow-2xl border border-gray-200 animate-in fade-in zoom-in duration-200">
      
      <div class="flex justify-between items-center pb-4 border-b border-gray-200">
        <div class="flex items-center gap-2">
          <div class="w-8 h-8 rounded-lg bg-laurel-900 text-champagne flex items-center justify-center">
            <i data-lucide="layout-grid" class="w-4 h-4"></i>
          </div>
          <div>
            <h3 class="font-serif font-bold text-xl text-laurel-950">Executive Syndicate Overview</h3>
            <p class="text-xs text-gray-500">Batch #449 Syndicate Summary & Voting Covenants</p>
          </div>
        </div>
        <button onclick="closeOverviewModal()" class="w-8 h-8 rounded-full bg-gray-100 flex items-center justify-center text-gray-600 hover:bg-gray-200">
          <i data-lucide="x" class="w-4 h-4"></i>
        </button>
      </div>

      <div class="mt-6 space-y-6 text-sm text-gray-600">
        <div>
          <h4 class="font-bold text-laurel-950 text-xs uppercase tracking-wider mb-2">Current Batch Objective</h4>
          <p class="text-xs leading-relaxed">
            The Investment Committee is allocating $35,000,000 in Series IV syndicate equity. Registered investors vote between Option A (Growth Focused) and Option B (Yield Focused).
          </p>
        </div>

        <div class="grid sm:grid-cols-2 gap-4">
          <div class="p-4 rounded-xl bg-laurel-50 border border-laurel-200">
            <span class="text-xs font-bold text-laurel-900 block">Option A: Travis Ridge MF</span>
            <ul class="mt-2 text-xs space-y-1 text-gray-600">
              <li>• Location: Austin, TX</li>
              <li>• Target IRR: 20.2% Net</li>
              <li>• Equity Target: $18.5M</li>
              <li>• Profile: Value-Add Expansion</li>
            </ul>
          </div>

          <div class="p-4 rounded-xl bg-blue-50 border border-blue-200">
            <span class="text-xs font-bold text-blue-900 block">Option B: Atlantic Logistics</span>
            <ul class="mt-2 text-xs space-y-1 text-gray-600">
              <li>• Location: Savannah, GA</li>
              <li>• Target IRR: 17.8% Net</li>
              <li>• Equity Target: $16.5M</li>
              <li>• Profile: Core+ NNN High Cashflow</li>
            </ul>
          </div>
        </div>

        <div class="p-4 rounded-xl bg-gray-50 border border-gray-200 text-xs">
          <span class="font-bold text-gray-900 block mb-1">Syndicate Key Dates:</span>
          <div class="grid grid-cols-2 gap-2 text-gray-500">
            <div>• Voting Closes: <strong>October 30, 2024</strong></div>
            <div>• Capital Call: <strong>November 10, 2024</strong></div>
            <div>• Target Acquisition: <strong>December 1, 2024</strong></div>
            <div>• First Distribution: <strong>Q1 2025</strong></div>
          </div>
        </div>
      </div>

      <div class="mt-8 pt-4 border-t border-gray-100 flex justify-end gap-3">
        <button onclick="closeOverviewModal()" class="px-4 py-2 rounded-xl text-xs font-semibold text-gray-600 hover:bg-gray-100">Dismiss</button>
        <button onclick="closeOverviewModal(); document.getElementById('arena-section').scrollIntoView({behavior: 'smooth'})" class="px-5 py-2 rounded-xl text-xs font-bold bg-laurel-900 text-white hover:bg-laurel-800">
          Cast Vote Now &rarr;
        </button>
      </div>

    </div>
  </div>

  <!-- ========================================================================= -->
  <!-- INVESTOR ONBOARDING & OM DOWNLOAD MODAL -->
  <!-- ========================================================================= -->
  <div id="investorModal" class="fixed inset-0 z-50 hidden bg-black/60 backdrop-blur-xs flex items-center justify-center p-4">
    <div class="bg-white rounded-3xl max-w-lg w-full p-6 sm:p-8 shadow-2xl border border-gray-200">
      <div class="flex justify-between items-center pb-3 border-b border-gray-100">
        <div>
          <h3 class="font-serif font-bold text-xl text-laurel-950">Accredited LP Access</h3>
          <p class="text-xs text-gray-500">Download full Offering Memorandum & Private Placement Memo</p>
        </div>
        <button onclick="closeInvestorModal()" class="w-8 h-8 rounded-full bg-gray-100 flex items-center justify-center text-gray-600 hover:bg-gray-200">
          <i data-lucide="x" class="w-4 h-4"></i>
        </button>
      </div>

      <form id="leadForm" onsubmit="handleLeadSubmit(event)" class="mt-5 space-y-4 text-xs">
        <div>
          <label class="block font-semibold text-gray-700 mb-1">Full Legal Name</label>
          <input type="text" required placeholder="e.g. Eleanor Vance" class="w-full px-3.5 py-2.5 rounded-xl border border-gray-300 focus:border-laurel-700 focus:outline-hidden text-sm">
        </div>
        <div>
          <label class="block font-semibold text-gray-700 mb-1">Institutional / Personal Email</label>
          <input type="email" required placeholder="name@familyoffice.com" class="w-full px-3.5 py-2.5 rounded-xl border border-gray-300 focus:border-laurel-700 focus:outline-hidden text-sm">
        </div>
        <div>
          <label class="block font-semibold text-gray-700 mb-1">Anticipated Capital Allocation</label>
          <select class="w-full px-3.5 py-2.5 rounded-xl bo
