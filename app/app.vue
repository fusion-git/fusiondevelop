<template>
  <UApp>
    <div class="card">
      <div class="logos">
        <img src="/vite.svg" alt="Vite Logo" class="logo vite-logo" />
        <span class="separator"></span>
        <img src="/fusiondevelop.svg" alt="Fusiondevelop Logo" class="logo fusiondevelop-logo" />
      </div>

      <main class="content">
        <h1 class="title">Fusiondevelop este în mentenanță</h1>
        <p class="subtitle">
          Lucrăm la restructurarea completă a proiectului pentru a trece pe o arhitectură nouă
          bazată pe Vite și o licență MIT.
        </p>

        <section class="details">
          <h2>Ce se schimbă?</h2>
          <ul>
            <li>
              ✅ <strong>Licență Deschisă:</strong>Trecere la Licența MIT pentru o adopție mai
              largă.
            </li>
            <li>
              🚀 <strong>Performanță:</strong>Noua structură bazată pe Vite va asigura un workflow
              ultra-rapid.
            </li>
            <li>
              🏗️ <strong>Arhitectură:</strong>Codul de bază este refăcut pentru modernizare și
              scalabilitate.
            </li>
          </ul>
        </section>

        <span class="tag">Un viitor mai rapid și mai liber.</span>
      </main>

      <footer>
        <p>
          Urmăriți progresul pe
          <a href="https://github.com/fusion-git/fusiondevelop" target="_blank">GitHub</a>.
        </p>
        <p class="copyright">
          © <span id="year"></span> Fusiondevelop. Toate drepturile rezervate.
        </p>
      </footer>
    </div>
    <div class="text-center">
      <p class="text-2xl font-bold">text to apply ui</p>
      <UButton>Click me</UButton>
      <UButton color="primary">Click me</UButton>
      <UButton color="secondary">Click me</UButton>
      <UButton color="success">Click me</UButton>
      <UButton color="warning">Click me</UButton>
      <UButton color="error">Click me</UButton>
      <UButton color="info">Click me</UButton>
    </div>
  </UApp>
</template>

<script setup lang="ts">
import { onMounted } from "vue"

onMounted(() => {
  const yearEl = document.getElementById("year")
  if (yearEl) {
    yearEl.textContent = String(new Date().getFullYear())
  }
})
</script>

<style>
/* --- Variabile Globale (Păstrate din codul dvs.) --- */
:root {
  --bg: #0f0f11;
  --card: #1a1a1d;
  --text: #e8e8e8;
  --accent: #646cff; /* Culoarea primară Vite */
  --secondary-accent: #ffac33; /* O nuanță caldă pentru accentul din listă */
  --radius: 12px; /* Am făcut marginile puțin mai fine */
  --transition: 0.25s ease;
}

/* --- Stiluri de Bază (Păstrate din codul dvs.) --- */
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0;
  background: var(--bg);
  color: var(--text);
  font-family: "Inter", sans-serif;
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}

.card {
  background: var(--card);
  padding: 2.5rem 2rem; /* Ușor ajustat */
  border-radius: var(--radius);
  min-width: min(95%, 1120px);
  width: 1200px;
  text-align: center;
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.4);
  border: 1px solid rgba(255, 255, 255, 0.08);
}

/* --- Stiluri Logo & Separator --- */
.logos {
  display: flex;
  justify-content: center;
  gap: 1.5rem; /* Ajustat */
  margin-bottom: 2rem;
  align-items: center;
}

.logo {
  height: 68px; /* Ajustat pentru vizibilitate */
  opacity: 0.95;
  transition: var(--transition);
}

.logo:hover {
  opacity: 1;
}

.separator {
  width: 2px;
  height: 35px;
  background-color: rgba(255, 255, 255, 0.2);
  border-radius: 1px;
}

/* --- Stiluri Text și Tag --- */
.title {
  font-size: clamp(1.8rem, 4vw, 2.5rem); /* Dimensiune adaptabilă */
  margin-bottom: 0.75rem;
  font-weight: 800; /* Mai puternic */
  color: var(--accent); /* Culoarea Vite */
}

.subtitle {
  line-height: 1.6;
  opacity: 0.9;
  font-size: 1.2rem;
  margin-bottom: 2rem;
}

.tag {
  display: inline-block;
  padding: 0.4rem 1.2rem;
  background: var(--secondary-accent); /* Altă culoare de accent */
  border-radius: 50px; /* Complet rotund */
  color: var(--bg);
  font-size: 1rem;
  font-weight: 600;
  margin-top: 2rem;
}

/* --- Stiluri Detalii (Adăugat) --- */
.details {
  margin-top: 2rem;
  background-color: rgba(255, 255, 255, 0.05); /* Ușor contrast */
  padding: 1.5rem;
  border-radius: var(--radius);
  text-align: left;
}

.details h2 {
  font-size: 1.2rem;
  font-weight: 600;
  color: var(--secondary-accent);
  margin-bottom: 1rem;
  padding-bottom: 5px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.details ul {
  list-style: none;
  padding-left: 0;
}

.details li {
  padding: 8px 0;
  font-size: 1.1rem;
  display: flex;
  align-items: center;
  gap: 10px;
}

.details li > * {
  margin-right: 5px;
}

/* --- Stiluri Footer (Ajustat) --- */
footer {
  margin-top: 3rem;
  font-size: 1rem;
  opacity: 0.8;
}

footer a {
  color: var(--accent);
  text-decoration: none;
  font-weight: 600;
  transition: color 0.3s;
}

footer a:hover {
  color: #a0a0ff;
}

.copyright {
  margin-top: 10px;
  font-size: 0.75rem;
  opacity: 0.6;
}
</style>
