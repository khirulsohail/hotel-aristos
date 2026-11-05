<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
  <meta name="description" content="Hotel Aristos Boutique & Suites — a quiet luxury urban retreat in South Khulshi, Chattogram. Book elegant rooms, premium amenities, and refined hospitality." />
  <title>Hotel Aristos Boutique & Suites · South Khulshi, Chattogram</title>

  <!-- Tailwind CSS via CDN -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Google Fonts: Playfair Display (serif) + Inter (sans-serif) -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700;800&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet" />

  <!-- Tailwind Theme Extension -->
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            charcoal: '#1A1A1A',
            gold: {
              DEFAULT: '#D4AF37',
              light: '#E6C75A',
              dark: '#A8862A',
            },
            slatey: {
              50:  '#F5F6F7',
              100: '#E7E9EC',
              200: '#C9CDD3',
              300: '#A7ADB6',
              400: '#7C828D',
              500: '#5A606B',
              600: '#3F444E',
              700: '#2B2F37',
              800: '#1D2026',
              900: '#121419',
            }
          },
          fontFamily: {
            serif: ['"Playfair Display"', 'Georgia', 'serif'],
            sans: ['Inter', 'system-ui', 'sans-serif'],
          },
          boxShadow: {
            'gold-glow': '0 10px 40px -10px rgba(212, 175, 55, 0.45)',
            'soft-dark': '0 20px 60px -20px rgba(0, 0, 0, 0.6)',
          },
        }
      }
    }
  </script>

  <!-- Inline Script: Mobile Menu Toggle -->
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const menuBtn = document.getElementById('menu-toggle');
      const mobileMenu = document.getElementById('mobile-menu');
      const menuIconOpen = document.getElementById('icon-open');
      const menuIconClose = document.getElementById('icon-close');

      menuBtn.addEventListener('click', () => {
        mobileMenu.classList.toggle('hidden');
        menuIconOpen.classList.toggle('hidden');
        menuIconClose.classList.toggle('hidden');
      });

      // Close mobile menu when any link inside it is clicked
      mobileMenu.querySelectorAll('a').forEach(link => {
        link.addEventListener('click', () => {
          mobileMenu.classList.add('hidden');
          menuIconOpen.classList.remove('hidden');
          menuIconClose.classList.add('hidden');
        });
      });
    });
  </script>
</head>

