<!DOCTYPE html>
<html lang="uk">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Одеса Шаурмама — Sunny Beach, Bulgaria</title>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800;900&display=swap" rel="stylesheet" />

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- AOS Animations -->
  <link rel="stylesheet" href="https://unpkg.com/aos@2.3.4/dist/aos.css" />

  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest/dist/umd/lucide.js"></script>

  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            brand: '#005581',
            accent: '#D4AF37',
            dark: '#020C14',
          },
          fontFamily: {
            mont: ['Montserrat', 'sans-serif'],
          },
          animation: {
            'float-slow': 'float 6s ease-in-out infinite',
            'pulse-brand': 'pulse-brand 2s infinite',
          },
          keyframes: {
            float: {
              '0%, 100%': { transform: 'translateY(0)' },
              '50%': { transform: 'translateY(-8px)' },
            },
            'pulse-brand': {
              '0%, 100%': { boxShadow: '0 0 0 0 rgba(0, 85, 129, 0.6)' },
              '50%': { boxShadow: '0 0 0 15px rgba(0, 85, 129, 0)' },
            }
          }
        }
      }
    }
  </script>

  <style>
    *, *::before, *::after { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      background: linear-gradient(to bottom, #020813 0%, #001B2E 50%, #00101C 100%);
      color: #F8FAFC;
      font-family: 'Montserrat', sans-serif;
      overflow-x: hidden;
    }

    body::before {
      content: '';
      position: fixed; inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.8' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.025'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 0;
    }

    .marine-pattern {
      position: absolute;
      inset: 0;
      opacity: 0.03;
      background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M50 15 A5 5 0 1 0 50 25 A5 5 0 1 0 50 15 Z M48 25 L48 75 L35 75 C35 85 65 85 65 75 L52 75 L52 25 Z M35 70 L30 70 L40 85 L50 70 L45 70 A10 10 0 0 1 35 70 Z C20 50 80 50 50 15' fill='%23ffffff'/%3E%3C/svg%3E");
      background-size: 150px 150px;
      pointer-events: none;
      z-index: 0;
    }

    .nav-blur {
      background: rgba(2, 12, 20, 0.85);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border-bottom: 1px solid rgba(0, 85, 129, 0.4);
    }

    .hero-bg {
      background-image: 
        linear-gradient(to bottom, rgba(2, 12, 20, 0.4) 0%, rgba(2, 12, 20, 0.8) 60%, rgba(2, 12, 20, 1) 100%),
        url('https://images.unsplash.com/photo-1544025162-d76694265947?w=1800&auto=format&fit=crop&q=80');
      background-size: cover;
      background-position: center;
    }

    .glass {
      background: rgba(255, 255, 255, 0.03);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border: 1px solid rgba(255, 255, 255, 0.08);
      box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
    }
    
    .menu-card {
      transition: all 0.3s ease;
    }
    .menu-card:hover {
      transform: translateY(-4px);
      border-color: rgba(212, 175, 55, 0.4);
      box-shadow: 0 12px 30px rgba(0, 85, 129, 0.3);
    }
    .menu-img {
      transition: transform 0.5s ease;
    }
    .menu-card:hover .menu-img {
      transform: scale(1.1);
    }

    .marine-divider {
      background: linear-gradient(90deg, transparent, #005581 50%, transparent);
      height: 2px;
      width: 100%;
      max-width: 200px;
      margin: 0 auto;
      border-radius: 2px;
      position: relative;
    }
    .marine-divider::after {
      content: '⚓';
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: #005581;
      font-size: 1.2rem;
      background: #020813;
      padding: 0 10px;
    }

    /* Language Switcher Logic */
    html[lang="uk"] .lang-bg { display: none !important; }
    html[lang="bg"] .lang-uk { display: none !important; }

    ::-webkit-scrollbar { width: 8px; }
    ::-webkit-scrollbar-track { background: #020813; }
    ::-webkit-scrollbar-thumb { background: #005581; border-radius: 4px; }
    ::-webkit-scrollbar-thumb:hover { background: #D4AF37; }

    .lang-btn.active {
      background-color: #005581;
      color: #ffffff;
      border-color: #005581;
    }

    /* Line styling for menu item details */
    .menu-price {
      background: rgba(212, 175, 55, 0.1);
      border: 1px solid rgba(212, 175, 55, 0.3);
      color: #D4AF37;
    }
  </style>
</head>
<body class="relative">

<div class="marine-pattern"></div>

<!-- HEADER -->
<nav class="nav-blur fixed top-0 left-0 right-0 z-50 transition-all">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 h-20 flex items-center justify-between">
    <div class="hidden md:flex flex-1 items-center gap-4 text-sm font-semibold tracking-wide">
      <a href="#menu" class="text-gray-300 hover:text-accent transition-colors"><span class="lang-uk">Меню</span><span class="lang-bg">Меню</span></a>
      <a href="#reviews" class="text-gray-300 hover:text-accent transition-colors"><span class="lang-uk">Відгуки</span><span class="lang-bg">Отзиви</span></a>
      <a href="#footer" class="text-gray-300 hover:text-accent transition-colors"><span class="lang-uk">Контакти</span><span class="lang-bg">Контакти</span></a>
    </div>
    <div class="flex-1 flex justify-center">
      <a href="#hero" class="flex items-center gap-3">
        <i data-lucide="anchor" class="w-6 h-6 text-brand"></i>
        <div class="font-mont font-900 text-xl tracking-tight text-white leading-none text-center">
          ШАУРМАМА
          <div class="text-[0.6rem] tracking-[0.2em] text-accent uppercase font-medium mt-1">Sunny Beach</div>
        </div>
      </a>
    </div>
    <div class="flex-1 flex justify-end items-center gap-4">
      <div class="flex rounded-full overflow-hidden border border-white/20 text-xs font-bold bg-white/5">
        <button onclick="setLang('uk')" id="btn-uk" class="lang-btn active px-3 py-1.5 transition-colors">UA</button>
        <button onclick="setLang('bg')" id="btn-bg" class="lang-btn text-gray-400 hover:text-white px-3 py-1.5 transition-colors">BG</button>
      </div>
      <a href="tel:+359882789795" class="hidden sm:flex items-center gap-2 text-white font-bold hover:text-brand transition-colors text-sm">
        <i data-lucide="phone" class="w-4 h-4 text-brand"></i>
        +359 88 278 9795
      </a>
    </div>
  </div>
</nav>

<!-- HERO SECTION -->
<section id="hero" class="hero-bg min-h-[100vh] flex flex-col items-center justify-center text-center px-4 pt-20 relative z-10">
  <div data-aos="fade-down" data-aos-duration="1000" class="glass px-5 py-2 rounded-full inline-flex items-center gap-2 mb-6 border-accent/30 text-accent font-semibold text-xs tracking-wider uppercase shadow-[0_0_20px_rgba(212,175,55,0.2)]">
    <i data-lucide="map-pin" class="w-3.5 h-3.5"></i>
    Sunny Beach, Bulgaria
  </div>
  <h1 data-aos="zoom-in" data-aos-delay="100" class="font-mont font-black text-white text-5xl md:text-7xl lg:text-8xl leading-tight max-w-5xl drop-shadow-2xl">
    <span class="lang-uk">Легендарна Одеська<br><span class="text-brand text-stroke drop-shadow-[0_0_35px_rgba(0,85,129,0.8)]">Шаурма</span><br>в Болгарії</span>
    <span class="lang-bg">Легендарен Одески<br><span class="text-brand drop-shadow-[0_0_35px_rgba(0,85,129,0.8)]">Дюнер</span><br>в България</span>
  </h1>
  <p data-aos="fade-up" data-aos-delay="300" class="font-medium text-lg md:text-xl text-gray-300 mt-6 max-w-2xl px-4">
    <span class="lang-uk">Справжній смак з берегів Чорного моря. Лаваш, авторські соуси та свіжі інгредієнти. 🌊</span>
    <span class="lang-bg">Истинският вкус от бреговете на Черно море. Лаваш, авторски сосове и пресни съставки. 🌊</span>
  </p>
  <div data-aos="fade-up" data-aos-delay="500" class="flex flex-col sm:flex-row gap-5 mt-10">
    <a href="https://wa.me/359882789795" target="_blank" class="animate-pulse-brand bg-brand text-white font-bold text-base px-8 py-4 rounded-full flex items-center justify-center gap-3 hover:bg-[#004066] transition-all shadow-lg shadow-brand/50 border border-blue-400/30">
      <i data-lucide="shopping-bag" class="w-5 h-5 text-accent"></i>
      <span class="lang-uk">Замовити доставку</span>
      <span class="lang-bg">Поръчай доставка</span>
    </a>
    <a href="#menu" class="glass text-white font-medium text-base px-8 py-4 rounded-full flex items-center justify-center gap-3 hover:border-white/40 transition-all group">
      <span class="lang-uk">Дивитись меню</span>
      <span class="lang-bg">Виж менюто</span>
      <i data-lucide="arrow-down" class="w-4 h-4 text-gray-400 group-hover:translate-y-1 transition-transform"></i>
    </a>
  </div>
</section>

<!-- MENU SECTION -->
<section id="menu" class="py-24 px-4 relative z-10">
  <div class="max-w-6xl mx-auto">
    
    <div class="text-center mb-16" data-aos="fade-up">
      <div class="marine-divider mb-6"></div>
      <h2 class="font-black text-white text-4xl sm:text-5xl tracking-tight uppercase">
        <span class="lang-uk">Наше Меню</span>
        <span class="lang-bg">Меню</span>
      </h2>
      <p class="text-accent mt-3 font-semibold uppercase tracking-widest text-sm">Quality from the Black Sea</p>
    </div>

    <!-- Category: ШАУРМА -->
    <div class="mt-12 mb-6 flex flex-col md:flex-row items-center gap-3" data-aos="fade-right">
      <div class="flex items-center gap-3">
         <i data-lucide="flame" class="w-7 h-7 text-brand"></i>
         <h3 class="text-3xl font-bold text-white tracking-wide uppercase">
           <span class="lang-uk">ШАУРМА</span>
           <span class="lang-bg">ШАУРМА</span>
         </h3>
      </div>
      <div class="md:ml-4 h-px bg-brand/30 flex-1 w-full mt-2 md:mt-0"></div>
    </div>
    
    <!-- Using horizontal cards for a neat, dense list that fits all 12 items beautifully -->
    <div class="grid md:grid-cols-2 gap-4">
      
      <!-- 1 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="0">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-dark/80 text-white text-xs flex items-center justify-center font-bold z-10">1</div>
          <img src="https://images.unsplash.com/photo-1561050501-9a7a6e0ff4ef?w=600&auto=format&fit=crop&q=80" alt="Classic" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
          <div class="flex items-start justify-between w-full h-full">
            <div class="flex flex-col h-full justify-center pr-12">
               <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма класична</span><span class="lang-bg">Шаурма класическа</span>
               </h4>
               <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">Classic Shawarma</div>
            </div>
            <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">6.5€</span>
          </div>
        </div>
      </div>

      <!-- 2 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="50">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-dark/80 text-white text-xs flex items-center justify-center font-bold z-10">2</div>
          <img src="https://images.unsplash.com/photo-1626804475297-41609ea0dc4f?w=600&auto=format&fit=crop&q=80" alt="Pork" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
          <div class="flex items-start justify-between w-full h-full">
            <div class="flex flex-col h-full justify-center pr-12">
               <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма відібрана свинина</span><span class="lang-bg">Шаурма от свинско месо</span>
               </h4>
               <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">Pork Shawarma</div>
            </div>
            <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">6.5€</span>
          </div>
        </div>
      </div>

      <!-- 3 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg border-brand/40" data-aos="fade-up" data-aos-delay="0">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-brand text-white text-xs flex items-center justify-center font-bold z-10">3</div>
          <img src="https://images.unsplash.com/photo-1648838775432-8e100ae966b9?w=600&auto=format&fit=crop&q=80" alt="Assorted" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
          <div class="flex items-start justify-between w-full h-full">
            <div class="flex flex-col h-full justify-center pr-12">
               <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма асорті</span><span class="lang-bg">Шаурма асорти</span>
               </h4>
               <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">Assorted Shawarma</div>
            </div>
            <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3 text-white bg-brand border-none">10€</span>
          </div>
        </div>
      </div>

      <!-- 4 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="50">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-dark/80 text-white text-xs flex items-center justify-center font-bold z-10">4</div>
          <img src="https://images.unsplash.com/photo-1599487488170-d11ec9c172f0?w=600&auto=format&fit=crop&q=80" alt="Fish" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
          <div class="flex items-start justify-between w-full h-full">
            <div class="flex flex-col h-full justify-center pr-12">
               <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма з червоною рибою</span><span class="lang-bg">Шаурма с красна риба</span>
               </h4>
               <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">Red fish Shawarma</div>
            </div>
            <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">9.5€</span>
          </div>
        </div>
      </div>

      <!-- 5 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="0">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-dark/80 text-white text-xs flex items-center justify-center font-bold z-10">5</div>
          <img src="https://images.unsplash.com/photo-1565299585323-38d6b0865b47?w=600&auto=format&fit=crop&q=80" alt="Hawaii" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
           <div class="flex flex-col h-full justify-center pr-12">
              <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма гавайська</span><span class="lang-bg">Шаурма хавайска</span>
              </h4>
              <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">Hawaii Shawarma</div>
           </div>
           <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">9.5€</span>
        </div>
      </div>

      <!-- 6 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="50">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-dark/80 text-white text-xs flex items-center justify-center font-bold z-10">6</div>
          <img src="https://images.unsplash.com/photo-1528736235302-52922df5c1b6?w=600&auto=format&fit=crop&q=80" alt="5 Cheese" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
           <div class="flex flex-col h-full justify-center pr-12">
              <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма 5 сирів</span><span class="lang-bg">Шаурма 5 сирине</span>
              </h4>
              <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">5 Cheese Shawarma</div>
           </div>
           <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">9.5€</span>
        </div>
      </div>

      <!-- 7 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="0">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-red-600 text-white text-xs flex items-center justify-center font-bold z-10">7</div>
          <img src="https://images.unsplash.com/photo-1588168333986-5078d3ae3976?w=600&auto=format&fit=crop&q=80" alt="Mexican" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
           <div class="flex flex-col h-full justify-center pr-12">
              <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма мексиканська</span><span class="lang-bg">Шаурма мексиканска</span>
              </h4>
              <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1 pr-4">Mexican Shawarma 🌶️</div>
           </div>
           <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">8.5€</span>
        </div>
      </div>

      <!-- 8 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="50">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-dark/80 text-white text-xs flex items-center justify-center font-bold z-10">8</div>
          <img src="https://images.unsplash.com/photo-1625937286074-9ca519d5d9df?w=600&auto=format&fit=crop&q=80" alt="Shrimp" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
           <div class="flex flex-col h-full justify-center pr-12">
              <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма з креветками і мідіями</span><span class="lang-bg">Шаурма с креветки мидии</span>
              </h4>
              <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">Shrimp & mussels</div>
           </div>
           <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">9.5€</span>
        </div>
      </div>

      <!-- 9 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="0">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-green-600 text-white text-xs flex items-center justify-center font-bold z-10">9</div>
          <img src="https://images.unsplash.com/photo-1585238341267-1cb11f26f2f1?w=600&auto=format&fit=crop&q=80" alt="Vegan" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
           <div class="flex flex-col h-full justify-center pr-12">
              <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма вегетаріанська</span><span class="lang-bg">Шаурма вегетарианска</span>
              </h4>
              <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">Shawarma vegan 🌱</div>
           </div>
           <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">6.5€</span>
        </div>
      </div>

      <!-- 10 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg border-brand/40" data-aos="fade-up" data-aos-delay="50">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-brand text-white text-xs flex items-center justify-center font-bold z-10">10</div>
          <img src="https://images.unsplash.com/photo-1559847844-5315695dadae?w=600&auto=format&fit=crop&q=80" alt="Chef" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
           <div class="flex flex-col h-full justify-center pr-12">
              <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма авторська</span><span class="lang-bg">Шаурма авторска</span>
              </h4>
              <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1 text-accent">Chef Shawarma ★</div>
           </div>
           <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">8€</span>
        </div>
      </div>

      <!-- 11 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="0">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-dark/80 text-white text-xs flex items-center justify-center font-bold z-10">11</div>
          <img src="https://images.unsplash.com/photo-1551024601-bec78aea704b?w=600&auto=format&fit=crop&q=80" alt="Sweet" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
           <div class="flex flex-col h-full justify-center pr-12">
              <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Шаурма солодка</span><span class="lang-bg">Шаурма сладка</span>
              </h4>
              <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">Sweet Shawarma</div>
           </div>
           <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">6.5€</span>
        </div>
      </div>

      <!-- 12 -->
      <div class="menu-card glass rounded-2xl overflow-hidden flex flex-row h-28 sm:h-32 shadow-lg" data-aos="fade-up" data-aos-delay="50">
        <div class="w-1/3 sm:w-[140px] h-full overflow-hidden shrink-0 relative">
          <div class="absolute top-2 left-2 w-6 h-6 rounded-full bg-dark/80 text-white text-xs flex items-center justify-center font-bold z-10">12</div>
          <img src="https://images.unsplash.com/photo-1634567280735-8ea13fefdd25?w=600&auto=format&fit=crop&q=80" alt="Suluguni" class="menu-img w-full h-full object-cover" />
        </div>
        <div class="p-3 sm:p-4 flex flex-col justify-center flex-1 relative">
           <div class="flex flex-col h-full justify-center pr-12">
              <h4 class="font-bold text-[13px] sm:text-[15px] text-white leading-tight">
                 <span class="lang-uk">Сулугуні в лаваші</span><span class="lang-bg">Сулугуни в лаваш</span>
              </h4>
              <div class="text-[10px] sm:text-xs text-gray-400 font-medium mt-1">Suluguni</div>
           </div>
           <span class="menu-price px-2 py-1 rounded-lg font-black text-sm sm:text-base absolute top-1/2 -translate-y-1/2 right-3">5.5€</span>
        </div>
      </div>

    </div>

    <!-- Category: BBQ -->
    <div class="mt-16 mb-6 flex flex-col md:flex-row items-center gap-3" data-aos="fade-right">
      <div class="flex items-center gap-3">
         <i data-lucide="drumstick" class="w-7 h-7 text-brand"></i>
         <h3 class="text-3xl font-bold text-white tracking-wide uppercase">BBQ</h3>
         <span class="text-xs font-semibold text-gray-400 border border-gray-600 px-2 py-0.5 rounded-md ml-2 hidden sm:block">100 грам</span>
      </div>
      <div class="md:ml-4 h-px bg-brand/30 flex-1 w-full mt-2 md:mt-0"></div>
    </div>
    
    <div class="grid md:grid-cols-2 gap-4">
      <!-- 13 -->
      <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
         <div class="flex items-center gap-4">
           <div class="relative w-16 sm:w-20 h-16 sm:h-20 shrink-0">
             <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">13</div>
             <img src="https://images.unsplash.com/photo-1555939594-58d7cb561ad1?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover shadow-lg" alt="Pork Neck">
           </div>
           <div>
              <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                <span class="lang-uk">Шашлик зі свинячого ошийка</span><span class="lang-bg">Шашлик от свински врат</span>
              </h4>
              <p class="text-gray-400 text-[10px] sm:text-xs mt-1">BBQ pork neck</p>
           </div>
         </div>
         <span class="menu-price px-3 py-1 rounded-lg font-black text-sm sm:text-base">4€</span>
      </div>

      <!-- 14 -->
      <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
         <div class="flex items-center gap-4">
           <div class="relative w-16 sm:w-20 h-16 sm:h-20 shrink-0">
             <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">14</div>
             <img src="https://images.unsplash.com/photo-1544025162-d76694265947?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover shadow-lg" alt="Ribs">
           </div>
           <div>
              <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                <span class="lang-uk">Свинячі ребра на грилі</span><span class="lang-bg">Свински ребра на скара</span>
              </h4>
              <p class="text-gray-400 text-[10px] sm:text-xs mt-1">Pork grilled ribs</p>
           </div>
         </div>
         <span class="menu-price px-3 py-1 rounded-lg font-black text-sm sm:text-base">4€</span>
      </div>

      <!-- 15 -->
      <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
         <div class="flex items-center gap-4">
           <div class="relative w-16 sm:w-20 h-16 sm:h-20 shrink-0">
             <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">15</div>
             <img src="https://images.unsplash.com/photo-1565557613262-e4210fd6c99c?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover shadow-lg" alt="Wings">
           </div>
           <div>
              <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                <span class="lang-uk">Курячі крильця</span><span class="lang-bg">Пилешки крилца</span>
              </h4>
              <p class="text-gray-400 text-[10px] sm:text-xs mt-1">Grilled chicken wings</p>
           </div>
         </div>
         <span class="menu-price px-3 py-1 rounded-lg font-black text-sm sm:text-base">3.5€</span>
      </div>

      <!-- 16 -->
      <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
         <div class="flex items-center gap-4">
           <div class="relative w-16 sm:w-20 h-16 sm:h-20 shrink-0">
             <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">16</div>
             <img src="https://images.unsplash.com/photo-1598514982205-f36b96d1ea8d?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover shadow-lg" alt="Chicken Skewers">
           </div>
           <div>
              <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                <span class="lang-uk">Курячий шашлик</span><span class="lang-bg">Пилешки шашлик</span>
              </h4>
              <p class="text-gray-400 text-[10px] sm:text-xs mt-1">Chicken BBQ skewers</p>
           </div>
         </div>
         <span class="menu-price px-3 py-1 rounded-lg font-black text-sm sm:text-base">4€</span>
      </div>
    </div>

    <!-- Category: ПЪРЖЕНИ -->
    <div class="mt-16 mb-6 flex flex-col md:flex-row items-center gap-3" data-aos="fade-right">
      <div class="flex items-center gap-3">
         <i data-lucide="waves" class="w-7 h-7 text-brand"></i>
         <h3 class="text-3xl font-bold text-white tracking-wide uppercase">
           <span class="lang-uk">ФРИТЮР</span><span class="lang-bg">ПЪРЖЕНИ</span>
         </h3>
         <span class="text-xs font-semibold text-gray-400 border border-gray-600 px-2 py-0.5 rounded-md ml-2 hidden sm:block">100 грам</span>
      </div>
      <div class="md:ml-4 h-px bg-brand/30 flex-1 w-full mt-2 md:mt-0"></div>
    </div>

    <div class="grid md:grid-cols-2 gap-4">
      <!-- 17 -->
      <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
         <div class="flex items-center gap-4">
           <div class="relative w-16 sm:w-20 h-16 sm:h-20 shrink-0">
             <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">17</div>
             <img src="https://images.unsplash.com/photo-1604908176997-125f25cc6f3d?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover shadow-lg" alt="Squids">
           </div>
           <div>
              <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                <span class="lang-uk">Кальмари, Цаца</span><span class="lang-bg">Калмари, Цаца</span>
              </h4>
              <p class="text-gray-400 text-[10px] sm:text-xs mt-1">Squids, Sprat fish</p>
           </div>
         </div>
         <span class="menu-price px-3 py-1 rounded-lg font-black text-sm sm:text-base">3€</span>
      </div>

      <!-- 18 -->
      <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
         <div class="flex items-center gap-4">
           <div class="relative w-16 sm:w-20 h-16 sm:h-20 shrink-0">
             <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">18</div>
             <img src="https://images.unsplash.com/photo-1448043552756-e747b7a2b2b8?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover shadow-lg" alt="Mussels">
           </div>
           <div>
              <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                <span class="lang-uk">Мідії, Хамса, Сардини</span><span class="lang-bg">Мидии, Хамсия, Сардини</span>
              </h4>
              <p class="text-gray-400 text-[10px] sm:text-xs mt-1">Mussels, Sardines</p>
           </div>
         </div>
         <span class="menu-price px-3 py-1 rounded-lg font-black text-sm sm:text-base">4€</span>
      </div>

      <!-- 19 -->
      <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
         <div class="flex items-center gap-4">
           <div class="relative w-16 sm:w-20 h-16 sm:h-20 shrink-0">
             <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">19</div>
             <img src="https://images.unsplash.com/photo-1569691899455-88464f6d3ab1?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover shadow-lg" alt="Nuggets">
           </div>
           <div>
              <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                <span class="lang-uk">Нагетси</span><span class="lang-bg">Нагетси</span>
              </h4>
              <p class="text-gray-400 text-[10px] sm:text-xs mt-1">Nuggets</p>
           </div>
         </div>
         <span class="menu-price px-3 py-1 rounded-lg font-black text-sm sm:text-base">3.5€</span>
      </div>

      <!-- 20 -->
      <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
         <div class="flex items-center gap-4">
           <div class="relative w-16 sm:w-20 h-16 sm:h-20 shrink-0">
             <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">20</div>
             <img src="https://images.unsplash.com/photo-1576107246150-13f8c85fa6d1?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover shadow-lg" alt="Fries">
           </div>
           <div>
              <div class="flex items-center gap-2">
                 <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                   <span class="lang-uk">Картопля фрі</span><span class="lang-bg">Пържени картофки</span>
                 </h4>
                 <span class="text-[9px] font-semibold text-gray-500 border border-gray-600 px-1 py-[1px] rounded whitespace-nowrap">150g</span>
              </div>
              <p class="text-gray-400 text-[10px] sm:text-xs mt-1">French fries</p>
           </div>
         </div>
         <span class="menu-price px-3 py-1 rounded-lg font-black text-sm sm:text-base">3€</span>
      </div>

      <!-- 21 -->
      <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
         <div class="flex items-center gap-4">
           <div class="relative w-16 sm:w-20 h-16 sm:h-20 shrink-0">
             <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">21</div>
             <img src="https://images.unsplash.com/photo-1626081014138-04fb33ee662a?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover shadow-lg" alt="Fried Cheese">
           </div>
           <div>
              <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                <span class="lang-uk">Смажений сир</span><span class="lang-bg">Пържено сирене</span>
              </h4>
              <p class="text-gray-400 text-[10px] sm:text-xs mt-1">Fried cheese</p>
           </div>
         </div>
         <span class="menu-price px-3 py-1 rounded-lg font-black text-sm sm:text-base">3€</span>
      </div>
    </div>

    <!-- 2 Cols layout for the remaining Categories -->
    <div class="grid md:grid-cols-2 gap-10 lg:gap-16 mt-16">
        
        <!-- Category: САЛАТА -->
        <div>
          <div class="mb-6 flex flex-col md:flex-row items-center gap-3" data-aos="fade-right">
            <div class="flex items-center gap-3">
               <i data-lucide="leaf" class="w-6 h-6 text-brand"></i>
               <h3 class="text-2xl font-bold text-white tracking-wide uppercase">
                 <span class="lang-uk">САЛАТИ</span><span class="lang-bg">САЛАТА</span>
               </h3>
            </div>
            <div class="md:ml-2 h-px bg-brand/30 flex-1 w-full mt-2 md:mt-0"></div>
          </div>
          
          <div class="flex flex-col gap-4">
            <!-- 22 -->
            <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up">
               <div class="flex items-center gap-4">
                 <div class="relative w-16 h-16 shrink-0">
                   <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">22</div>
                   <img src="https://images.unsplash.com/photo-1540189549336-e6e99c3679fe?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover" alt="Standard Salad">
                 </div>
                 <div>
                    <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                      <span class="lang-uk">Стандартний</span><span class="lang-bg">Стандартен</span>
                    </h4>
                    <p class="text-gray-400 text-[10px] sm:text-xs mt-1">Standard</p>
                 </div>
               </div>
               <span class="menu-price px-3 py-1 rounded-lg font-black text-sm">4.5€</span>
            </div>
            <!-- 23 -->
            <div class="menu-card glass rounded-2xl p-4 flex items-center justify-between" data-aos="fade-up" data-aos-delay="50">
               <div class="flex items-center gap-4">
                 <div class="relative w-16 h-16 shrink-0">
                   <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">23</div>
                   <img src="https://images.unsplash.com/photo-1592417817098-8fd3d9eb14a5?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover" alt="Caprese">
                 </div>
                 <div>
                    <h4 class="font-bold text-white text-[13px] sm:text-[15px] leading-tight">
                      <span class="lang-uk">Капрезе</span><span class="lang-bg">Капрезе</span>
                    </h4>
                    <p class="text-gray-400 text-[10px] sm:text-xs mt-1">Caprese</p>
                 </div>
               </div>
               <span class="menu-price px-3 py-1 rounded-lg font-black text-sm">6.5€</span>
            </div>
          </div>
        </div>

        <!-- Category: ДОПЪЛНИТЕЛНИ ЯСТИЯ -->
        <div>
          <div class="mb-6 flex flex-col md:flex-row items-center gap-3" data-aos="fade-right" data-aos-delay="100">
            <div class="flex items-center gap-3">
               <i data-lucide="utensils-crossed" class="w-6 h-6 text-brand"></i>
               <h3 class="text-2xl font-bold text-white tracking-wide uppercase text-center sm:text-left">
                 <span class="lang-uk">ДОДАТКОВІ СТРАВИ</span><span class="lang-bg">ДОПЪЛНИТЕЛНИ ЯСТИЯ</span>
               </h3>
            </div>
            <div class="md:ml-2 h-px bg-brand/30 flex-1 w-full mt-2 md:mt-0"></div>
          </div>
          
          <div class="flex flex-col gap-4">
            <!-- 24 -->
            <div class="menu-card glass rounded-2xl p-4 flex items-center gap-4" data-aos="fade-up">
              <div class="relative w-16 h-16 shrink-0">
                 <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">24</div>
                 <img src="https://images.unsplash.com/photo-1552611052-33e04de081de?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover" alt="Pelmeni">
              </div>
              <div class="flex-1 flex items-center justify-between pr-2">
                 <div>
                    <h4 class="font-bold text-white text-[13px] sm:text-[14px] leading-tight max-w-[150px]">
                      <span class="lang-uk">Пельмені (свинина, яловичина)</span><span class="lang-bg">Пелмени (свинско говеждо месо)</span>
                    </h4>
                    <p class="text-gray-400 text-[10px] mt-1">Dumplings</p>
                 </div>
                 <span class="menu-price px-3 py-1 rounded-lg font-black text-sm shrink-0">5.5€</span>
              </div>
            </div>
            <!-- 25 -->
            <div class="menu-card glass rounded-2xl p-4 flex items-center gap-4" data-aos="fade-up" data-aos-delay="50">
              <div class="relative w-16 h-16 shrink-0">
                 <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">25</div>
                 <img src="https://images.unsplash.com/photo-1625944230945-1b7dd1109033?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover" alt="Vareniki">
              </div>
              <div class="flex-1 flex items-center justify-between pr-2">
                 <div>
                    <h4 class="font-bold text-white text-[13px] sm:text-[14px] leading-tight max-w-[150px]">
                      <span class="lang-uk">Вареники (картопля, вишня)</span><span class="lang-bg">Вареники (картофи, вишни)</span>
                    </h4>
                 </div>
                 <span class="menu-price px-3 py-1 rounded-lg font-black text-sm shrink-0">5.5€</span>
              </div>
            </div>
            <!-- 26 -->
            <div class="menu-card glass rounded-2xl p-4 flex items-center gap-4" data-aos="fade-up" data-aos-delay="100">
              <div class="relative w-16 h-16 shrink-0">
                 <div class="absolute -top-2 -left-2 w-5 h-5 rounded-full bg-dark/80 border border-white/10 text-white text-[10px] flex items-center justify-center font-bold z-10">26</div>
                 <img src="https://images.unsplash.com/photo-1582298538104-e35002b85e92?w=200&auto=format&fit=crop&q=80" class="w-full h-full rounded-lg object-cover" alt="Boiled Shrimp">
              </div>
              <div class="flex-1 flex items-center justify-between pr-2">
                 <div>
                    <div class="flex items-center gap-2">
                      <h4 class="font-bold text-white text-[13px] sm:text-[14px] leading-tight">
                        <span class="lang-uk">Креветки варені</span><span class="lang-bg">Креветки варени</span>
                      </h4>
                      <span class="text-[9px] font-semibold text-gray-500 border border-gray-600 px-1 py-[1px] rounded whitespace-nowrap">500g</span>
                    </div>
                    <p class="text-gray-400 text-[10px] mt-1">Shrimps boiled</p>
                 </div>
                 <span class="menu-price px-3 py-1 rounded-lg font-black text-sm shrink-0">13€</span>
              </div>
            </div>
          </div>
        </div>
    </div>

    <!-- Category: НАПИТКИ (Drinks) -->
    <div class="mt-16" data-aos="fade-up">
      <div class="mb-6 flex flex-col md:flex-row items-center gap-3">
         <div class="flex items-center gap-3 justify-center md:justify-start w-full md:w-auto">
            <i data-lucide="cup-soda" class="w-6 h-6 text-brand"></i>
            <h3 class="text-2xl font-bold text-white tracking-wide uppercase">
              <span class="lang-uk">НАПОЇ</span><span class="lang-bg">НАПИТКИ</span>
            </h3>
         </div>
         <div class="hidden md:block h-px bg-brand/30 flex-1 w-full mt-2 md:mt-0"></div>
      </div>
      
      <div class="menu-card glass rounded-3xl p-6 md:p-8 flex flex-col sm:flex-row items-center gap-6 shadow-[0_0_40px_rgba(0,85,129,0.1)] border-brand/20">
         <div class="w-full sm:w-32 h-32 shrink-0 rounded-2xl overflow-hidden shadow-lg border border-white/5">
            <img src="https://images.unsplash.com/photo-1622483767028-3f66f32aef97?w=400&auto=format&fit=crop&q=80" class="w-full h-full object-cover" alt="Drinks">
         </div>
         <div class="flex-1 text-center sm:text-left">
            <div class="text-[10px] text-gray-500 font-bold uppercase tracking-widest mb-2">0.5 / 1L</div>
            <h4 class="font-bold text-white text-lg md:text-xl leading-relaxed max-w-xl text-gray-300">
               Cola, Fanta, Sprite, <span class="lang-uk">Живчик</span><span class="lang-bg">Живчик</span>, <span class="lang-uk">Квас</span><span class="lang-bg">Квас</span>, <span class="lang-uk">Айран</span><span class="lang-bg">Айран</span>
            </h4>
         </div>
         <div class="shrink-0 mt-4 sm:mt-0">
            <span class="menu-price px-6 py-3 rounded-xl font-black text-xl md:text-2xl shadow-xl shadow-accent/20 block text-center">2.5€</span>
         </div>
      </div>
    </div>

  </div>
</section>

<!-- REVIEWS & INSTAGRAM -->
<section id="reviews" class="py-24 px-4 bg-[#010a12] relative border-y border-white/5">
  <div class="absolute right-0 top-0 w-1/3 h-full bg-brand/5 blur-[120px] rounded-full pointer-events-none"></div>
  <div class="absolute left-0 bottom-0 w-1/3 h-full bg-accent/5 blur-[120px] rounded-full pointer-events-none"></div>

  <div class="max-w-6xl mx-auto relative z-10">
    <div class="mb-20">
      <div class="text-center mb-12" data-aos="fade-up">
        <h2 class="font-black text-white text-3xl sm:text-4xl tracking-tight">
          <span class="lang-uk">Що кажуть наші гості</span>
          <span class="lang-bg">Какво казват нашите гости</span>
        </h2>
        <div class="flex justify-center flex-row gap-1 mt-4">
          <i data-lucide="star" class="w-5 h-5 text-accent fill-accent"></i>
          <i data-lucide="star" class="w-5 h-5 text-accent fill-accent"></i>
          <i data-lucide="star" class="w-5 h-5 text-accent fill-accent"></i>
          <i data-lucide="star" class="w-5 h-5 text-accent fill-accent"></i>
          <i data-lucide="star" class="w-5 h-5 text-accent fill-accent"></i>
        </div>
      </div>
      <div class="grid md:grid-cols-3 gap-6">
        <div class="glass p-6 rounded-2xl" data-aos="fade-up" data-aos-delay="0">
          <div class="flex items-center gap-3 mb-4">
            <div class="w-10 h-10 rounded-full bg-brand flex justify-center items-center font-bold text-white">M</div>
            <div>
              <div class="font-bold text-white text-sm">Максим В.</div>
              <div class="text-xs text-gray-500">Google Review</div>
            </div>
          </div>
          <p class="text-sm text-gray-300 italic">"Найкраща шаурма на узбережжі! М'ясо соковите, соус просто бомба. Обов'язково повернемось!"</p>
        </div>
        <div class="glass p-6 rounded-2xl" data-aos="fade-up" data-aos-delay="100">
          <div class="flex items-center gap-3 mb-4">
            <div class="w-10 h-10 rounded-full bg-accent text-dark flex justify-center items-center font-bold">A</div>
            <div>
              <div class="font-bold text-white text-sm">Anna Ivanova</div>
              <div class="text-xs text-gray-500">Google Review</div>
            </div>
          </div>
          <p class="text-sm text-gray-300 italic">"Много вкусна храна! Калмарите са фантастични, а обслужването е на ниво. Препоръчвам горещо."</p>
        </div>
        <div class="glass p-6 rounded-2xl" data-aos="fade-up" data-aos-delay="200">
          <div class="flex items-center gap-3 mb-4">
            <div class="w-10 h-10 rounded-full bg-gray-700 flex justify-center items-center font-bold text-white">O</div>
            <div>
              <div class="font-bold text-white text-sm">Oleksandr K.</div>
              <div class="text-xs text-gray-500">Google Review</div>
            </div>
          </div>
          <p class="text-sm text-gray-300 italic">"Шашлик просто тане у роті. Тепер ми постійні клієнти. Дякую за шматочок Одеси в Болгарії!"</p>
        </div>
      </div>
    </div>

    <!-- Instagram Grid -->
    <div class="text-center mb-8" data-aos="fade-up">
      <i data-lucide="instagram" class="w-8 h-8 text-brand mx-auto mb-3"></i>
      <h2 class="font-bold text-white text-2xl tracking-tight">
        <span class="lang-uk">Слідкуйте за нами в Instagram</span>
        <span class="lang-bg">Следвайте ни в Instagram</span>
      </h2>
      <a href="#" class="text-accent hover:underline text-sm font-semibold mt-2 inline-block">@shaurmama_bg</a>
    </div>

    <div class="grid grid-cols-2 md:grid-cols-6 border border-white/10 rounded-2xl overflow-hidden glass shadow-2xl" data-aos="fade-up">
      <img src="https://images.unsplash.com/photo-1579871494447-9811cf80d66c?w=400&auto=format&fit=crop&q=80" class="w-full h-40 md:h-48 object-cover hover:scale-110 transition-transform duration-500" alt="Insta 1">
      <img src="https://images.unsplash.com/photo-1544025162-d76694265947?w=400&auto=format&fit=crop&q=80" class="w-full h-40 md:h-48 object-cover hover:scale-110 transition-transform duration-500" alt="Insta 2">
      <img src="https://images.unsplash.com/photo-1628840042765-356cda07504e?w=400&auto=format&fit=crop&q=80" class="w-full h-40 md:h-48 object-cover hover:scale-110 transition-transform duration-500" alt="Insta 3">
      <img src="https://images.unsplash.com/photo-1561050501-9a7a6e0ff4ef?w=400&auto=format&fit=crop&q=80" class="w-full h-40 md:h-48 object-cover hover:scale-110 transition-transform duration-500" alt="Insta 4">
      <img src="https://images.unsplash.com/photo-1648838775432-8e100ae966b9?w=400&auto=format&fit=crop&q=80" class="w-full h-40 md:h-48 object-cover hover:scale-110 transition-transform duration-500" alt="Insta 5">
      <img src="https://images.unsplash.com/photo-1604908176997-125f25cc6f3d?w=400&auto=format&fit=crop&q=80" class="w-full h-40 md:h-48 object-cover hover:scale-110 transition-transform duration-500" alt="Insta 6">
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer id="footer" class="relative bg-[#02050A] border-t border-brand/20 pt-16 pb-8 px-4 z-10">
  <div class="max-w-6xl mx-auto grid md:grid-cols-2 gap-12 items-center">
    <div data-aos="fade-right">
      <div class="flex items-center gap-3 mb-6">
        <i data-lucide="anchor" class="w-8 h-8 text-brand"></i>
        <div class="font-mont font-900 text-3xl tracking-tight text-white leading-none">ШАУРМАМА</div>
      </div>
      <div class="space-y-4">
        <div class="flex items-center gap-3 text-gray-300">
          <div class="w-10 h-10 rounded-full bg-white/5 border border-white/10 flex justify-center items-center text-brand">
            <i data-lucide="clock" class="w-5 h-5"></i>
          </div>
          <div>
            <div class="font-semibold text-white">
              <span class="lang-uk">Час роботи</span>
              <span class="lang-bg">Работно време</span>
            </div>
            <div class="text-sm">11:00 - 21:00</div>
          </div>
        </div>
        <div class="flex items-center gap-3 text-gray-300">
          <div class="w-10 h-10 rounded-full bg-white/5 border border-white/10 flex justify-center items-center text-brand">
             <i data-lucide="map-pin" class="w-5 h-5"></i>
          </div>
          <div>
            <div class="font-semibold text-white">Luxury Beach Dolphin</div>
            <div class="text-sm">Sunny Beach, Bulgaria</div>
          </div>
        </div>
        <div class="flex flex-col items-start gap-4 mt-8">
           <a href="https://maps.google.com/?q=42.7093233,27.7214693" target="_blank" class="glass px-6 py-3 rounded-full flex items-center gap-2 text-white font-bold hover:border-accent transition-colors text-sm">
              <i data-lucide="navigation" class="w-4 h-4 text-brand"></i>
              <span class="lang-uk">Маршрут в Google Maps</span>
              <span class="lang-bg">Маршрут в Google Maps</span>
           </a>
        </div>
      </div>
    </div>
    
    <div class="flex justify-center md:justify-end" data-aos="fade-left">
       <div class="w-full max-w-sm h-64 glass rounded-3xl relative overflow-hidden flex items-center justify-center border-brand/20 shadow-[0_0_40px_rgba(0,85,129,0.2)] hover:border-brand/50 transition-colors group cursor-pointer" onclick="window.open('https://maps.google.com/?q=42.7093233,27.7214693','_blank')">
         <div class="absolute inset-0 opacity-20" style="background-image: radial-gradient(#005581 2px, transparent 2px); background-size: 20px 20px;"></div>
         <div class="absolute inset-x-0 top-1/2 h-[1px] bg-brand/30"></div>
         <div class="absolute inset-y-0 left-1/2 w-[1px] bg-brand/30"></div>
         <div class="relative z-10 flex flex-col items-center">
            <div class="w-12 h-12 bg-dark border-2 border-brand rounded-full flex justify-center items-center shadow-[0_0_20px_rgba(0,85,129,0.8)] animate-float-slow group-hover:scale-110 transition-transform">
               <i data-lucide="anchor" class="w-5 h-5 text-accent"></i>
            </div>
            <div class="bg-dark/80 px-3 py-1 rounded-full text-xs font-bold text-accent border border-white/10 mt-3 backdrop-blur-sm">
              Open Maps
            </div>
         </div>
       </div>
    </div>
  </div>

  <div class="max-w-6xl mx-auto mt-16 pt-6 border-t border-white/5 flex flex-col md:flex-row items-center justify-between text-xs text-gray-500 gap-4">
    <p>© 2024 Shaurmama Sunny Beach. All rights reserved.</p>
    <div class="flex gap-4">
      <a href="#" class="hover:text-white transition-colors"><i data-lucide="instagram" class="w-4 h-4"></i></a>
      <a href="#" class="hover:text-white transition-colors"><i data-lucide="facebook" class="w-4 h-4"></i></a>
    </div>
  </div>
</footer>

<!-- FAB (WhatsApp) -->
<a href="https://wa.me/359882789795" target="_blank"
   class="fixed bottom-6 right-5 z-[100] w-14 h-14 bg-[#25D366] rounded-full flex items-center justify-center shadow-[0_0_20px_rgba(37,211,102,0.5)] transform hover:scale-110 transition-transform hidden sm:flex"
   aria-label="WhatsApp">
   <svg class="w-7 h-7 text-white" viewBox="0 0 24 24" fill="currentColor">
    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
  </svg>
</a>
<a href="https://wa.me/359882789795" target="_blank"
   class="fixed bottom-6 right-5 z-[100] w-14 h-14 bg-[#25D366] rounded-full flex items-center justify-center shadow-[0_0_20px_rgba(37,211,102,0.5)] transform hover:scale-110 transition-transform md:hidden"
   aria-label="WhatsApp">
   <svg class="w-7 h-7 text-white" viewBox="0 0 24 24" fill="currentColor">
    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
  </svg>
</a>

<!-- SCRIPTS -->
<script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>
<script>
  AOS.init({ duration: 800, easing: 'ease-out-cubic', once: true, offset: 50 });
  lucide.createIcons();

  function setLang(lang) {
    document.documentElement.lang = lang;
    const btnUk = document.getElementById('btn-uk');
    const btnBg = document.getElementById('btn-bg');
    
    if(lang === 'uk') {
      btnUk.classList.add('active');
      btnUk.classList.remove('text-gray-400', 'hover:text-white');
      btnBg.classList.remove('active');
      btnBg.classList.add('text-gray-400', 'hover:text-white');
    } else {
      btnBg.classList.add('active');
      btnBg.classList.remove('text-gray-400', 'hover:text-white');
      btnUk.classList.remove('active');
      btnUk.classList.add('text-gray-400', 'hover:text-white');
    }
  }

  window.addEventListener('scroll', () => {
    const nav = document.querySelector('nav');
    if (window.scrollY > 40) {
      nav.style.background = 'rgba(2, 12, 20, 0.98)';
      nav.style.boxShadow = '0 10px 30px -10px rgba(0, 0, 0, 0.5)';
    } else {
      nav.style.background = 'rgba(2, 12, 20, 0.85)';
      nav.style.boxShadow = 'none';
      nav.style.borderBottomColor = 'rgba(0, 85, 129, 0.4)';
    }
  });
</script>
</body>
</html>
