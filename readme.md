<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Week 07 Lab: Pure CSS Scroll Progress & Reveals</title>
</head>
<body>

  <!-- The Reading Progress Indicator -->
  <div class="progress-indicator"></div>

  <div class="article-layout">
    <header class="article-header">
      <span class="article-meta">DESIGN SYSTEMS // 2026</span>
      <h1 class="article-title">The Compositor Revolution</h1>
      <p class="article-lead">How native browser engines reclaimed scrolling animations from heavy JavaScript runtimes.</p>
    </header>

    <main class="article-body">
      <p>For over a decade, creating interactive scroll effects meant writing event listeners that intercepted the browser's scrolling thread. Every scroll tick forced the browser to run JavaScript, recalculate element coordinates, and trigger costly layout repaints. On low-power mobile devices, this resulted in choppy, frustrating interfaces.</p>

      <p>Today, modern web specifications allow us to link animation timelines directly to scroll parameters natively in CSS. This shifts the heavy mathematical lifting directly to the browser's compositor thread, running smoothly at maximum device refresh rates (90Hz, 120Hz) without waking up the main JavaScript thread.</p>

      <!-- Grid of Cards that will reveal on scroll -->
      <section class="reveal-grid">
        
        <article class="reveal-card">
          <div class="reveal-card__icon">🚀</div>
          <h3 class="reveal-card__title">Thread Isolation</h3>
          <p class="reveal-card__text">By keeping animation calculations on the compositor thread, scroll interactions remain buttery-smooth even if a heavy JS script blocks the main thread.</p>
        </article>

        <article class="reveal-card">
          <div class="reveal-card__icon">⚡</div>
          <h3 class="reveal-card__title">Declarative Keyframes</h3>
          <p class="reveal-card__text">Define your start and end positions in standard CSS keyframes, and let the browser smoothly interpolate the frames relative to scroll offsets.</p>
        </article>

        <article class="reveal-card">
          <div class="reveal-card__icon">🎨</div>
          <h3 class="reveal-card__title">Hardware Acceleration</h3>
          <p class="reveal-card__text">Animating GPU-friendly properties like transforms and opacity avoids expensive browser repaints, keeping mobile device temperatures low.</p>
        </article>

        <article class="reveal-card">
          <div class="reveal-card__icon">🔒</div>
          <h3 class="reveal-card__title">Native Security</h3>
          <p class="reveal-card__text">Reducing dependency on third-party scroll-monitoring libraries reduces your bundle size and eliminates potential security attack vectors.</p>
        </article>

      </section>
      