<body class="bg-charcoal text-slatey-100 font-sans antialiased selection:bg-gold/30 selection:text-white">

  <!-- ============================================= -->
  <!-- 1. HEADER & NAVIGATION                         -->
  <!-- ============================================= -->
  <header class="fixed top-0 inset-x-0 z-50 bg-charcoal/85 backdrop-blur-md border-b border-white/5">
    <nav class="max-w-7xl mx-auto px-5 md:px-8 h-20 flex items-center justify-between">
      <!-- Logo -->
      <a href="#home" class="flex items-center gap-2 group">
        <span class="font-serif text-2xl md:text-3xl tracking-wide text-white">
          Hotel <span class="text-gold font-semibold">Aristos</span>
        </span>
        <span class="hidden sm:inline-block text-[10px] uppercase tracking-[0.3em] text-slatey-300 border-l border-gold/40 pl-2 ml-1">
          Boutique & Suites
        </span>
      </a>

      <!-- Desktop Nav -->
      <ul class="hidden lg:flex items-center gap-9 text-sm tracking-wide text-slatey-200">
        <li><a href="#home" class="hover:text-gold transition-colors duration-300">Home</a></li>
        <li><a href="#about" class="hover:text-gold transition-colors duration-300">About</a></li>
        <li><a href="#rooms" class="hover:text-gold transition-colors duration-300">Accommodation</a></li>
        <li><a href="#amenities" class="hover:text-gold transition-colors duration-300">Amenities</a></li>
        <li><a href="#contact" class="hover:text-gold transition-colors duration-300">Contact</a></li>
      </ul>

      <!-- Right Cluster: CTA + Hamburger -->
      <div class="flex items-center gap-3">
        <a href="#book"
           class="hidden sm:inline-flex items-center gap-2 bg-gold hover:bg-gold-light text-charcoal font-semibold text-sm px-5 py-2.5 rounded-full shadow-gold-glow transition-all duration-300 hover:-translate-y-0.5">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
            <path d="M8 2v4M16 2v4M3 10h18M5 4h14a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2z"/>
          </svg>
          Book Now
        </a>

        <!-- Hamburger -->
        <button id="menu-toggle"
                aria-label="Toggle navigation"
                aria-expanded="false"
                class="lg:hidden inline-flex items-center justify-center w-11 h-11 rounded-full border border-white/10 hover:border-gold/60 text-white transition-colors">
          <!-- Open Icon -->
          <svg id="icon-open" xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <line x1="3" y1="6" x2="21" y2="6" />
            <line x1="3" y1="12" x2="21" y2="12" />
            <line x1="3" y1="18" x2="21" y2="18" />
          </svg>
          <!-- Close Icon -->
          <svg id="icon-close" xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 hidden" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <line x1="18" y1="6" x2="6" y2="18" />
            <line x1="6" y1="6" x2="18" y2="18" />
          </svg>
        </button>
      </div>
    </nav>

    <!-- Mobile Menu -->
    <div id="mobile-menu" class="hidden lg:hidden border-t border-white/5 bg-charcoal/95 backdrop-blur-md">
      <ul class="px-6 py-6 flex flex-col gap-4 text-slatey-100">
        <li><a href="#home" class="block py-2 hover:text-gold transition">Home</a></li>
        <li><a href="#about" class="block py-2 hover:text-gold transition">About</a></li>
        <li><a href="#rooms" class="block py-2 hover:text-gold transition">Accommodation</a></li>
        <li><a href="#amenities" class="block py-2 hover:text-gold transition">Amenities</a></li>
        <li><a href="#contact" class="block py-2 hover:text-gold transition">Contact</a></li>
        <li class="pt-2">
          <a href="#book" class="inline-flex w-full justify-center items-center gap-2 bg-gold text-charcoal font-semibold px-5 py-3 rounded-full">
            Book Now
          </a>
        </li>
      </ul>
    </div>
  </header>

  <main>
    <!-- ============================================= -->
    <!-- 2. HERO SHOWCASE                              -->
    <!-- ============================================= -->
    <section id="home" class="relative min-h-screen w-full flex items-center overflow-hidden">
      <!-- Background Image -->
      <div class="absolute inset-0">
        <img src="https://images.unsplash.com/photo-1564501049412-61c2a3083791?auto=format&fit=crop&w=1920&q=80"
             alt="Hotel Aristos Boutique facade at dusk"
             class="w-full h-full object-cover" />
        <div class="absolute inset-0 bg-gradient-to-b from-charcoal/85 via-charcoal/55 to-charcoal/95"></div>
        <div class="absolute inset-0 bg-gradient-to-r from-charcoal/80 to-transparent"></div>
      </div>

      <!-- Hero Content -->
      <div class="relative z-10 max-w-7xl mx-auto px-5 md:px-8 pt-28 pb-16 w-full">
        <div class="max-w-3xl">
          <p class="inline-flex items-center gap-3 text-xs uppercase tracking-[0.35em] text-gold mb-6">
            <span class="h-px w-10 bg-gold"></span>
            South Khulshi · Chattogram
          </p>

          <h1 class="font-serif text-4xl sm:text-5xl md:text-6xl lg:text-7xl leading-[1.05] text-white">
            A Quiet Luxury<br />
            <span class="text-gold italic">Urban Retreat</span> in<br />
            the Heart of Khulshi.
          </h1>

          <p class="mt-6 text-base md:text-lg text-slatey-200 max-w-xl leading-relaxed">
            Discover refined boutique hospitality where contemporary design meets serene comfort —
            crafted for travellers who value stillness, style, and personalised service.
          </p>

          <div class="mt-8 flex flex-wrap gap-4">
            <a href="#rooms" class="inline-flex items-center gap-2 bg-gold hover:bg-gold-light text-charcoal font-semibold px-7 py-3.5 rounded-full shadow-gold-glow transition-all duration-300 hover:-translate-y-0.5">
              Explore Suites
            </a>
            <a href="#about" class="inline-flex items-center gap-2 border border-white/25 hover:border-gold hover:text-gold text-white font-medium px-7 py-3.5 rounded-full transition-all duration-300">
              Our Story
            </a>
          </div>
        </div>

        <!-- Reservation Block -->
        <div id="book" class="mt-12 lg:mt-16 max-w-4xl bg-charcoal/80 backdrop-blur-xl border border-white/10 rounded-2xl p-5 md:p-7 shadow-soft-dark">
          <h3 class="font-serif text-lg md:text-xl text-white mb-4 flex items-center gap-2">
            <span class="w-1.5 h-5 bg-gold rounded-full"></span>
            Reserve Your Stay
          </h3>
          <form class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4" onsubmit="event.preventDefault(); alert('Availability search initiated. Our front desk will reach out shortly.');">
            <!-- Check-in -->
            <div>
              <label for="checkin" class="block text-[11px] uppercase tracking-[0.2em] text-slatey-300 mb-1.5">Check-in</label>
              <input type="date" id="checkin" name="checkin"
                     class="w-full bg-slatey-800/60 border border-white/10 focus:border-gold/60 focus:ring-1 focus:ring-gold/40 rounded-lg px-3.5 py-2.5 text-sm text-white placeholder-slatey-400 outline-none transition" />
            </div>
            <!-- Check-out -->
            <div>
              <label for="checkout" class="block text-[11px] uppercase tracking-[0.2em] text-slatey-300 mb-1.5">Check-out</label>
              <input type="date" id="checkout" name="checkout"
                     class="w-full bg-slatey-800/60 border border-white/10 focus:border-gold/60 focus:ring-1 focus:ring-gold/40 rounded-lg px-3.5 py-2.5 text-sm text-white placeholder-slatey-400 outline-none transition" />
            </div>
            <!-- Guests -->
            <div>
              <label for="guests" class="block text-[11px] uppercase tracking-[0.2em] text-slatey-300 mb-1.5">Guests</label>
              <select id="guests" name="guests"
                      class="w-full bg-slatey-800/60 border border-white/10 focus:border-gold/60 focus:ring-1 focus:ring-gold/40 rounded-lg px-3.5 py-2.5 text-sm text-white outline-none transition">
                <option class="bg-charcoal">1 Adult</option>
                <option class="bg-charcoal">2 Adults</option>
                <option class="bg-charcoal">2 Adults · 1 Child</option>
                <option class="bg-charcoal">2 Adults · 2 Children</option>
                <option class="bg-charcoal">3 Adults</option>
                <option class="bg-charcoal">4 Adults</option>
              </select>
            </div>
            <!-- Submit -->
            <div class="flex items-end">
              <button type="submit"
                      class="w-full inline-flex items-center justify-center gap-2 bg-gold hover:bg-gold-light text-charcoal font-semibold px-5 py-2.5 rounded-lg shadow-gold-glow transition-all duration-300 hover:-translate-y-0.5">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                  <circle cx="11" cy="11" r="8" />
                  <line x1="21" y1="21" x2="16.65" y2="16.65" />
                </svg>
                Search
              </button>
            </div>
          </form>
        </div>
      </div>

      <!-- Scroll cue -->
      <a href="#about" class="absolute bottom-6 left-1/2 -translate-x-1/2 z-10 hidden md:flex flex-col items-center gap-2 text-slatey-300 hover:text-gold transition">
        <span class="text-[10px] uppercase tracking-[0.3em]">Scroll</span>
        <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4 animate-bounce" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <line x1="12" y1="5" x2="12" y2="19" />
          <polyline points="19 12 12 19 5 12" />
        </svg>
      </a>
    </section>

    <!-- ============================================= -->
    <!-- 3. ABOUT SECTION                              -->
    <!-- ============================================= -->
    <section id="about" class="relative py-20 md:py-28 bg-charcoal">
      <div class="max-w-7xl mx-auto px-5 md:px-8 grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16 items-center">
        <!-- Image Split -->
        <div class="relative order-2 lg:order-1">
          <div class="grid grid-cols-2 gap-4">
            <img src="https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?auto=format&fit=crop&w=600&q=80"
                 alt="Elegant boutique room interior"
                 class="rounded-2xl w-full h-72 md:h-96 object-cover shadow-soft-dark" />
            <img src="https://images.unsplash.com/photo-1611892440504-42a792e24d32?auto=format&fit=crop&w=600&q=80"
                 alt="Serene lobby lounge"
                 class="rounded-2xl w-full h-72 md:h-96 object-cover mt-8 shadow-soft-dark" />
          </div>
          <!-- Floating accent badge -->
          <div class="absolute -bottom-6 left-1/2 -translate-x-1/2 lg:left-auto lg:right-6 bg-gold text-charcoal px-5 py-3 rounded-xl shadow-gold-glow text-center">
            <p class="font-serif text-2xl font-bold leading-none">12+</p>
            <p class="text-[10px] uppercase tracking-[0.2em] mt-1">Years of Hospitality</p>
          </div>
        </div>

        <!-- Text Split -->
        <div class="order-1 lg:order-2">
          <p class="inline-flex items-center gap-3 text-xs uppercase tracking-[0.35em] text-gold mb-5">
            <span class="h-px w-10 bg-gold"></span>
            Our Philosophy
          </p>
          <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl text-white leading-tight">
            Serenity, Refined for the<br />
            <span class="text-gold italic">Modern Traveller.</span>
          </h2>
          <p class="mt-6 text-slatey-200 leading-relaxed">
            Nestled in the leafy, residential enclave of South Khulshi, Hotel Aristos Boutique & Suites
            is a sanctuary from Chattogram's restless pulse. Every corner is composed with intention —
            from warm ambient lighting to curated textures and muted earth tones — so that the moment
            you step through our doors, the city softens into stillness.
          </p>
          <p class="mt-4 text-slatey-300 leading-relaxed">
            Our hospitality is unhurried and bespoke. Whether you're visiting for business, a weekend
            retreat, or an extended stay, our team crafts an experience that feels personal, quiet,
            and unmistakably premium.
          </p>

          <!-- Mini stats -->
          <div class="mt-9 grid grid-cols-3 gap-4">
            <div class="border-l-2 border-gold/60 pl-4">
              <p class="font-serif text-2xl text-white">42</p>
              <p class="text-xs uppercase tracking-wider text-slatey-400 mt-1">Curated Rooms</p>
            </div>
            <div class="border-l-2 border-gold/60 pl-4">
              <p class="font-serif text-2xl text-white">7</p>
              <p class="text-xs uppercase tracking-wider text-slatey-400 mt-1">Premium Amenities</p>
            </div>
            <div class="border-l-2 border-gold/60 pl-4">
              <p class="font-serif text-2xl text-white">24/7</p>
              <p class="text-xs uppercase tracking-wider text-slatey-400 mt-1">Concierge Care</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ============================================= -->
    <!-- 4. ACCOMMODATION GRID                         -->
    <!-- ============================================= -->
    <section id="rooms" class="relative py-20 md:py-28 bg-slatey-900">
      <div class="max-w-7xl mx-auto px-5 md:px-8">
        <!-- Section header -->
        <div class="text-center max-w-2xl mx-auto mb-14">
          <p class="inline-flex items-center gap-3 text-xs uppercase tracking-[0.35em] text-gold mb-4">
            <span class="h-px w-10 bg-gold"></span>
            Accommodation
            <span class="h-px w-10 bg-gold"></span>
          </p>
          <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl text-white leading-tight">
            Rooms Crafted for Every Kind of Retreat
          </h2>
          <p class="mt-5 text-slatey-300 leading-relaxed">
            Each suite balances privacy, comfort, and quiet luxury — designed with thoughtful detail
            and warm, layered textures.
          </p>
        </div>

        <!-- Grid -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">

          <!-- Executive Single -->
          <article class="group bg-charcoal border border-white/5 rounded-2xl overflow-hidden hover:border-gold/40 transition-all duration-500 hover:-translate-y-2 hover:shadow-soft-dark">
            <div class="relative h-56 overflow-hidden">
              <img src="https://images.unsplash.com/photo-1631049307264-da0ec9d70304?auto=format&fit=crop&w=600&q=80"
                   alt="Executive Single room"
                   class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" />
              <div class="absolute top-3 right-3 bg-gold text-charcoal text-xs font-semibold px-3 py-1.5 rounded-full shadow-gold-glow">
                BDT 2,800 / night
              </div>
            </div>
            <div class="p-6">
              <h3 class="font-serif text-xl text-white mb-2 group-hover:text-gold transition-colors">Executive Single</h3>
              <p class="text-sm text-slatey-300 leading-relaxed mb-5">
                A refined 22 m² sanctuary with a plush queen bed, ergonomic workspace, and curated
                ambient lighting for the solo traveller.
              </p>
              <a href="#book" class="inline-flex items-center gap-2 text-sm text-gold font-medium hover:gap-3 transition-all">
                Reserve
                <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                  <line x1="5" y1="12" x2="19" y2="12" />
                  <polyline points="12 5 19 12 12 19" />
                </svg>
              </a>
            </div>
          </article>

          <!-- Deluxe Couple -->
          <article class="group bg-charcoal border border-white/5 rounded-2xl overflow-hidden hover:border-gold/40 transition-all duration-500 hover:-translate-y-2 hover:shadow-soft-dark">
            <div class="relative h-56 overflow-hidden">
              <img src="https://images.unsplash.com/photo-1611892440504-42a792e24d32?auto=format&fit=crop&w=600&q=80"
                   alt="Deluxe Couple room"
                   class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" />
              <div class="absolute top-3 right-3 bg-gold text-charcoal text-xs font-semibold px-3 py-1.5 rounded-full shadow-gold-glow">
                BDT 4,000 / night
              </div>
            </div>
            <div class="p-6">
              <h3 class="font-serif text-xl text-white mb-2 group-hover:text-gold transition-colors">Deluxe Couple</h3>
              <p class="text-sm text-slatey-300 leading-relaxed mb-5">
                An intimate 28 m² suite with king bed, rainfall shower, and a private lounge
                corner — perfect for two.
              </p>
              <a href="#book" class="inline-flex items-center gap-2 text-sm text-gold font-medium hover:gap-3 transition-all">
                Reserve
                <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                  <line x1="5" y1="12" x2="19" y2="12" />
                  <polyline points="12 5 19 12 12 19" />
                </svg>
              </a>
            </div>
          </article>

          <!-- Deluxe Twin -->
          <article class="group bg-charcoal border border-white/5 rounded-2xl overflow-hidden hover:border-gold/40 transition-all duration-500 hover:-translate-y-2 hover:shadow-soft-dark">
            <div class="relative h-56 overflow-hidden">
              <img src="https://images.unsplash.com/photo-1566665797739-1674de2a421a?auto=format&fit=crop&w=600&q=80"
                   alt="Deluxe Twin room"
                   class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" />
              <div class="absolute top-3 right-3 bg-gold text-charcoal text-xs font-semibold px-3 py-1.5 rounded-full shadow-gold-glow">
                BDT 4,000 / night
              </div>
            </div>
            <div class="p-6">
              <h3 class="font-serif text-xl text-white mb-2 group-hover:text-gold transition-colors">Deluxe Twin</h3>
              <p class="text-sm text-slatey-300 leading-relaxed mb-5">
                Two premium single beds in a spacious 30 m² layout with separate work desks — ideal
                for business partners or friends.
              </p>
              <a href="#book" class="inline-flex items-center gap-2 text-sm text-gold font-medium hover:gap-3 transition-all">
                Reserve
                <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                  <line x1="5" y1="12" x2="19" y2="12" />
                  <polyline points="12 5 19 12 12 19" />
                </svg>
              </a>
            </div>
          </article>

          <!-- Deluxe Family -->
          <article class="group bg-charcoal border border-gold/30 rounded-2xl overflow-hidden transition-all duration-500 hover:-translate-y-2 hover:shadow-gold-glow relative">
            <span class="absolute top-3 left-3 z-10 bg-charcoal text-gold text-[10px] uppercase tracking-wider px-3 py-1 rounded-full border border-gold/40">
              Most Popular
            </span>
            <div class="relative h-56 overflow-hidden">
              <img src="https://images.unsplash.com/photo-1582719478250-c89cae4dc85b?auto=format&fit=crop&w=600&q=80"
                   alt="Deluxe Family room"
                   class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-700" />
              <div class="absolute top-3 right-3 bg-gold text-charcoal text-xs font-semibold px-3 py-1.5 rounded-full shadow-gold-glow">
                BDT 4,500 / night
              </div>
            </div>
            <div class="p-6">
              <h3 class="font-serif text-xl text-white mb-2 group-hover:text-gold transition-colors">Deluxe Family</h3>
              <p class="text-sm text-slatey-300 leading-relaxed mb-5">
                A generous 38 m² suite with a king bed and two twin beds, family lounge, and
                adjoining bathroom — built for shared comfort.
              </p>
              <a href="#book" class="inline-flex items-center gap-2 text-sm text-gold font-medium hover:gap-3 transition-all">
                Reserve
                <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
                  <line x1="5" y1="12" x2="19" y2="12" />
                  <polyline points="12 5 19 12 12 19" />
                </svg>
              </a>
            </div>
          </article>

        </div>
      </div>
    </section>

    <!-- ============================================= -->
    <!-- 5. FEATURES & AMENITIES                       -->
    <!-- ============================================= -->
    <section id="amenities" class="relative py-20 md:py-28 bg-charcoal">
      <div class="max-w-7xl mx-auto px-5 md:px-8">
        <!-- Header -->
        <div class="text-center max-w-2xl mx-auto mb-14">
          <p class="inline-flex items-center gap-3 text-xs uppercase tracking-[0.35em] text-gold mb-4">
            <span class="h-px w-10 bg-gold"></span>
            Features & Amenities
            <span class="h-px w-10 bg-gold"></span>
          </p>
          <h2 class="font-serif text-3xl md:text-4xl lg:text-5xl text-white leading-tight">
            Everything You Need,<br />Quietly Considered.
          </h2>
        </div>

        <!-- Grid -->
        <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-5">

          <!-- Indoor Swimming Pool -->
          <div class="group flex flex-col items-center text-center bg-slatey-800/40 border border-white/5 rounded-2xl p-7 hover:border-gold/40 hover:bg-slatey-800/70 transition-all duration-300 hover:-translate-y-1">
            <div class="w-14 h-14 rounded-full bg-gold/10 flex items-center justify-center text-gold mb-4 group-hover:bg-gold group-hover:text-charcoal transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M2 20h20M2 16c1.5 0 1.5 1 3 1s1.5-1 3-1 1.5 1 3 1 1.5-1 3-1 1.5 1 3 1 1.5-1 3-1M6 12V5a2 2 0 0 1 2-2h2M14 12V5a2 2 0 0 1 2-2h2" />
              </svg>
            </div>
            <h3 class="font-serif text-base text-white mb-1">Indoor Swimming Pool</h3>
            <p class="text-xs text-slatey-400">Heated · Year-round</p>
          </div>

          <!-- Fitness Gym -->
          <div class="group flex flex-col items-center text-center bg-slatey-800/40 border border-white/5 rounded-2xl p-7 hover:border-gold/40 hover:bg-slatey-800/70 transition-all duration-300 hover:-translate-y-1">
            <div class="w-14 h-14 rounded-full bg-gold/10 flex items-center justify-center text-gold mb-4 group-hover:bg-gold group-hover:text-charcoal transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M6.5 6.5h11M17.5 17.5h-11M3 7v10M21 7v10M9 9v6M15 9v6" />
              </svg>
            </div>
            <h3 class="font-serif text-base text-white mb-1">Fitness Gym</h3>
            <p class="text-xs text-slatey-400">Modern Equipment</p>
          </div>

          <!-- On-site Restaurant -->
          <div class="group flex flex-col items-center text-center bg-slatey-800/40 border border-white/5 rounded-2xl p-7 hover:border-gold/40 hover:bg-slatey-800/70 transition-all duration-300 hover:-translate-y-1">
            <div class="w-14 h-14 rounded-full bg-gold/10 flex items-center justify-center text-gold mb-4 group-hover:bg-gold group-hover:text-charcoal transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M3 2v7c0 1.1.9 2 2 2h0a2 2 0 0 0 2-2V2M5 11v11M19 2c-1.5 0-3 1.5-3 4v6c0 1.1.9 2 2 2h0a2 2 0 0 0 2-2V8M18 22V14" />
              </svg>
            </div>
            <h3 class="font-serif text-base text-white mb-1">On-site Restaurant</h3>
            <p class="text-xs text-slatey-400">Curated Menu</p>
          </div>

          <!-- Free Private Parking -->
          <div class="group flex flex-col items-center text-center bg-slatey-800/40 border border-white/5 rounded-2xl p-7 hover:border-gold/40 hover:bg-slatey-800/70 transition-all duration-300 hover:-translate-y-1">
            <div class="w-14 h-14 rounded-full bg-gold/10 flex items-center justify-center text-gold mb-4 group-hover:bg-gold group-hover:text-charcoal transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <rect x="3" y="3" width="18" height="18" rx="2" />
                <path d="M9 17V7h4a3 3 0 0 1 0 6H9" />
              </svg>
            </div>
            <h3 class="font-serif text-base text-white mb-1">Free Private Parking</h3>
            <p class="text-xs text-slatey-400">Secure · 24/7</p>
          </div>

          <!-- High-Speed Wi-Fi -->
          <div class="group flex flex-col items-center text-center bg-slatey-800/40 border border-white/5 rounded-2xl p-7 hover:border-gold/40 hover:bg-slatey-800/70 transition-all duration-300 hover:-translate-y-1">
            <div class="w-14 h-14 rounded-full bg-gold/10 flex items-center justify-center text-gold mb-4 group-hover:bg-gold group-hover:text-charcoal transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M5 12.55a11 11 0 0 1 14.08 0M1.42 9a16 16 0 0 1 21.16 0M8.53 16.11a6 6 0 0 1 6.95 0M12 20h.01" />
              </svg>
            </div>
            <h3 class="font-serif text-base text-white mb-1">High-Speed Wi-Fi</h3>
            <p class="text-xs text-slatey-400">Fibre · Whole Property</p>
          </div>

          <!-- 24-Hour Room Service -->
          <div class="group flex flex-col items-center text-center bg-slatey-800/40 border border-white/5 rounded-2xl p-7 hover:border-gold/40 hover:bg-slatey-800/70 transition-all duration-300 hover:-translate-y-1">
            <div class="w-14 h-14 rounded-full bg-gold/10 flex items-center justify-center text-gold mb-4 group-hover:bg-gold group-hover:text-charcoal transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <circle cx="12" cy="12" r="10" />
                <polyline points="12 6 12 12 16 14" />
              </svg>
            </div>
            <h3 class="font-serif text-base text-white mb-1">24-Hour Room Service</h3>
            <p class="text-xs text-slatey-400">Anytime · In-Room Dining</p>
          </div>

          <!-- Complimentary Daily Buffet Breakfast -->
          <div class="group flex flex-col items-center text-center bg-slatey-800/40 border border-white/5 rounded-2xl p-7 hover:border-gold/40 hover:bg-slatey-800/70 transition-all duration-300 hover:-translate-y-1">
            <div class="w-14 h-14 rounded-full bg-gold/10 flex items-center justify-center text-gold mb-4 group-hover:bg-gold group-hover:text-charcoal transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M17 8h1a4 4 0 1 1 0 8h-1M3 8h14v9a4 4 0 0 1-4 4H7a4 4 0 0 1-4-4z" />
                <line x1="6" y1="2" x2="6" y2="4" />
                <line x1="10" y1="2" x2="10" y2="4" />
                <line x1="14" y1="2" x2="14" y2="4" />
              </svg>
            </div>
            <h3 class="font-serif text-base text-white mb-1">Daily Buffet Breakfast</h3>
            <p class="text-xs text-slatey-400">Complimentary</p>
          </div>

          <!-- Concierge (extra structural card to fill 8-grid cleanly) -->
          <div class="group flex flex-col items-center text-center bg-gradient-to-br from-gold/15 to-transparent border border-gold/30 rounded-2xl p-7 hover:border-gold/60 transition-all duration-300 hover:-translate-y-1">
            <div class="w-14 h-14 rounded-full bg-gold flex items-center justify-center text-charcoal mb-4">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M12 2l2.39 4.84 5.34.78-3.86 3.76.91 5.31L12 14.13 7.21 16.7l.91-5.31L4.27 7.62l5.34-.78L12 2z" />
              </svg>
            </div>
            <h3 class="font-serif text-base text-white mb-1">Boutique Concierge</h3>
            <p class="text-xs text-slatey-400">Personalised Care</p>
          </div>

        </div>
      </div>
    </section>

    <!-- ============================================= -->
    <!-- CTA STRIP                                     -->
    <!-- ============================================= -->
    <section class="relative py-16 bg-slatey-900 border-y border-white/5">
      <div class="max-w-5xl mx-auto px-5 md:px-8 text-center">
        <h2 class="font-serif text-2xl md:text-4xl text-white leading-tight">
          Ready to experience <span class="text-gold italic">quiet luxury</span>?
        </h2>
        <p class="mt-4 text-slatey-300 max-w-2xl mx-auto">
          Reserve your stay directly with our front desk for the best available rate and complimentary upgrades.
        </p>
        <a href="tel:+8801820524413" class="mt-7 inline-flex items-center gap-2 bg-gold hover:bg-gold-light text-charcoal font-semibold px-8 py-3.5 rounded-full shadow-gold-glow transition-all duration-300 hover:-translate-y-0.5">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
            <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z" />
          </svg>
          +880 1820 524413
        </a>
      </div>
    </section>
  </main>

  <!-- ============================================= -->
  <!-- 6. FOOTER                                     -->
  <!-- ============================================= -->
  <footer id="contact" class="bg-charcoal border-t border-white/5">
    <div class="max-w-7xl mx-auto px-5 md:px-8 py-16">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-10">

        <!-- Brand -->
        <div class="lg:col-span-1">
          <h3 class="font-serif text-2xl text-white">
            Hotel <span class="text-gold">Aristos</span>
          </h3>
          <p class="text-[10px] uppercase tracking-[0.3em] text-slatey-400 mt-1">Boutique & Suites</p>
          <p class="mt-5 text-sm text-slatey-300 leading-relaxed">
            A quiet luxury urban retreat in the heart of South Khulshi, Chattogram. Designed for the
            modern traveller who values stillness and refinement.
          </p>
        </div>

        <!-- Address -->
        <div>
          <h4 class="font-serif text-base text-gold mb-5">Visit Us</h4>
          <address class="not-italic text-sm text-slatey-300 leading-relaxed space-y-2">
            <p>House 3, Road 3, South Khulshi</p>
            <p>Chattogram 4225, Bangladesh</p>
            <p class="text-slatey-400">GPS: 22.3594° N, 91.8214° E</p>
          </address>
          <a href="https://maps.google.com/?q=South+Khulshi+Chattogram"
             target="_blank" rel="noopener"
             class="mt-4 inline-flex items-center gap-2 text-sm text-gold hover:gap-3 transition-all">
            Get Directions
            <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round">
              <line x1="5" y1="12" x2="19" y2="12" />
              <polyline points="12 5 19 12 12 19" />
            </svg>
          </a>
        </div>

        <!-- Contact -->
        <div>
          <h4 class="font-serif text-base text-gold mb-5">Contact</h4>
          <ul class="space-y-3 text-sm text-slatey-300">
            <li>
              <a href="tel:+8801820524413" class="inline-flex items-center gap-3 hover:text-gold transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4 text-gold" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z" />
                </svg>
                +880 1820 524413
              </a>
            </li>
            <li>
              <a href="tel:+8801818699845" class="inline-flex items-center gap-3 hover:text-gold transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4 text-gold" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z" />
                </svg>
                +880 1818 699845
              </a>
            </li>
            <li>
              <a href="mailto:aristosctg@gmail.com" class="inline-flex items-center gap-3 hover:text-gold transition">
                <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4 text-gold" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z" />
                  <polyline points="22,6 12,13 2,6" />
                </svg>
                aristosctg@gmail.com
              </a>
            </li>
          </ul>
        </div>

        <!-- Social + Quick Links -->
        <div>
          <h4 class="font-serif text-base text-gold mb-5">Connect</h4>
          <div class="flex items-center gap-3 mb-7">
            <!-- Facebook -->
            <a href="#" aria-label="Facebook" class="w-10 h-10 rounded-full bg-slatey-800/60 border border-white/10 hover:bg-gold hover:text-charcoal hover:border-gold text-slatey-200 flex items-center justify-center transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M22 12c0-5.52-4.48-10-10-10S2 6.48 2 12c0 4.84 3.44 8.87 8 9.8V15H8v-3h2V9.5C10 7.57 11.57 6 13.5 6H16v3h-2c-.55 0-1 .45-1 1v2h3v3h-3v6.95c5.05-.5 9-4.76 9-9.95z"/></svg>
            </a>
            <!-- Instagram -->
            <a href="#" aria-label="Instagram" class="w-10 h-10 rounded-full bg-slatey-800/60 border border-white/10 hover:bg-gold hover:text-charcoal hover:border-gold text-slatey-200 flex items-center justify-center transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
            </a>
            <!-- X / Twitter -->
            <a href="#" aria-label="X" class="w-10 h-10 rounded-full bg-slatey-800/60 border border-white/10 hover:bg-gold hover:text-charcoal hover:border-gold text-slatey-200 flex items-center justify-center transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
            </a>
            <!-- WhatsApp -->
            <a href="#" aria-label="WhatsApp" class="w-10 h-10 rounded-full bg-slatey-800/60 border border-white/10 hover:bg-gold hover:text-charcoal hover:border-gold text-slatey-200 flex items-center justify-center transition-all duration-300">
              <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.967-.94 1.165-.173.198-.347.223-.644.074-.297-.149-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.297-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51l-.57-.01c-.198 0-.52.074-.792.372s-1.04 1.016-1.04 2.479 1.065 2.876 1.213 3.074c.149.198 2.095 3.2 5.076 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.872.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.981.999-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.83 9.83 0 0 1 2.893 6.994c-.003 5.45-4.437 9.885-9.885 9.885M20.52 3.449C18.24 1.245 15.24 0 12.045 0 5.463 0 .104 5.334.101 11.892c0 2.096.549 4.142 1.595 5.945L0 24l6.305-1.654a11.9 11.9 0 0 0 5.683 1.444h.005c6.581 0 11.94-5.335 11.943-11.893a11.8 11.8 0 0 0-3.485-8.448"/></svg>
            </a>
          </div>

          <h4 class="font-serif text-base text-gold mb-4">Quick Links</h4>
          <ul class="space-y-2 text-sm text-slatey-300">
            <li><a href="#about" class="hover:text-gold transition">About Aristos</a></li>
            <li><a href="#rooms" class="hover:text-gold transition">Accommodation</a></li>
            <li><a href="#amenities" class="hover:text-gold transition">Amenities</a></li>
            <li><a href="#book" class="hover:text-gold transition">Book a Room</a></li>
          </ul>
        </div>
      </div>

      <!-- Bottom bar -->
      <div class="mt-14 pt-7 border-t border-white/5 flex flex-col md:flex-row items-center justify-between gap-4 text-xs text-slatey-400">
        <p>© 2026 Hotel Aristos Boutique & Suites. All rights reserved.</p>
        <div class="flex items-center gap-5">
          <a href="#" class="hover:text-gold transition">Privacy Policy</a>
          <a href="#" class="hover:text-gold transition">Terms of Service</a>
          <a href="#" class="hover:text-gold transition">Cancellation</a>
        </div>
      </div>
    </div>
  </footer>
</body>
</html>
