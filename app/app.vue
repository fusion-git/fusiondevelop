<template>
  <UApp>
    <!-- wrapper global -->
    <div
      class="flex min-h-screen flex-col items-center justify-center bg-[#0f0f11] px-4 text-[#e8e8e8]"
    >
      <!-- CARD -->
      <div
        class="w-full max-w-[1120px] rounded-xl border border-white/10 bg-[#1a1a1d] px-6 py-10 text-center shadow-[0_12px_30px_rgba(0,0,0,0.4)] sm:px-8"
      >
        <!-- LOGOS -->
        <div class="mb-8 flex items-center justify-center gap-6">
          <img
            src="/vite.svg"
            alt="Vite Logo"
            class="h-[68px] opacity-95 transition hover:opacity-100"
          />

          <span class="h-[35px] w-[2px] rounded-sm bg-white/20"></span>

          <img
            src="/fusiondevelop.svg"
            alt="Fusiondevelop Logo"
            class="h-[68px] opacity-95 transition hover:opacity-100"
          />
        </div>

        <!-- CONTENT -->
        <main>
          <h1 class="mb-3 text-[clamp(1.8rem,4vw,2.5rem)] font-extrabold text-[#646cff]">
            Fusiondevelop este în mentenanță
          </h1>

          <p class="mb-8 text-lg leading-relaxed opacity-90 sm:text-xl">
            Lucrăm la restructurarea completă a proiectului pentru a trece pe o arhitectură nouă
            bazată pe Vite și o licență MIT.
          </p>

          <!-- DETAILS -->
          <section class="mt-8 rounded-xl bg-white/5 p-6 text-left">
            <h2 class="mb-4 border-b border-white/10 pb-2 text-xl font-semibold text-[#ffac33]">
              Ce se schimbă?
            </h2>

            <ul class="space-y-3">
              <li class="flex items-start gap-3 text-lg">
                <span>✅</span>
                <span>
                  <strong>Licență Deschisă:</strong>
                  Trecere la Licența MIT pentru o adopție mai largă.
                </span>
              </li>

              <li class="flex items-start gap-3 text-lg">
                <span>🚀</span>
                <span>
                  <strong>Performanță:</strong>
                  Noua structură bazată pe Vite va asigura un workflow ultra-rapid.
                </span>
              </li>

              <li class="flex items-start gap-3 text-lg">
                <span>🏗️</span>
                <span>
                  <strong>Arhitectură:</strong>
                  Codul de bază este refăcut pentru modernizare și scalabilitate.
                </span>
              </li>
            </ul>
          </section>

          <!-- TAG -->
          <span
            class="mt-8 inline-block rounded-full bg-[#ffac33] px-5 py-1.5 font-semibold text-[#0f0f11]"
          >
            Un viitor mai rapid și mai liber.
          </span>
        </main>

        <!-- FOOTER -->
        <footer class="mt-12 text-base opacity-80">
          <p>
            Urmăriți progresul pe
            <a
              href="https://github.com/fusion-git/fusiondevelop"
              target="_blank"
              class="font-semibold text-[#646cff] transition hover:text-[#a0a0ff]"
            >
              GitHub </a
            >.
          </p>

          <p class="mt-2 text-xs opacity-60">
            © {{ year }} Fusiondevelop. Toate drepturile rezervate.
          </p>
        </footer>
      </div>
    </div>
  </UApp>
</template>

<script setup lang="ts">
const year = new Date().getFullYear()
</script>
