<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>¿Dirás que sí?</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">
<style>
  /* Una tarjeta centrada sobre fondo menta; look único (claro) en cualquier tema */
  :root {
    --menta: #a8ece7; --menta2: #bfe9e4; --rosa: #f3d9da;
    --blanco: #ffffff; --texto: #667077; --gris: #93a3a1;
    --verde: #14b39a; --verde2: #1fc9a8; --rojo: #e2363b; --rojo2: #f0654a;
    --fuente: 'Poppins', system-ui, -apple-system, 'Segoe UI', sans-serif;
    color-scheme: light;
  }
  * { box-sizing: border-box; }
  html, body { height: 100%; }
  body {
    margin: 0;
    font-family: var(--fuente);
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    padding-left: max(16px, env(safe-area-inset-left, 0px));
    padding-right: max(16px, env(safe-area-inset-right, 0px));
    padding-block: 16px;
    background: linear-gradient(160deg, var(--menta) 0%, var(--menta2) 50%, var(--rosa) 100%);
    background-color: var(--menta2);
    -webkit-tap-highlight-color: transparent;
    user-select: none;
    -webkit-user-select: none;
    touch-action: manipulation;
  }

  .heart {
    position: fixed;
    bottom: -40px;
    opacity: .5;
    pointer-events: none;
    animation: subir linear forwards;
    z-index: 1;
  }
  @keyframes subir { to { transform: translateY(-110vh) rotate(25deg); opacity: 0; } }

  .card {
    position: relative;
    z-index: 2;
    width: 100%;
    max-width: 380px;
    background: var(--blanco);
    border-radius: 26px;
    padding: 28px 20px 30px;
    text-align: center;
    box-shadow: 0 20px 50px rgba(0,0,0,.12);
    animation: entrar .45s ease;
  }
  @keyframes entrar { from { transform: scale(.85); opacity: 0; } to { transform: scale(1); opacity: 1; } }

  .imagen {
    width: min(160px, 42vw);
    aspect-ratio: 1;
    max-width: 100%;
    margin: 0 auto 16px;
    border-radius: 20px;
    background: linear-gradient(145deg, #3c4150, #565c6e);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: min(84px, 22vw);
    box-shadow: inset 0 0 25px rgba(0,0,0,.25);
  }

  .progreso { font-size: 13px; color: var(--gris); margin-bottom: 6px; font-weight: 600; letter-spacing: .02em; }

  h1 {
    font-size: clamp(21px, 6vw, 25px);
    font-weight: 800;
    line-height: 1.25;
    text-wrap: balance;
    margin: 0 0 24px;
    color: var(--rojo);
    background: linear-gradient(90deg, #e8553f, #e2366b);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .botones {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    justify-content: center;
    align-items: center;
    min-height: 64px;
  }

  button {
    font-family: inherit;
    border: none;
    cursor: pointer;
    color: var(--blanco);
    font-weight: 800;
    border-radius: 999px;
    transition: transform .2s, font-size .25s, padding .25s;
  }
  button:focus-visible { outline: 3px solid var(--verde); outline-offset: 3px; }

  .si {
    background: linear-gradient(135deg, var(--verde2), var(--verde));
    font-size: 21px;
    padding: 14px 40px;
    box-shadow: 0 10px 25px rgba(20,179,154,.4);
  }
  .si:active { transform: scale(.96); }

  .no {
    background: linear-gradient(135deg, var(--rojo2), var(--rojo));
    font-size: 15px;
    padding: 13px 24px;
    box-shadow: 0 10px 25px rgba(226,54,59,.35);
    white-space: nowrap;
  }
  .no.huyendo {
    position: fixed;
    z-index: 5;
    margin: 0;
    transition: left .22s ease, top .22s ease, font-size .25s, padding .25s;
  }

  .campo {
    width: 100%;
    font-family: inherit;
    font-size: 16px;
    padding: 12px 16px;
    margin: -8px 0 18px;
    border: 2px solid #d6efec;
    border-radius: 14px;
    background: #f6fbfa;
    color: #3c4150;
    text-align: center;
    outline: none;
    user-select: text;
    -webkit-user-select: text;
  }
  .campo:focus { border-color: var(--verde2); background: var(--blanco); }
  .campo::placeholder { color: var(--gris); }
  .respuestas { color: var(--texto); font-size: 15px; margin: -8px 0 18px; }
  .respuestas b { color: var(--verde); }
  .final p { color: var(--texto); margin: -12px 0 20px; }
  .reiniciar { background: #eef6f5; color: var(--verde); font-size: 14px; padding: 10px 22px; }

  @media (prefers-reduced-motion: reduce) {
    .card, .heart { animation-duration: .01s; }
    .no.huyendo { transition: none; }
  }
</style>
</head>
<body>

<div class="card" id="card"></div>

<script>
  // ✏️ Edita aquí tus preguntas
  const preguntas = [
    { emoji: "🥺", texto: "¿Quieres ser mi amigo?" },
    { emoji: "🍦", texto: "¿Vamos por un heladito?" },
    { emoji: "🎬", texto: "¿Vemos una peli juntos?" },
    { emoji: "🤗", texto: "¿Me das un abrazo virtual?" },
    { emoji: "💚", texto: "¿Prometes no olvidarte de mí?", campo: "Escribe tu respuesta aquí" }
  ];

  const textosNo = ["No"];

  const card = document.getElementById("card");
  let actual = 0, intentos = 0, botonNo = null, ultimoEscape = 0;

  function mostrarPregunta() {
    intentos = 0;
    if (botonNo) botonNo.remove();
    const p = preguntas[actual];

    card.className = "card";
    card.style.animation = "none";
    card.offsetHeight;
    card.style.animation = "";

    card.innerHTML = `
      <div class="imagen">${p.emoji}</div>
      <div class="progreso">Pregunta ${actual + 1} de ${preguntas.length}</div>
      <h1>${p.texto}</h1>
      ${p.campo ? `<input class="campo" id="campo" type="text" maxlength="60" placeholder="${p.campo}" autocomplete="off">` : ""}
      <div class="botones">
        <button class="si" id="si">Sí 💚</button>
        <button class="no" id="no">${textosNo[0]}</button>
      </div>`;

    document.getElementById("si").addEventListener("click", responderSi);
    botonNo = document.getElementById("no");
    botonNo.addEventListener("mouseenter", escapar);
    botonNo.addEventListener("pointerdown", e => { e.preventDefault(); escapar(); });
    botonNo.addEventListener("touchstart", e => { e.preventDefault(); escapar(); }, { passive: false });
    botonNo.addEventListener("click", e => { e.preventDefault(); escapar(); });
  }

  function escapar() {
    // evita que un solo toque cuente doble (touchstart + pointerdown)
    const ahora = Date.now();
    if (ahora - ultimoEscape < 150) return;
    ultimoEscape = ahora;
    intentos++;

    if (!botonNo.classList.contains("huyendo")) {
      const r = botonNo.getBoundingClientRect();
      document.body.appendChild(botonNo);
      botonNo.classList.add("huyendo");
      botonNo.style.left = r.left + "px";
      botonNo.style.top = r.top + "px";
    }

    botonNo.textContent = textosNo[intentos % textosNo.length];
    const escalaNo = Math.max(0.6, 1 - intentos * 0.07);
    botonNo.style.fontSize = (15 * escalaNo) + "px";
    botonNo.style.padding = `${13 * escalaNo}px ${24 * escalaNo}px`;

    const si = document.getElementById("si");
    if (si) {
      const escalaSi = Math.min(1.6, 1 + intentos * 0.08);
      si.style.fontSize = (21 * escalaSi) + "px";
      si.style.padding = `${14 * escalaSi}px ${40 * escalaSi}px`;
    }

    // Nueva posición dentro de la pantalla, lejos del lugar actual y sin tapar el "Sí"
    const ancho = botonNo.offsetWidth, alto = botonNo.offsetHeight;
    const margen = 12;
    const maxX = Math.max(margen, window.innerWidth - ancho - margen);
    const maxY = Math.max(margen, window.innerHeight - alto - margen);
    const actualR = botonNo.getBoundingClientRect();
    const siR = si ? si.getBoundingClientRect() : null;
    let x, y, intentosPos = 0;
    do {
      x = margen + Math.random() * (maxX - margen);
      y = margen + Math.random() * (maxY - margen);
      intentosPos++;
      const lejos = Math.hypot(x - actualR.left, y - actualR.top) > 120;
      const tapaSi = siR && x < siR.right && x + ancho > siR.left && y < siR.bottom && y + alto > siR.top;
      if (lejos && !tapaSi) break;
    } while (intentosPos < 30);
    botonNo.style.left = x + "px";
    botonNo.style.top = y + "px";
  }

  const respuestas = [];

  function responderSi() {
    const campo = document.getElementById("campo");
    if (campo && campo.value.trim()) {
      respuestas.push({ pregunta: preguntas[actual].campo, valor: campo.value.trim() });
    }
    lluviaDeCorazones(18);
    actual++;
    if (actual < preguntas.length) setTimeout(mostrarPregunta, 250);
    else mostrarFinal();
  }

  function mostrarFinal() {
    if (botonNo) botonNo.remove();
    card.className = "card final";
    card.innerHTML = `
      <div class="imagen">🥰</div>
      <h1>¡Sabía que dirías que sí!</h1>
      <p>Eres lo máximo 💚</p>
      ${respuestas.map(r => `<div class="respuestas">${r.pregunta}<br><b></b></div>`).join("")}
      <button class="reiniciar" id="reiniciar">Volver a empezar</button>`;
    card.querySelectorAll(".respuestas b").forEach((b, i) => { b.textContent = respuestas[i].valor; });
    document.getElementById("reiniciar").onclick = () => { actual = 0; respuestas.length = 0; mostrarPregunta(); };
    let veces = 0;
    const fiesta = setInterval(() => { lluviaDeCorazones(10); if (++veces > 6) clearInterval(fiesta); }, 400);
  }

  function crearCorazon() {
    const emojis = ["💚", "💖", "💕", "🩷", "✨"];
    const h = document.createElement("div");
    h.className = "heart";
    h.textContent = emojis[Math.floor(Math.random() * emojis.length)];
    h.style.left = Math.random() * 95 + "vw";
    h.style.fontSize = (16 + Math.random() * 20) + "px";
    h.style.animationDuration = (4 + Math.random() * 4) + "s";
    document.body.appendChild(h);
    setTimeout(() => h.remove(), 8500);
  }

  function lluviaDeCorazones(n) { for (let i = 0; i < n; i++) setTimeout(crearCorazon, i * 60); }

  setInterval(crearCorazon, 900);
  mostrarPregunta();
</script>
</body>
</html>
