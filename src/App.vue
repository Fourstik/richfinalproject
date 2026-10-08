<template>
  <div id="app">
    <!-- Bootswatch Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary shadow-sm mb-4">
      <div class="container">
        <router-link class="navbar-brand font-weight-bold" :to="{ name: 'HomePage' }">
          <i class="fas fa-cubes mr-2"></i>VueJS 3
        </router-link>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarColor01">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarColor01">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'HomePage' }" exact>Home</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'BlogPage' }">Blog</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'GalleryPage' }">Gallery</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'AboutPage' }">About</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{ name: 'ContactPage' }">Contact</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Main Dynamic Route Viewport -->
    <main class="container">
      <router-view/>
    </main>

    <!-- Footer -->
    <footer class="container text-center text-muted py-4 mt-5 border-top">
      <p class="small mb-0">FIN-LAB-1: VueJS 3 Routing & Navigation Activity &copy; 2026 (Node v24 Ready)</p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
:root {
  --brand: #22c55e;
  --brand-dark: #15803d;
  --bg: #0a0a0a;
  --surface: #171717;
  --border: #2a2a2a;
  --text: #e5e7eb;
  --muted: #9ca3af;
}

/* Page */
body {
  background: var(--bg) !important;
  color: var(--text) !important;
}
h1, h2, h3, h4, h5, h6 { color: var(--brand) !important; }
.text-muted, .lead { color: var(--muted) !important; }
.border-top, hr { border-color: var(--border) !important; }

/* Links */
a { color: var(--brand) !important; }
a:hover { color: #4ade80 !important; }

/* Navbar (stays light text so it's readable on green) */
.navbar.bg-primary {
  background: linear-gradient(to bottom, var(--brand), var(--brand-dark)) !important;
}
.navbar a, .navbar .nav-link { color: #fff !important; }
.navbar-nav .router-link-exact-active {
  font-weight: 700;
  border-bottom: 2px solid #fff;
}

/* Cards, boxes, alerts */
.card, .list-group-item, .bg-white, .bg-light {
  background: var(--surface) !important;
  border-color: var(--border) !important;
  color: var(--text) !important;
}
.alert-primary, .alert-info {
  background: #052e16 !important;
  border-color: var(--brand-dark) !important;
  color: #bbf7d0 !important;
}

/* Buttons and badges */
.btn-primary, .badge-primary {
  background-color: var(--brand) !important;
  border-color: var(--brand) !important;
  color: #000 !important;
}
.btn-primary:hover { background-color: var(--brand-dark) !important; }
.btn-outline-primary {
  color: var(--brand) !important;
  border-color: var(--brand) !important;
  background: transparent !important;
}
.btn-outline-primary:hover,
.btn-outline-primary.active {
  background-color: var(--brand) !important;
  color: #000 !important;
}
.badge-light, .badge-secondary {
  background: var(--border) !important;
  color: var(--text) !important;
}

:root {
  --green: #22C55E;
  --green-rgb: 34, 197, 94;
  --green-deep: #15803D;
  --green-tint: #052E16;

  /* every Bootstrap "blue" becomes green */
  --bs-primary: var(--green);
  --bs-primary-rgb: var(--green-rgb);
  --bs-info: var(--green);
  --bs-info-rgb: var(--green-rgb);
  --bs-link-color: var(--green);
  --bs-link-hover-color: #4ADE80;
}

/* Buttons (Submit Inquiry, filter pills) */
.btn-primary,
.btn-info {
  --bs-btn-bg: var(--green-deep);
  --bs-btn-border-color: var(--green-deep);
  --bs-btn-color: #fff;
  --bs-btn-hover-bg: var(--green);
  --bs-btn-hover-border-color: var(--green);
  --bs-btn-hover-color: #052E16;
  --bs-btn-active-bg: var(--green);
  --bs-btn-active-border-color: var(--green);
}

/* Gallery filter buttons: active state ("All Works") */
.btn-group .btn.active,
.btn-group .btn:active {
  background-color: var(--green-deep) !important;
  border-color: var(--green-deep) !important;
  color: #fff !important;
}

/* Text and icon colors that were blue */
.text-primary,
.text-info,
a.text-primary,
h1.text-primary,
h2.text-primary {
  color: var(--green) !important;
}

/* Blue badges and pills (Vue Router 4, Node v24 Engine, Deployment) */
.badge.bg-primary,
.badge.bg-info,
.bg-primary,
.bg-info {
  background-color: var(--green-deep) !important;
  color: #fff !important;
}

/* About page hero: blue gradient -> deep green */
.bg-primary.bg-gradient,
.jumbotron,
.hero,
.card.bg-primary {
  background: linear-gradient(135deg, var(--green-deep), var(--green-tint)) !important;
  color: #fff !important;
}

/* Form focus rings and borders */
.form-control:focus,
.form-select:focus {
  border-color: var(--green);
  box-shadow: 0 0 0 0.25rem rgba(var(--green-rgb), 0.25);
}

/* Borders that were blue */
.border-primary,
.border-info {
  border-color: var(--green) !important;
}

.btn-primary,
.btn-info,
.btn-group .btn.active {
  background-image: linear-gradient(180deg, #22C55E, #15803D) !important;
  background-color: #15803D !important;
  border-color: #15803D !important;
  color: #fff !important;
}

.btn-primary:hover,
.btn-info:hover {
  background-image: linear-gradient(180deg, #4ADE80, #22C55E) !important;
  border-color: #22C55E !important;
  color: #052E16 !important;
}

/* ===== Navbar polish ===== */
.navbar.bg-primary {
  background: linear-gradient(135deg, #16a34a 0%, #14532d 100%) !important;
  border-bottom: 1px solid rgba(74, 222, 128, 0.35);
  box-shadow: 0 4px 20px rgba(34, 197, 94, 0.25) !important;
  padding-top: 0.7rem;
  padding-bottom: 0.7rem;
  position: sticky;
  top: 0;
  z-index: 1030;
}

/* Brand */
.navbar-brand {
  font-size: 1.35rem;
  letter-spacing: 0.5px;
  border-bottom: none !important;
}
.navbar-brand i {
  color: #86efac;
}

/* Links */
.navbar .navbar-nav .nav-link {
  color: rgba(255, 255, 255, 0.85) !important;
  padding: 0.45rem 0.9rem;
  margin: 0 0.15rem;
  border-radius: 999px;
  border-bottom: none;
  transition: background 0.2s ease, color 0.2s ease, transform 0.2s ease;
}
.navbar .navbar-nav .nav-link:hover {
  background: rgba(255, 255, 255, 0.15);
  color: #fff !important;
  transform: translateY(-1px);
}

/* Active page: pill instead of underline */
.navbar .navbar-nav .nav-link.router-link-exact-active {
  background: rgba(0, 0, 0, 0.35);
  color: #fff !important;
  font-weight: 700;
  border-bottom: none;
}
</style>
