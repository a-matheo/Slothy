<template>
  <div>
    <a class="skip-link" href="#contenido">Saltar al contenido</a>

    <header class="site-header" :class="{ scrolled: isScrolled }" id="inicio">
      <nav class="nav container" aria-label="Navegación principal">
        <a class="brand" href="#inicio" aria-label="Slothy, ir al inicio">
          <span class="brand-mark" aria-hidden="true">
            <svg viewBox="0 0 64 64">
              <path d="M13 28C13 15 21 8 32 8s19 7 19 20v12c0 10-8 16-19 16S13 50 13 40Z" />
              <path class="face" d="M19 29c2-9 7-14 13-14s11 5 13 14c-2 10-7 15-13 15S21 39 19 29Z" />
              <path class="mask" d="M20 28c4-7 8-9 12-9s8 2 12 9c-3 7-7 10-12 10s-9-3-12-10Z" />
              <circle cx="26" cy="29" r="2.2" />
              <circle cx="38" cy="29" r="2.2" />
              <path class="nose" d="M29 34h6l-3 3Z" />
            </svg>
          </span>
          <span><strong>Slothy</strong><small>WRO 2026 · Junior</small></span>
        </a>
        <button class="menu-toggle" type="button" aria-expanded="false" :aria-controls="'nav-links'" @click="toggleMenu">
          <span></span><span></span><span></span><span class="sr-only">Abrir menú</span>
        </button>
        <div class="nav-links" id="nav-links" :class="{ open: menuOpen }">
          <a href="#problema" @click="closeMenu">Problema</a>
          <a href="#solucion" @click="closeMenu">Solución</a>
          <a href="#tecnologia" @click="closeMenu">Tecnología</a>
          <a href="#impacto" @click="closeMenu">Impacto</a>
          <a href="#equipo" @click="closeMenu">Equipo</a>
          <a class="nav-cta" href="#demo" @click="closeMenu">Probar experiencia</a>
        </div>
      </nav>
    </header>

    <main id="contenido">
      <section class="hero">
        <div class="hero-shape hero-shape-one"></div>
        <div class="hero-shape hero-shape-two"></div>
        <div class="container hero-grid">
          <div class="hero-copy reveal visible">
            <div class="eyebrow"><span></span> Los Mechachavales · Categoría Junior</div>
            <h1>El museo que <em>escucha, responde</em> y aprende con cada niño.</h1>
            <p class="hero-lead">Slothy es un robot guía transportable para el Museo Nacional. Utiliza reconocimiento de voz, inteligencia artificial y movimiento para transformar información cultural en una experiencia clara, dinámica y adaptada de los 2 a los 12 años.</p>
            <div class="hero-actions">
              <a class="button primary" href="#demo">Vivir la demostración <span aria-hidden="true">→</span></a>
              <a class="button secondary" href="#resumen-jueces">Resumen para jueces</a>
            </div>
            <div class="hero-proof" aria-label="Capacidades principales">
              <div><strong>3</strong><span>niveles por edad</span></div>
              <div><strong>5</strong><span>funciones operativas</span></div>
              <div><strong>1</strong><span>Raspberry Pi 4</span></div>
            </div>
          </div>

          <div class="hero-visual reveal visible" aria-label="Ilustración conceptual de Slothy">
            <div class="orbit orbit-one"></div>
            <div class="orbit orbit-two"></div>
            <div class="robot-card">
              <svg class="slothy-illustration" viewBox="0 0 560 620" role="img" aria-labelledby="slothyTitle slothyDesc">
                <title id="slothyTitle">Ilustración de Slothy</title>
                <desc id="slothyDesc">Robot con forma de perezoso, pantalla, brazos móviles y base transportable.</desc>
                <defs>
                  <linearGradient id="bodyGradient" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#8f684e" /><stop offset="1" stop-color="#5b3b2e" /></linearGradient>
                  <linearGradient id="screenGradient" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#fdf3d4" /><stop offset="1" stop-color="#dff4ef" /></linearGradient>
                  <filter id="shadow" x="-30%" y="-30%" width="160%" height="160%"><feDropShadow dx="0" dy="18" stdDeviation="20" flood-opacity="0.22" /></filter>
                </defs>
                <g filter="url(#shadow)">
                  <path class="arm arm-left" d="M155 292c-74 18-110 67-106 120 2 29 17 49 37 48 19-1 29-18 22-37-9-28 15-51 66-59Z" fill="#6b4836" />
                  <path class="arm arm-right" d="M405 292c74 18 110 67 106 120-2 29-17 49-37 48-19-1-29-18-22-37 9-28-15-51-66-59Z" fill="#6b4836" />
                  <rect x="132" y="251" width="296" height="279" rx="88" fill="url(#bodyGradient)" />
                  <path d="M185 224c0-94 39-157 95-157s95 63 95 157c0 48-42 84-95 84s-95-36-95-84Z" fill="#6b4836" />
                  <ellipse cx="280" cy="211" rx="76" ry="82" fill="#e9d4b5" />
                  <path d="M208 202c16-51 42-75 72-75s56 24 72 75c-22 32-44 45-72 45s-50-13-72-45Z" fill="#8b6b58" />
                  <ellipse cx="248" cy="202" rx="19" ry="14" fill="#efe4cf" transform="rotate(-14 248 202)" />
                  <ellipse cx="312" cy="202" rx="19" ry="14" fill="#efe4cf" transform="rotate(14 312 202)" />
                  <circle cx="250" cy="202" r="5" fill="#21382d" /><circle cx="310" cy="202" r="5" fill="#21382d" />
                  <path d="M266 224q14 12 28 0" fill="none" stroke="#21382d" stroke-width="6" stroke-linecap="round" />
                  <path d="M273 216h14l-7 8Z" fill="#21382d" />
                  <rect x="172" y="318" width="216" height="144" rx="23" fill="#20372e" />
                  <rect x="184" y="330" width="192" height="120" rx="15" fill="url(#screenGradient)" />
                  <circle cx="227" cy="372" r="23" fill="#f28b30" />
                  <path d="M215 373l9 9 16-20" fill="none" stroke="#fff" stroke-width="7" stroke-linecap="round" stroke-linejoin="round" />
                  <rect x="263" y="354" width="82" height="12" rx="6" fill="#1f4d3b" opacity="0.9" />
                  <rect x="263" y="377" width="63" height="9" rx="4.5" fill="#507965" opacity="0.75" />
                  <rect x="263" y="396" width="76" height="9" rx="4.5" fill="#507965" opacity="0.55" />
                  <rect x="210" y="489" width="140" height="74" rx="31" fill="#3e2e28" />
                  <circle cx="238" cy="528" r="10" fill="#f7c85b" /><circle cx="280" cy="528" r="10" fill="#f28b30" /><circle cx="322" cy="528" r="10" fill="#6bb8a7" />
                </g>
                <g class="sound-waves" fill="none" stroke="#f28b30" stroke-width="8" stroke-linecap="round">
                  <path d="M421 150q38 33 0 66" /><path d="M445 128q64 55 0 110" />
                </g>
                <g class="sparkles" fill="#f7c85b"><path d="M100 176l7 17 17 7-17 7-7 17-7-17-17-7 17-7Z" /><circle cx="455" cy="292" r="8" /><circle cx="100" cy="316" r="6" /></g>
              </svg>
              <div class="robot-status"><span></span> Prototipo funcional</div>
            </div>
            <div class="floating-note note-one"><strong>“¿Qué deseas aprender?”</strong><span>Reconocimiento de voz</span></div>
            <div class="floating-note note-two"><strong>Respuesta adaptada</strong><span>IA + voz + movimiento</span></div>
          </div>
        </div>
      </section>

      <section class="judge-bar" aria-label="Resumen del proyecto">
        <div class="container judge-bar-grid">
          <p><span>Problema</span> Acceso limitado y lenguaje técnico</p>
          <p><span>Usuario</span> Niños de 2 a 12 años</p>
          <p><span>Caso de uso</span> Museo Nacional</p>
          <p><span>Diferenciador</span> Aprendizaje más dinámico</p>
        </div>
      </section>

      <section class="section problem" id="problema">
        <div class="container split-heading reveal visible">
          <div>
            <div class="section-kicker">01 · El reto</div>
            <h2>La cultura no debería sentirse lejana ni difícil.</h2>
          </div>
          <p>Una visita al museo puede quedar fuera del alcance de algunos niños. Incluso cuando la información está disponible, el lenguaje técnico y una explicación poco interactiva pueden reducir el interés y la comprensión.</p>
        </div>
        <div class="container challenge-grid">
          <article class="challenge-card reveal visible"><span class="card-number">01</span><div class="icon-box" aria-hidden="true">↗</div><h3>Distancia y acceso</h3><p>No todos los niños pueden desplazarse hasta un museo o participar en una visita presencial.</p></article>
          <article class="challenge-card reveal visible"><span class="card-number">02</span><div class="icon-box" aria-hidden="true">Aa</div><h3>Lenguaje complejo</h3><p>Una misma explicación no funciona igual para un niño de 3 años que para uno de 12.</p></article>
          <article class="challenge-card reveal visible"><span class="card-number">03</span><div class="icon-box" aria-hidden="true">◉</div><h3>Poca interacción</h3><p>Escuchar información sin poder preguntar, elegir o explorar hace que la experiencia pierda dinamismo.</p></article>
        </div>
        <div class="container goal-banner reveal visible">
          <div class="goal-icon" aria-hidden="true">★</div>
          <div><span>Nuestra meta</span><strong>Acercar el Museo Nacional a cada niño con una experiencia sencilla, visual y participativa.</strong></div>
        </div>
      </section>

      <section class="section solution" id="solucion">
        <div class="container section-heading centered reveal visible">
          <div class="section-kicker">02 · La solución</div>
          <h2>Slothy convierte información en conversación.</h2>
          <p>El niño no recibe una explicación fija: elige su nivel, pregunta con su voz y obtiene una respuesta adaptada.</p>
        </div>
        <div class="container flow-grid">
          <article class="flow-step reveal visible"><span>1</span><div class="flow-icon">⌁</div><h3>Elegir edad</h3><p>Selecciona Oruguitas, Aventureros o Conquista.</p></article>
          <div class="flow-arrow" aria-hidden="true">→</div>
          <article class="flow-step reveal visible"><span>2</span><div class="flow-icon">◉</div><h3>Hacer una pregunta</h3><p>El micrófono recibe la voz del niño.</p></article>
          <div class="flow-arrow" aria-hidden="true">→</div>
          <article class="flow-step reveal visible"><span>3</span><div class="flow-icon">✦</div><h3>Procesar con IA</h3><p>Raspberry Pi 4 coordina la consulta y el nivel.</p></article>
          <div class="flow-arrow" aria-hidden="true">→</div>
          <article class="flow-step reveal visible"><span>4</span><div class="flow-icon">◖</div><h3>Responder</h3><p>Slothy habla y acompaña la explicación con movimiento.</p></article>
        </div>
      </section>

      <section class="section learning" id="demo">
        <div class="container learning-grid">
          <div class="learning-copy reveal visible">
            <div class="section-kicker">03 · Demostración conceptual</div>
            <h2>Una misma pregunta. Tres formas de aprender.</h2>
            <p>Prueba cómo cambia la profundidad de la respuesta según la edad. Esta demostración web representa la lógica educativa de Slothy; el prototipo físico integra reconocimiento de voz, IA, voz y movimiento.</p>
            <div class="mode-summary">
              <span class="mode-dot dot-orange"></span><p><strong>Oruguitas:</strong> pocas palabras, ritmo pausado y apoyo visual.</p>
              <span class="mode-dot dot-green"></span><p><strong>Aventureros:</strong> lenguaje simple, más datos y exploración.</p>
              <span class="mode-dot dot-brown"></span><p><strong>Conquista:</strong> términos más técnicos y respuestas completas.</p>
            </div>
          </div>

          <div class="demo-console reveal visible" aria-label="Demostración de respuestas adaptadas">
            <div class="console-top"><div class="console-lights"><i></i><i></i><i></i></div><span>Simulador de aprendizaje Slothy</span><button id="speak-answer" type="button" aria-label="Escuchar respuesta" @click="speakAnswer">🔊</button></div>
            <div class="console-body">
              <div class="mode-tabs" role="tablist" aria-label="Seleccionar modo por edad">
                <button v-for="mode in modes" :key="mode.key" class="mode-tab" :class="{ active: selectedMode === mode.key }" type="button" role="tab" :aria-selected="selectedMode === mode.key" @click="selectedMode = mode.key">
                  <span>{{ mode.range }}</span>{{ mode.label }}
                </button>
              </div>
              <label for="demo-question">Pregunta del visitante</label>
              <select id="demo-question" v-model="selectedQuestion">
                <option value="vasija">¿Qué es una vasija precolombina?</option>
                <option value="museo">¿Por qué es importante un museo?</option>
                <option value="conservar">¿Por qué debemos cuidar los objetos antiguos?</option>
              </select>
              <div class="robot-message" aria-live="polite">
                <div class="mini-sloth" aria-hidden="true">◉ᴥ◉</div>
                <div>
                  <span>{{ answerLabel }}</span>
                  <p>{{ currentAnswer }}</p>
                </div>
              </div>
              <button class="button primary console-button" id="change-answer" type="button" @click="refreshAnswer">Adaptar explicación</button>
            </div>
          </div>
        </div>
      </section>

      <section class="section technology" id="tecnologia">
        <div class="container split-heading light reveal visible">
          <div><div class="section-kicker">04 · Tecnología</div><h2>Raspberry Pi 4 es el cerebro de Slothy.</h2></div>
          <p>Centraliza la interacción: recibe la pregunta, coordina el reconocimiento de voz, consulta la inteligencia artificial y activa la respuesta hablada y los movimientos.</p>
        </div>

        <div class="container architecture reveal visible" aria-label="Arquitectura de funcionamiento">
          <div class="architecture-node"><div class="node-icon">🎙</div><strong>Micrófono</strong><span>Pregunta del niño</span></div>
          <div class="architecture-line"><i></i><b>voz</b></div>
          <div class="architecture-node main-node"><div class="pi-board"><i></i><i></i><i></i><i></i><span>RPi 4</span></div><strong>Raspberry Pi 4</strong><span>Control central</span></div>
          <div class="architecture-line"><i></i><b>consulta</b></div>
          <div class="architecture-node"><div class="node-icon">✦</div><strong>IA</strong><span>Respuesta adaptada</span></div>
          <div class="architecture-line return-line"><i></i><b>acción</b></div>
          <div class="output-stack">
            <div class="architecture-node small-node"><div class="node-icon">🔊</div><strong>Voz</strong></div>
            <div class="architecture-node small-node"><div class="node-icon">⚙</div><strong>Servos</strong></div>
          </div>
        </div>

        <div class="container tech-bottom">
          <div class="status-panel reveal visible">
            <span class="panel-label">Estado actual del prototipo</span>
            <h3>Capacidades confirmadas en funcionamiento</h3>
            <ul class="check-list">
              <li><i>✓</i> Reconocimiento de voz</li>
              <li><i>✓</i> Respuestas mediante inteligencia artificial</li>
              <li><i>✓</i> Voz del robot</li>
              <li><i>✓</i> Movimiento con servomotores</li>
              <li><i>✓</i> Alimentación mediante batería</li>
            </ul>
          </div>
          <div class="battery-card reveal visible">
            <svg viewBox="0 0 260 160" aria-hidden="true"><rect x="32" y="32" width="188" height="96" rx="24" /><rect x="220" y="61" width="16" height="38" rx="5" /><rect class="charge" x="48" y="48" width="153" height="64" rx="13" /><path d="M125 54l-26 39h24l-10 31 42-48h-26l14-22Z" /></svg>
            <strong>Autonomía transportable</strong><p>La batería permite presentar Slothy sin depender permanentemente de una toma eléctrica.</p>
          </div>
        </div>
      </section>

      <section class="section innovation">
        <div class="container section-heading centered reveal visible">
          <div class="section-kicker">05 · Innovación</div>
          <h2>No es solo información en una pantalla.</h2>
          <p>Slothy combina una presencia física amigable con conversación, adaptación por edad y movimiento para sostener la atención del infante.</p>
        </div>
        <div class="container innovation-grid">
          <article class="innovation-card reveal visible"><div class="big-letter">D</div><h3>Dinámico</h3><p>El niño elige, pregunta, escucha y observa una reacción física del robot.</p></article>
          <article class="innovation-card featured reveal visible"><span class="feature-tag">Diferenciador principal</span><div class="big-letter">A</div><h3>Adaptativo</h3><p>La misma idea cambia en vocabulario, extensión y profundidad según el nivel de desarrollo.</p></article>
          <article class="innovation-card reveal visible"><div class="big-letter">C</div><h3>Cercano</h3><p>Su identidad de perezoso reduce la sensación de estar frente a una herramienta técnica.</p></article>
          <article class="innovation-card reveal visible"><div class="big-letter">P</div><h3>Portable</h3><p>Puede llevarse a escuelas, centros comunitarios y otras instituciones.</p></article>
        </div>
      </section>

      <section class="section impact" id="impacto">
        <div class="container impact-grid">
          <div class="impact-visual reveal visible">
            <div class="museum-scene">
              <div class="museum-roof"></div><div class="museum-name">MUSEO</div>
              <div class="columns"><i></i><i></i><i></i><i></i></div><div class="museum-base"></div>
              <div class="path"></div>
              <div class="slothy-pin"><span>◉ᴥ◉</span></div>
              <div class="school-pin"><span>ABC</span></div>
            </div>
            <div class="impact-quote">“Slothy no busca sustituir al museo; busca ser una extensión de él.”</div>
          </div>
          <div class="impact-copy reveal visible">
            <div class="section-kicker">06 · Impacto social</div>
            <h2>Una primera puerta hacia el Museo Nacional.</h2>
            <p>El caso de uso inicial está enfocado en el Museo Nacional. Slothy puede llevar parte de su experiencia educativa a niños que no pueden desplazarse, ayudándolos a descubrir el valor de visitar, conservar y comprender un museo.</p>
            <div class="impact-list">
              <div><span>01</span><p><strong>Acceso:</strong> acerca contenido cultural a más espacios.</p></div>
              <div><span>02</span><p><strong>Comprensión:</strong> ajusta el lenguaje a la edad.</p></div>
              <div><span>03</span><p><strong>Curiosidad:</strong> permite preguntar en lugar de limitarse a escuchar.</p></div>
              <div><span>04</span><p><strong>Continuidad:</strong> motiva una futura visita presencial.</p></div>
            </div>
          </div>
        </div>
      </section>

      <section class="section process" id="proceso">
        <div class="container split-heading reveal visible">
          <div><div class="section-kicker">07 · Proceso de desarrollo</div><h2>De una idea general a una identidad propia.</h2></div>
          <p>El equipo descartó propuestas, comparó alternativas, practicó modelado y reorganizó el diseño hasta llegar a un robot que une educación, arte y tecnología.</p>
        </div>
        <div class="container timeline">
          <article class="timeline-item reveal visible"><span>01</span><div><h3>Exploración inicial</h3><p>Se evaluaron una máquina de patrones y un dispositivo artístico asistido.</p></div></article>
          <article class="timeline-item reveal visible"><span>02</span><div><h3>Primer prototipo: Manolito</h3><p>Se planteó un guía de museo, pero su diseño era simple y no tenía suficiente identidad.</p></div></article>
          <article class="timeline-item reveal visible"><span>03</span><div><h3>Nace Slothy</h3><p>Se integraron tres modos, interacción mediante IA y una apariencia propia.</p></div></article>
          <article class="timeline-item reveal visible"><span>04</span><div><h3>Modelado y programación</h3><p>Se diseñó la carcasa, la distribución de componentes y el control con Raspberry Pi 4.</p></div></article>
        </div>
      </section>

      <section class="section validation">
        <div class="container validation-card reveal visible">
          <div>
            <div class="section-kicker">08 · Validación</div>
            <h2>El proyecto ya fue presentado a personas externas al equipo.</h2>
            <p>La siguiente mejora documental será registrar de manera cuantitativa las opiniones recibidas, los cambios aplicados y los resultados de pruebas con niños, docentes o personal vinculado con museos.</p>
          </div>
          <div class="validation-next">
            <span>Próxima evidencia</span>
            <ol><li>Persona consultada</li><li>Comentario recibido</li><li>Cambio realizado</li><li>Resultado observado</li></ol>
          </div>
        </div>
      </section>

      <section class="section viability">
        <div class="container section-heading centered reveal visible">
          <div class="section-kicker">09 · Viabilidad</div>
          <h2>Un camino realista para llevar Slothy a más lugares.</h2>
          <p>No se presenta un costo inventado. El presupuesto por unidad se definirá mediante cotizaciones reales de componentes, impresión 3D, batería y ensamblaje.</p>
        </div>
        <div class="container viability-steps">
          <article class="reveal visible"><span>Fase 1</span><h3>Piloto</h3><p>Probar el robot con un conjunto pequeño de contenidos del Museo Nacional.</p><i>Meta: validar interacción</i></article>
          <article class="reveal visible"><span>Fase 2</span><h3>Medición</h3><p>Registrar comprensión, interés, preguntas realizadas y fallos técnicos.</p><i>Meta: mejorar el prototipo</i></article>
          <article class="reveal visible"><span>Fase 3</span><h3>Implementación</h3><p>Crear paquetes de contenido y adaptar nuevas unidades para escuelas o instituciones.</p><i>Meta: ampliar el acceso</i></article>
        </div>
        <div class="container resource-strip reveal visible"><strong>Recursos clave:</strong><span>Raspberry Pi 4</span><span>Micrófono</span><span>Parlante</span><span>Servomotores</span><span>Batería</span><span>Carcasa 3D</span><span>Contenido educativo</span></div>
      </section>

      <section class="section team" id="equipo">
        <div class="container section-heading centered reveal visible"><div class="section-kicker">10 · Trabajo en equipo</div><h2>Los Mechachavales</h2><p>Un proyecto colaborativo entre estudiantes del Colegio Laboratorio del CUP y PRAYM Academy.</p></div>
        <div class="container team-grid">
          <article class="team-card reveal visible"><div class="avatar avatar-one"><span>AM</span></div><h3>Abdiel Matheo<br>Solano Alfaro</h3><p>Modelado 3D y programación de Raspberry Pi.</p><div class="skill-tags"><span>Diseño</span><span>Código</span></div></article>
          <article class="team-card reveal visible"><div class="avatar avatar-two"><span>MS</span></div><h3>Meredith<br>Sánchez Arce</h3><p>Redacción y desarrollo del documento escrito.</p><div class="skill-tags"><span>Investigación</span><span>Comunicación</span></div></article>
          <article class="team-card reveal visible"><div class="avatar avatar-three"><span>AV</span></div><h3>Andrés<br>Ventura Aguilar</h3><p>Modelado 3D y programación de Raspberry Pi.</p><div class="skill-tags"><span>Diseño</span><span>Código</span></div></article>
        </div>
        <div class="container teamwork-note reveal visible"><span>↔</span><p><strong>Colaboración técnica:</strong> Andrés y Matheo se apoyaron mutuamente durante el modelado y la programación para resolver problemas y unificar el prototipo.</p></div>
      </section>

      <section class="section judges" id="resumen-jueces">
        <div class="container judges-card reveal visible">
          <div class="judges-copy">
            <div class="section-kicker">Resumen para jueces</div>
            <h2>¿Por qué Slothy merece destacar?</h2>
            <p>Responde a un problema social real con una solución física, educativa y funcional. Su fortaleza está en adaptar la experiencia, no solo en mostrar información.</p>
            <button class="button light-button" id="presentation-mode" type="button" @click="activatePresentation">Activar modo presentación</button>
          </div>
          <div class="judge-checks">
            <div><i>✓</i><span><strong>Problema claro</strong>Acceso y comprensión cultural</span></div>
            <div><i>✓</i><span><strong>Usuario definido</strong>Infantes de 2 a 12 años</span></div>
            <div><i>✓</i><span><strong>Prototipo funcional</strong>Voz, IA, servos y batería</span></div>
            <div><i>✓</i><span><strong>Innovación educativa</strong>Tres niveles de explicación</span></div>
            <div><i>✓</i><span><strong>Impacto posible</strong>Museos fuera del museo</span></div>
            <div><i>✓</i><span><strong>Proceso documentado</strong>Iteración y trabajo conjunto</span></div>
          </div>
        </div>
      </section>

      <section class="section qr-section" id="qr">
        <div class="container qr-card reveal visible">
          <div class="qr-copy"><div class="section-kicker">Comparte el proyecto</div><h2>Escanea y explora Slothy.</h2><p>El código se genera automáticamente con la dirección de esta página cuando el sitio se publica en GitHub Pages.</p><div class="url-box"><span>{{ siteUrl }}</span><button id="copy-url" type="button" @click="copyUrl">Copiar</button></div></div>
          <div class="qr-box"><div id="qr-code" aria-label="Código QR del sitio web" v-html="qrMarkup"></div><span>Apunta la cámara aquí</span></div>
        </div>
      </section>
    </main>

    <footer class="footer">
      <div class="container footer-grid">
        <div class="footer-brand"><strong>Slothy</strong><span>Aprender de un museo, sin estar dentro del museo.</span></div>
        <div><span>WRO 2026</span><strong>Categoría Junior</strong></div>
        <div><span>Equipo</span><strong>Los Mechachavales</strong></div>
      </div>
      <div class="container footer-bottom"><p>Proyecto educativo desarrollado para competición de robótica.</p><a href="#inicio">Volver arriba ↑</a></div>
    </footer>

    <div class="presentation-toast" :class="{ show: presentationActive }" role="status">Modo presentación activado · Presiona Esc para salir</div>
  </div>
</template>

<script setup>
import { computed, onMounted, onUnmounted, ref } from 'vue'
import QRCode from 'qrcode'

const isScrolled = ref(false)
const menuOpen = ref(false)
const presentationActive = ref(false)
const selectedMode = ref('oruguitas')
const selectedQuestion = ref('vasija')
const modes = [
  { key: 'oruguitas', label: 'Oruguitas', range: '2–5' },
  { key: 'aventureros', label: 'Aventureros', range: '6–9' },
  { key: 'conquista', label: 'Conquista', range: '10–12' }
]

const demoContent = {
  vasija: {
    oruguitas: 'Es un recipiente muy antiguo. Las personas lo usaban para guardar comida o agua.',
    aventureros: 'Es una pieza de barro creada por pueblos indígenas antes de la llegada de los españoles. Su forma y sus dibujos nos ayudan a conocer cómo vivían.',
    conquista: 'Una vasija precolombina es una pieza arqueológica de cerámica elaborada por sociedades indígenas anteriores al periodo colonial. Su forma, decoración y lugar de hallazgo permiten estudiar actividades domésticas, rituales y comerciales.'
  },
  museo: {
    oruguitas: 'Un museo cuida cosas especiales y nos enseña historias del pasado.',
    aventureros: 'Un museo protege objetos importantes y nos permite descubrir cómo vivían otras personas y cómo cambió nuestro país.',
    conquista: 'Un museo investiga, conserva y comunica patrimonio cultural. Sus colecciones conectan evidencias del pasado con preguntas del presente y ayudan a construir memoria colectiva.'
  },
  conservar: {
    oruguitas: 'Porque son parte de nuestra historia y no se pueden reemplazar.',
    aventureros: 'Porque cada objeto antiguo guarda pistas sobre las personas que lo crearon. Si se daña, podemos perder una parte de la historia.',
    conquista: 'Debemos conservarlos porque constituyen evidencia material única. Su pérdida elimina información sobre tecnologías, creencias, alimentación, comercio y organización de sociedades anteriores.'
  }
}

const modeNames = {
  oruguitas: 'Respuesta para 2–5 años',
  aventureros: 'Respuesta para 6–9 años',
  conquista: 'Respuesta para 10–12 años'
}

const answerLabel = computed(() => modeNames[selectedMode.value])
const currentAnswer = computed(() => demoContent[selectedQuestion.value][selectedMode.value])
const qrMarkup = ref('')
const siteUrl = ref('https://TU-USUARIO.github.io/slothy-wro-2026/')

function toggleMenu() {
  menuOpen.value = !menuOpen.value
}

function closeMenu() {
  menuOpen.value = false
}

function refreshAnswer() {
  // Force reactive update for the demo content
  selectedQuestion.value = selectedQuestion.value
}

function speakAnswer() {
  if (!('speechSynthesis' in window)) return
  window.speechSynthesis.cancel()
  const utterance = new SpeechSynthesisUtterance(currentAnswer.value)
  utterance.lang = 'es-CR'
  utterance.rate = selectedMode.value === 'oruguitas' ? 0.78 : selectedMode.value === 'aventureros' ? 0.92 : 1
  const spanishVoice = window.speechSynthesis.getVoices().find((voice) => voice.lang.toLowerCase().startsWith('es'))
  if (spanishVoice) utterance.voice = spanishVoice
  window.speechSynthesis.speak(utterance)
}

async function copyUrl() {
  try {
    await navigator.clipboard.writeText(siteUrl.value)
  } catch {
    window.location.href = siteUrl.value
  }
}

function activatePresentation() {
  presentationActive.value = true
  try {
    if (!document.fullscreenElement) document.documentElement.requestFullscreen()
  } catch {}
}

function onScroll() {
  isScrolled.value = window.scrollY > 18
}

function onKeydown(event) {
  if (event.key === 'Escape') presentationActive.value = false
}

onMounted(async () => {
  onScroll()
  window.addEventListener('scroll', onScroll, { passive: true })
  window.addEventListener('keydown', onKeydown)

  const isPublished = ['http:', 'https:'].includes(window.location.protocol) && !['localhost', '127.0.0.1'].includes(window.location.hostname)
  siteUrl.value = isPublished ? window.location.href.split('#')[0].split('?')[0] : 'https://TU-USUARIO.github.io/slothy-wro-2026/'

  try {
    const svg = await QRCode.toString(siteUrl.value, { type: 'svg', margin: 1, width: 260, color: { dark: '#1e3b2d', light: '#ffffff' } })
    qrMarkup.value = svg
  } catch {
    qrMarkup.value = '<p style="padding:20px;color:#1f4d3b;font-weight:800">El QR aparecerá al publicar el sitio.</p>'
  }
})

onUnmounted(() => {
  window.removeEventListener('scroll', onScroll)
  window.removeEventListener('keydown', onKeydown)
})
</script>

<style scoped>
:root {
  --forest: #1f4d3b;
  --forest-dark: #143528;
  --forest-soft: #487563;
  --cream: #fffaf0;
  --paper: #fffdf8;
  --orange: #ef8734;
  --orange-dark: #c96620;
  --yellow: #f6c85f;
  --mint: #dff4ed;
  --teal: #65b8a4;
  --brown: #5c3c2f;
  --brown-soft: #8b6a56;
  --ink: #1c2822;
  --muted: #607069;
  --line: rgba(31, 77, 59, .14);
  --shadow: 0 24px 70px rgba(42, 58, 49, .13);
  --radius: 28px;
  --container: min(1180px, calc(100% - 40px));
}

* { box-sizing: border-box; }
html { scroll-behavior: smooth; scroll-padding-top: 90px; }
body { margin: 0; background: var(--paper); color: var(--ink); font-family: Inter, ui-rounded, "Segoe UI", system-ui, -apple-system, BlinkMacSystemFont, sans-serif; line-height: 1.6; overflow-x: hidden; }
body::selection { background: var(--yellow); color: var(--forest-dark); }
a { color: inherit; }
button, select { font: inherit; }
img, svg { max-width: 100%; display: block; }
.container { width: var(--container); margin-inline: auto; }
.sr-only { position: absolute; width: 1px; height: 1px; padding: 0; margin: -1px; overflow: hidden; clip: rect(0,0,0,0); white-space: nowrap; border: 0; }
.skip-link { position: fixed; z-index: 9999; top: 8px; left: 8px; transform: translateY(-150%); padding: 10px 16px; border-radius: 10px; background: white; color: var(--forest); }
.skip-link:focus { transform: translateY(0); }
.site-header { position: fixed; z-index: 1000; inset: 0 0 auto; background: rgba(255, 253, 248, .86); border-bottom: 1px solid transparent; backdrop-filter: blur(18px); transition: box-shadow .25s ease, border-color .25s ease; }
.site-header.scrolled { border-color: var(--line); box-shadow: 0 8px 35px rgba(31, 55, 44, .08); }
.nav { min-height: 78px; display: flex; align-items: center; justify-content: space-between; gap: 28px; }
.brand { display: flex; align-items: center; gap: 11px; text-decoration: none; color: var(--forest); }
.brand-mark { width: 48px; height: 48px; padding: 4px; display: grid; place-items: center; background: var(--mint); border-radius: 16px; }
.brand-mark svg path:first-child { fill: var(--brown); }
.brand-mark .face { fill: #ead8bf; }
.brand-mark .mask { fill: #9b7a64; }
.brand-mark circle, .brand-mark .nose { fill: var(--forest-dark); }
.brand strong { display: block; font-size: 1.2rem; line-height: 1.1; }
.brand small { display: block; margin-top: 3px; color: var(--muted); font-size: .72rem; font-weight: 700; letter-spacing: .04em; }
.nav-links { display: flex; align-items: center; gap: 27px; }
.nav-links a { position: relative; text-decoration: none; font-weight: 700; font-size: .9rem; color: #42544b; }
.nav-links > a:not(.nav-cta)::after { content: ""; position: absolute; left: 0; right: 100%; bottom: -7px; height: 2px; background: var(--orange); transition: right .25s ease; }
.nav-links > a:hover::after, .nav-links > a.active::after { right: 0; }
.nav-cta { padding: 11px 18px; background: var(--forest); color: white !important; border-radius: 999px; box-shadow: 0 8px 22px rgba(31, 77, 59, .2); }
.menu-toggle { display: none; width: 44px; height: 44px; border: 0; border-radius: 12px; background: var(--mint); padding: 11px; }
.menu-toggle span:not(.sr-only) { display: block; height: 2px; margin: 5px 0; background: var(--forest); border-radius: 2px; transition: .25s ease; }
.hero { position: relative; min-height: 840px; padding: 152px 0 85px; background: radial-gradient(circle at 10% 20%, rgba(246, 200, 95, .18), transparent 28%), radial-gradient(circle at 92% 15%, rgba(101, 184, 164, .2), transparent 30%), linear-gradient(160deg, #fffdf7 0%, #fff9e9 58%, #edf8f3 100%); overflow: hidden; }
.hero::before { content: ""; position: absolute; inset: auto 0 0; height: 170px; background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 160'%3E%3Cpath fill='%23fffdf8' d='M0 92l60 11c60 11 180 33 300 27s240-40 360-43 240 25 360 31 240-11 300-20l60-9v71H0Z'/%3E%3C/svg%3E") bottom/cover no-repeat; pointer-events: none; }
.hero-shape { position: absolute; border-radius: 50%; filter: blur(1px); opacity: .55; }
.hero-shape-one { width: 240px; height: 240px; left: -120px; top: 260px; border: 42px solid rgba(239, 135, 52, .18); }
.hero-shape-two { width: 140px; height: 140px; right: 4%; bottom: 70px; background: repeating-linear-gradient(45deg, rgba(31,77,59,.12) 0 7px, transparent 7px 14px); }
.hero-grid { display: grid; grid-template-columns: 1.03fr .97fr; align-items: center; gap: 65px; }
.eyebrow, .section-kicker { display: inline-flex; align-items: center; gap: 9px; color: var(--orange-dark); font-size: .78rem; line-height: 1.3; text-transform: uppercase; font-weight: 900; letter-spacing: .12em; }
.eyebrow span { width: 26px; height: 2px; background: currentColor; }
.hero h1 { max-width: 700px; margin: 21px 0 24px; color: var(--forest-dark); font-size: clamp(3.2rem, 5.3vw, 6.1rem); line-height: .96; letter-spacing: -.06em; }
.hero h1 em { position: relative; color: var(--orange); font-style: normal; }
.hero h1 em::after { content: ""; position: absolute; z-index: -1; left: -2%; right: -2%; bottom: 7%; height: 15%; background: var(--yellow); opacity: .45; transform: rotate(-1deg); border-radius: 100%; }
.hero-lead { max-width: 660px; margin: 0; color: #4e6258; font-size: 1.12rem; }
.hero-actions { display: flex; flex-wrap: wrap; gap: 13px; margin-top: 34px; }
.button { min-height: 50px; padding: 13px 21px; display: inline-flex; justify-content: center; align-items: center; gap: 12px; border: 0; border-radius: 15px; cursor: pointer; text-decoration: none; font-weight: 850; transition: transform .2s ease, box-shadow .2s ease, background .2s ease; }
.button:hover { transform: translateY(-2px); }
.button.primary { background: var(--forest); color: white; box-shadow: 0 13px 30px rgba(31, 77, 59, .2); }
.button.primary:hover { background: var(--forest-dark); box-shadow: 0 18px 38px rgba(31, 77, 59, .25); }
.button.secondary { background: rgba(255,255,255,.7); border: 1px solid rgba(31,77,59,.2); color: var(--forest); }
.hero-proof { display: flex; gap: 27px; margin-top: 43px; }
.hero-proof div { display: grid; grid-template-columns: auto 1fr; align-items: center; gap: 9px; }
.hero-proof strong { color: var(--forest); font-size: 1.85rem; line-height: 1; }
.hero-proof span { max-width: 82px; color: var(--muted); font-size: .78rem; line-height: 1.2; font-weight: 750; }
.hero-visual { position: relative; min-height: 610px; display: grid; place-items: center; }
.robot-card { position: relative; z-index: 2; width: min(500px, 100%); aspect-ratio: .9; padding: 24px; display: grid; place-items: center; background: rgba(255,255,255,.62); border: 1px solid rgba(255,255,255,.8); box-shadow: var(--shadow); backdrop-filter: blur(14px); border-radius: 42% 42% 27% 27% / 26% 26% 22% 22%; }
.slothy-illustration { width: 100%; max-height: 530px; overflow: visible; }
.arm-left { transform-origin: 160px 315px; animation: wave-left 4.6s ease-in-out infinite; }
.arm-right { transform-origin: 400px 315px; animation: wave-right 4.6s ease-in-out infinite; }
.sound-waves { animation: pulse-wave 2.2s ease-in-out infinite; transform-origin: 420px 190px; }
.sparkles { animation: sparkle 3s ease-in-out infinite; transform-origin: center; }
.robot-status { position: absolute; left: 50%; bottom: 23px; transform: translateX(-50%); display: flex; align-items: center; gap: 8px; padding: 8px 13px; background: white; border-radius: 999px; color: var(--forest); font-size: .75rem; font-weight: 850; box-shadow: 0 8px 25px rgba(31,77,59,.12); white-space: nowrap; }
.robot-status span { width: 8px; height: 8px; background: #49b574; border-radius: 50%; box-shadow: 0 0 0 5px rgba(73,181,116,.15); }
.orbit { position: absolute; border: 1px dashed rgba(31,77,59,.25); border-radius: 50%; animation: orbit 26s linear infinite; }
.orbit::before { content: ""; position: absolute; width: 15px; height: 15px; background: var(--orange); border: 4px solid var(--paper); border-radius: 50%; top: 8%; left: 22%; }
.orbit-one { width: 590px; height: 590px; }
.orbit-two { width: 460px; height: 460px; animation-direction: reverse; animation-duration: 20s; }
.orbit-two::before { background: var(--teal); top: 70%; left: 92%; }
.floating-note { position: absolute; z-index: 3; min-width: 195px; padding: 13px 17px; background: white; border: 1px solid var(--line); border-radius: 15px; box-shadow: 0 18px 50px rgba(40,65,53,.13); animation: float 4s ease-in-out infinite; }
.floating-note strong, .floating-note span { display: block; }
.floating-note strong { color: var(--forest); font-size: .83rem; }
.floating-note span { margin-top: 3px; color: var(--muted); font-size: .7rem; }
.note-one { left: -5%; top: 21%; }
.note-two { right: -7%; bottom: 16%; animation-delay: -2s; }
.judge-bar { position: relative; z-index: 5; margin-top: -25px; }
.judge-bar-grid { display: grid; grid-template-columns: repeat(4, 1fr); background: var(--forest); border-radius: 24px; box-shadow: 0 22px 60px rgba(31,77,59,.24); overflow: hidden; }
.judge-bar p { margin: 0; padding: 22px 25px; color: rgba(255,255,255,.78); font-size: .86rem; border-right: 1px solid rgba(255,255,255,.14); }
.judge-bar p:last-child { border: 0; }
.judge-bar span { display: block; margin-bottom: 5px; color: var(--yellow); font-size: .7rem; font-weight: 900; letter-spacing: .09em; text-transform: uppercase; }
.section { padding: 120px 0; }
.section-heading { max-width: 800px; margin-bottom: 58px; }
.section-heading.centered { margin-inline: auto; text-align: center; }
.section h2 { margin: 13px 0 18px; color: var(--forest-dark); font-size: clamp(2.3rem, 4.2vw, 4.4rem); line-height: 1.03; letter-spacing: -.055em; }
.section-heading p, .split-heading > p { color: var(--muted); font-size: 1.08rem; }
.split-heading { display: grid; grid-template-columns: 1.05fr .75fr; align-items: end; gap: 80px; margin-bottom: 55px; }
.split-heading h2 { margin-bottom: 0; }
.split-heading > p { margin: 0 0 8px; }
.challenge-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
.challenge-card { position: relative; min-height: 310px; padding: 32px; background: white; border: 1px solid var(--line); border-radius: var(--radius); overflow: hidden; transition: transform .25s ease, box-shadow .25s ease; }
.challenge-card:hover { transform: translateY(-6px); box-shadow: var(--shadow); }
.challenge-card::after { content: ""; position: absolute; right: -40px; bottom: -50px; width: 140px; height: 140px; background: var(--mint); border-radius: 50%; opacity: .75; }
.challenge-card:nth-child(2)::after { background: #fff1d6; }
.challenge-card:nth-child(3)::after { background: #f2e9df; }
.card-number { position: absolute; top: 26px; right: 28px; color: rgba(31,77,59,.19); font-weight: 900; font-size: 1rem; }
.icon-box { width: 56px; height: 56px; display: grid; place-items: center; background: var(--mint); border-radius: 18px; color: var(--forest); font-size: 1.1rem; font-weight: 900; }
.challenge-card:nth-child(2) .icon-box { background: #fff1d6; color: var(--orange-dark); }
.challenge-card:nth-child(3) .icon-box { background: #f2e9df; color: var(--brown); }
.challenge-card h3 { position: relative; z-index: 2; margin: 42px 0 10px; color: var(--forest); font-size: 1.35rem; }
.challenge-card p { position: relative; z-index: 2; margin: 0; color: var(--muted); }
.goal-banner { margin-top: 24px; padding: 28px 34px; display: flex; align-items: center; gap: 22px; background: linear-gradient(100deg, var(--forest), #2e6954); border-radius: 22px; color: white; }
.goal-icon { width: 58px; height: 58px; flex: 0 0 auto; display: grid; place-items: center; background: var(--yellow); border-radius: 18px; color: var(--forest); font-size: 1.35rem; }
.goal-banner span { display: block; color: var(--yellow); font-size: .72rem; font-weight: 900; text-transform: uppercase; letter-spacing: .1em; }
.goal-banner strong { display: block; margin-top: 4px; font-size: 1.12rem; }
.solution { background: #f6f3eb; }
.flow-grid { display: grid; grid-template-columns: 1fr auto 1fr auto 1fr auto 1fr; align-items: center; gap: 12px; }
.flow-step { min-height: 245px; padding: 25px; background: white; border-radius: 24px; border: 1px solid rgba(31,77,59,.08); box-shadow: 0 15px 40px rgba(58,71,64,.07); }
.flow-step > span { color: var(--orange); font-weight: 900; font-size: .78rem; }
.flow-icon { width: 55px; height: 55px; margin: 24px 0 20px; display: grid; place-items: center; background: var(--mint); border-radius: 50%; color: var(--forest); font-weight: 900; font-size: 1.3rem; }
.flow-step:nth-of-type(2) .flow-icon { background: #fff0d7; color: var(--orange); }
.flow-step:nth-of-type(3) .flow-icon { background: #e9e1fa; color: #665193; }
.flow-step:nth-of-type(4) .flow-icon { background: #f0e7e0; color: var(--brown); }
.flow-step h3 { margin: 0 0 7px; color: var(--forest); font-size: 1.12rem; }
.flow-step p { margin: 0; color: var(--muted); font-size: .88rem; }
.flow-arrow { color: rgba(31,77,59,.4); font-size: 1.3rem; }
.learning { background: var(--forest-dark); color: white; overflow: hidden; }
.learning-grid { display: grid; grid-template-columns: .8fr 1.2fr; align-items: center; gap: 80px; }
.learning h2, .technology h2 { color: white; }
.learning-copy > p { color: rgba(255,255,255,.68); }
.mode-summary { margin-top: 36px; display: grid; grid-template-columns: 14px 1fr; align-items: start; gap: 14px 12px; }
.mode-summary p { margin: 0; color: rgba(255,255,255,.7); font-size: .9rem; }
.mode-summary strong { color: white; }
.mode-dot { width: 11px; height: 11px; margin-top: 6px; border-radius: 50%; box-shadow: 0 0 0 5px rgba(255,255,255,.08); }
.dot-orange { background: var(--orange); }.dot-green { background: var(--teal); }.dot-brown { background: #c7a085; }
.demo-console { background: #f7f8f4; color: var(--ink); border: 8px solid #344d42; border-radius: 30px; box-shadow: 0 40px 100px rgba(0,0,0,.3); overflow: hidden; }
.console-top { min-height: 55px; padding: 0 18px; display: flex; align-items: center; gap: 15px; background: #263d33; color: rgba(255,255,255,.75); font-size: .78rem; font-weight: 750; }
.console-lights { display: flex; gap: 6px; }
.console-lights i { width: 10px; height: 10px; background: #ff6d5d; border-radius: 50%; }.console-lights i:nth-child(2){background:#f6c85f}.console-lights i:nth-child(3){background:#62c38c}
.console-top > span { flex: 1; }
.console-top button { width: 35px; height: 35px; border: 0; border-radius: 10px; background: rgba(255,255,255,.08); cursor: pointer; }
.console-body { padding: 31px; }
.mode-tabs { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; margin-bottom: 26px; }
.mode-tab { padding: 13px 8px; border: 1px solid var(--line); border-radius: 13px; background: white; color: var(--muted); cursor: pointer; font-size: .79rem; font-weight: 850; transition: .2s ease; }
.mode-tab span { display: block; color: inherit; font-size: .65rem; opacity: .7; }
.mode-tab:hover { transform: translateY(-2px); }
.mode-tab.active { background: var(--orange); border-color: var(--orange); color: white; box-shadow: 0 10px 25px rgba(239,135,52,.22); }
.console-body label { display: block; margin-bottom: 7px; color: var(--forest); font-size: .76rem; font-weight: 900; text-transform: uppercase; letter-spacing: .08em; }
.console-body select { width: 100%; padding: 13px 15px; border: 1px solid var(--line); border-radius: 13px; background: white; color: var(--ink); outline: none; }
.console-body select:focus { border-color: var(--teal); box-shadow: 0 0 0 4px rgba(101,184,164,.15); }
.robot-message { min-height: 160px; margin: 18px 0; padding: 22px; display: grid; grid-template-columns: 61px 1fr; gap: 17px; align-items: start; background: var(--mint); border-radius: 19px; }
.mini-sloth { width: 61px; height: 61px; display: grid; place-items: center; background: var(--brown); color: #f4e2ca; border-radius: 22px; font-size: .9rem; font-weight: 900; }
.robot-message span { color: var(--forest-soft); font-size: .72rem; font-weight: 900; text-transform: uppercase; letter-spacing: .06em; }
.robot-message p { margin: 7px 0 0; color: var(--forest-dark); font-size: 1.04rem; font-weight: 700; }
.console-button { width: 100%; }
.technology { background: #1f4d3b; color: white; }
.split-heading.light > p { color: rgba(255,255,255,.68); }
.architecture { padding: 38px; display: grid; grid-template-columns: 1fr .65fr 1.2fr .65fr 1fr .65fr 1fr; align-items: center; gap: 8px; background: rgba(255,255,255,.07); border: 1px solid rgba(255,255,255,.13); border-radius: 30px; }
.architecture-node { min-height: 145px; padding: 18px; display: flex; flex-direction: column; align-items: center; justify-content: center; background: white; border-radius: 22px; color: var(--forest-dark); text-align: center; }
.architecture-node strong { margin-top: 8px; font-size: .92rem; }
.architecture-node span { color: var(--muted); font-size: .7rem; }
.node-icon { width: 48px; height: 48px; display: grid; place-items: center; background: var(--mint); border-radius: 15px; font-size: 1.3rem; }
.main-node { background: var(--yellow); transform: scale(1.05); }
.pi-board { position: relative; width: 73px; height: 53px; display: grid; place-items: center; background: var(--forest); border-radius: 9px; color: white; box-shadow: inset 0 0 0 3px rgba(255,255,255,.14); }
.pi-board i { position: absolute; width: 7px; height: 7px; background: var(--yellow); border-radius: 50%; }.pi-board i:nth-child(1){left:8px;top:8px}.pi-board i:nth-child(2){right:8px;top:8px}.pi-board i:nth-child(3){left:8px;bottom:8px}.pi-board i:nth-child(4){right:8px;bottom:8px}
.pi-board span { color: white; font-size: .7rem; font-weight: 900; }
.architecture-line { text-align: center; color: rgba(255,255,255,.6); }
.architecture-line i { position: relative; display: block; height: 2px; background: rgba(255,255,255,.3); }
.architecture-line i::after { content: ""; position: absolute; right: -1px; top: -4px; border-left: 7px solid var(--yellow); border-top: 5px solid transparent; border-bottom: 5px solid transparent; }
.architecture-line b { display: block; margin-top: 7px; font-size: .62rem; text-transform: uppercase; letter-spacing: .08em; }
.output-stack { display: grid; gap: 8px; }
.small-node { min-height: 68px; flex-direction: row; gap: 10px; padding: 10px; }
.small-node .node-icon { width: 35px; height: 35px; border-radius: 10px; font-size: .95rem; }
.small-node strong { margin: 0; }
.tech-bottom { margin-top: 25px; display: grid; grid-template-columns: 1.3fr .7fr; gap: 22px; }
.status-panel, .battery-card { padding: 34px; background: white; border-radius: 26px; color: var(--ink); }
.panel-label { color: var(--orange-dark); font-size: .72rem; font-weight: 900; letter-spacing: .09em; text-transform: uppercase; }
.status-panel h3 { margin: 7px 0 23px; color: var(--forest); font-size: 1.45rem; }
.check-list { margin: 0; padding: 0; display: grid; grid-template-columns: 1fr 1fr; gap: 11px; list-style: none; }
.check-list li { display: flex; align-items: center; gap: 9px; color: var(--muted); font-size: .88rem; font-weight: 750; }
.check-list i { width: 25px; height: 25px; display: grid; place-items: center; background: var(--mint); border-radius: 50%; color: var(--forest); font-style: normal; }
.battery-card { background: var(--yellow); }
.battery-card svg { width: 170px; margin: -10px auto 8px; }
.battery-card svg rect { fill: none; stroke: var(--forest); stroke-width: 8px; }.battery-card svg .charge { fill: var(--forest); stroke: none; }.battery-card svg path { fill: var(--yellow); }
.battery-card strong { display: block; color: var(--forest); font-size: 1.2rem; }.battery-card p { margin: 7px 0 0; color: #5f573e; font-size: .88rem; }
.innovation-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 18px; }
.innovation-card { position: relative; min-height: 305px; padding: 28px; display: flex; flex-direction: column; justify-content: flex-end; border: 1px solid var(--line); border-radius: 28px; background: white; overflow: hidden; }
.innovation-card::before { content: ""; position: absolute; width: 170px; height: 170px; top: -70px; right: -60px; background: var(--mint); border-radius: 50%; }
.innovation-card:nth-child(3)::before { background: #f0e4d7; }.innovation-card:nth-child(4)::before { background: #fff1d6; }
.innovation-card.featured { background: var(--orange); border-color: var(--orange); color: white; transform: translateY(-14px); box-shadow: 0 25px 65px rgba(239,135,52,.23); }
.innovation-card.featured::before { background: rgba(255,255,255,.14); }
.feature-tag { position: absolute; left: 24px; top: 22px; padding: 6px 10px; background: rgba(255,255,255,.18); border-radius: 999px; font-size: .65rem; font-weight: 900; text-transform: uppercase; }
.big-letter { position: absolute; top: 1px; right: 25px; color: rgba(31,77,59,.13); font-size: 7.5rem; line-height: 1; font-weight: 950; }
.featured .big-letter { color: rgba(255,255,255,.14); }
.innovation-card h3 { position: relative; margin: 0 0 7px; color: var(--forest); font-size: 1.3rem; }.innovation-card p { position: relative; margin: 0; color: var(--muted); font-size: .9rem; }
.featured h3, .featured p { color: white; }
.impact { background: #f5f1e8; }
.impact-grid { display: grid; grid-template-columns: 1.05fr .95fr; align-items: center; gap: 75px; }
.impact-visual { min-height: 560px; position: relative; padding: 45px; background: linear-gradient(150deg, #dff4ed, #fbf3da); border-radius: 42px; overflow: hidden; }
.museum-scene { position: relative; height: 390px; display: flex; flex-direction: column; align-items: center; justify-content: center; }
.museum-roof { width: 78%; height: 55px; background: var(--forest); clip-path: polygon(50% 0,100% 100%,0 100%); }
.museum-name { width: 72%; padding: 10px; background: var(--brown); color: white; text-align: center; font-size: .7rem; letter-spacing: .4em; font-weight: 900; }
.columns { width: 66%; height: 155px; display: flex; justify-content: space-between; padding: 12px 20px; background: rgba(255,255,255,.75); }
.columns i { width: 18%; background: repeating-linear-gradient(90deg,#d8c7a8 0 7px,#eadcc2 7px 14px); border-radius: 4px 4px 0 0; }
.museum-base { width: 76%; height: 32px; background: var(--brown); border-radius: 3px; }
.path { position: absolute; width: 260px; height: 150px; bottom: -72px; background: rgba(255,255,255,.55); clip-path: polygon(38% 0,62% 0,100% 100%,0 100%); }
.slothy-pin, .school-pin { position: absolute; z-index: 2; width: 66px; height: 66px; display: grid; place-items: center; border: 6px solid white; border-radius: 50% 50% 50% 0; transform: rotate(-45deg); box-shadow: 0 10px 25px rgba(35,70,52,.15); }
.slothy-pin span, .school-pin span { transform: rotate(45deg); font-size: .72rem; font-weight: 900; }
.slothy-pin { left: 15%; bottom: 56px; background: var(--orange); color: white; }.school-pin { right: 12%; bottom: 20px; background: var(--teal); color: var(--forest); }
.impact-quote { position: relative; z-index: 4; margin-top: 18px; padding: 19px 22px; background: white; border-radius: 17px; color: var(--forest); font-weight: 850; box-shadow: 0 17px 40px rgba(31,77,59,.1); }
.impact-copy > p { color: var(--muted); font-size: 1.05rem; }
.impact-list { margin-top: 30px; display: grid; gap: 12px; }
.impact-list div { display: grid; grid-template-columns: 39px 1fr; align-items: start; gap: 15px; }
.impact-list span { width: 39px; height: 39px; display: grid; place-items: center; background: var(--forest); color: var(--yellow); border-radius: 12px; font-size: .72rem; font-weight: 900; }
.impact-list p { margin: 4px 0 0; color: var(--muted); }.impact-list strong { color: var(--forest); }
.timeline { position: relative; display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; }
.timeline::before { content: ""; position: absolute; left: 7%; right: 7%; top: 26px; height: 2px; background: var(--line); }
.timeline-item { position: relative; padding-top: 62px; }
.timeline-item > span { position: absolute; z-index: 2; top: 0; left: 0; width: 52px; height: 52px; display: grid; place-items: center; background: var(--forest); border: 7px solid var(--paper); border-radius: 50%; color: var(--yellow); font-weight: 900; box-shadow: 0 0 0 2px var(--forest); }
.timeline-item h3 { margin: 0 0 8px; color: var(--forest); font-size: 1.08rem; }.timeline-item p { margin: 0; color: var(--muted); font-size: .87rem; }
.validation { padding-top: 0; }
.validation-card { padding: 45px; display: grid; grid-template-columns: 1.15fr .85fr; gap: 55px; align-items: center; background: var(--yellow); border-radius: 32px; }
.validation-card h2 { font-size: clamp(2rem, 3.5vw, 3.3rem); }.validation-card p { color: #625c48; }
.validation-next { padding: 25px; background: rgba(255,255,255,.65); border-radius: 21px; }
.validation-next span { color: var(--orange-dark); font-size: .7rem; font-weight: 900; text-transform: uppercase; letter-spacing: .09em; }
.validation-next ol { margin: 15px 0 0; padding-left: 21px; color: var(--forest); font-weight: 800; }
.validation-next li { padding: 5px 0; }
.viability { background: #eff6f2; }
.viability-steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
.viability-steps article { min-height: 260px; padding: 30px; background: white; border-radius: 25px; border-top: 5px solid var(--orange); box-shadow: 0 15px 40px rgba(31,77,59,.07); }
.viability-steps article:nth-child(2){border-color:var(--teal)}.viability-steps article:nth-child(3){border-color:var(--brown)}
.viability-steps span { color: var(--orange-dark); font-size: .72rem; font-weight: 900; letter-spacing: .08em; text-transform: uppercase; }
.viability-steps h3 { margin: 28px 0 8px; color: var(--forest); font-size: 1.35rem; }.viability-steps p { color: var(--muted); }.viability-steps i { display: block; margin-top: 22px; color: var(--forest-soft); font-size: .78rem; font-style: normal; font-weight: 850; }
.resource-strip { margin-top: 22px; padding: 20px; display: flex; flex-wrap: wrap; align-items: center; gap: 10px; background: var(--forest); border-radius: 20px; color: white; }
.resource-strip strong { margin-right: 5px; color: var(--yellow); }.resource-strip span { padding: 6px 10px; background: rgba(255,255,255,.09); border-radius: 999px; font-size: .75rem; }
.team-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
.team-card { padding: 34px; text-align: center; background: white; border: 1px solid var(--line); border-radius: 28px; transition: .25s ease; }
.team-card:hover { transform: translateY(-6px); box-shadow: var(--shadow); }
.avatar { width: 110px; height: 110px; margin: 0 auto 23px; display: grid; place-items: center; border-radius: 42% 58% 50% 50%; background: var(--mint); color: var(--forest); font-size: 1.5rem; font-weight: 950; transform: rotate(-4deg); }
.avatar span { transform: rotate(4deg); }.avatar-two { background: #fff0d7; color: var(--orange-dark); transform: rotate(5deg); }.avatar-two span { transform: rotate(-5deg); }.avatar-three { background: #efe5dc; color: var(--brown); }
.team-card h3 { margin: 0 0 9px; color: var(--forest); line-height: 1.2; }.team-card p { min-height: 52px; margin: 0; color: var(--muted); font-size: .9rem; }
.skill-tags { margin-top: 20px; display: flex; justify-content: center; flex-wrap: wrap; gap: 7px; }.skill-tags span { padding: 6px 10px; background: #f2f5f3; border-radius: 999px; color: var(--forest-soft); font-size: .68rem; font-weight: 850; }
.teamwork-note { margin-top: 22px; padding: 23px 28px; display: flex; align-items: center; gap: 17px; background: var(--mint); border-radius: 20px; }
.teamwork-note > span { width: 45px; height: 45px; flex: 0 0 auto; display: grid; place-items: center; background: var(--forest); border-radius: 14px; color: var(--yellow); font-size: 1.3rem; }.teamwork-note p { margin: 0; color: var(--forest-soft); }.teamwork-note strong { color: var(--forest); }
.judges { background: var(--forest-dark); }
.judges-card { display: grid; grid-template-columns: .9fr 1.1fr; gap: 60px; align-items: center; }
.judges-card h2 { color: white; }.judges-copy > p { color: rgba(255,255,255,.67); }.light-button { margin-top: 20px; background: var(--yellow); color: var(--forest-dark); }
.judge-checks { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
.judge-checks > div { padding: 17px; display: grid; grid-template-columns: 35px 1fr; gap: 12px; background: rgba(255,255,255,.07); border: 1px solid rgba(255,255,255,.11); border-radius: 16px; }
.judge-checks i { width: 35px; height: 35px; display: grid; place-items: center; background: var(--yellow); color: var(--forest); border-radius: 50%; font-style: normal; font-weight: 900; }
.judge-checks strong, .judge-checks span { display: block; }.judge-checks strong { color: white; font-size: .84rem; }.judge-checks span { color: rgba(255,255,255,.56); font-size: .72rem; }
.qr-section { background: #f8efe2; }
.qr-card { padding: 55px; display: grid; grid-template-columns: 1fr auto; align-items: center; gap: 70px; background: white; border-radius: 34px; box-shadow: var(--shadow); }
.qr-copy { max-width: 630px; }.qr-copy p { color: var(--muted); }
.url-box { margin-top: 24px; padding: 8px 8px 8px 15px; display: flex; align-items: center; gap: 12px; background: #f1f5f2; border-radius: 13px; }
.url-box span { flex: 1; color: var(--forest); font-size: .8rem; overflow: hidden; white-space: nowrap; text-overflow: ellipsis; }
.url-box button { padding: 8px 12px; border: 0; border-radius: 9px; background: var(--forest); color: white; cursor: pointer; font-weight: 800; font-size: .75rem; }
.qr-box { padding: 16px; background: var(--cream); border: 1px solid var(--line); border-radius: 24px; text-align: center; }
#qr-code { width: 230px; height: 230px; display: grid; place-items: center; background: white; border-radius: 14px; overflow: hidden; }
#qr-code canvas { width: 100%; height: 100%; }
.qr-box > span { display: block; margin-top: 10px; color: var(--forest-soft); font-size: .72rem; font-weight: 850; }
.footer { padding: 60px 0 28px; background: #15291f; color: white; }
.footer-grid { display: grid; grid-template-columns: 1.5fr .7fr .7fr; gap: 45px; align-items: start; }
.footer-grid span, .footer-grid strong { display: block; }.footer-grid span { color: rgba(255,255,255,.5); font-size: .75rem; }.footer-grid strong { margin-top: 4px; color: white; }
.footer-brand strong { color: var(--yellow); font-size: 1.7rem; }.footer-brand span { max-width: 340px; margin-top: 7px; font-size: .86rem; }
.footer-bottom { margin-top: 45px; padding-top: 21px; display: flex; justify-content: space-between; border-top: 1px solid rgba(255,255,255,.1); color: rgba(255,255,255,.45); font-size: .75rem; }.footer-bottom p { margin: 0; }.footer-bottom a { color: var(--yellow); text-decoration: none; font-weight: 800; }
.reveal { opacity: 0; transform: translateY(24px); transition: opacity .7s ease, transform .7s ease; }
.reveal.visible { opacity: 1; transform: translateY(0); }
.presentation-toast { position: fixed; z-index: 2000; left: 50%; bottom: 25px; transform: translate(-50%, 130%); padding: 12px 18px; background: var(--ink); color: white; border-radius: 999px; box-shadow: var(--shadow); font-size: .78rem; transition: transform .35s ease; }
.presentation-toast.show { transform: translate(-50%, 0); }
body.presentation .site-header, body.presentation .judge-bar { display: none; }
body.presentation .hero { padding-top: 75px; min-height: 100vh; }
body.presentation { cursor: none; }
@keyframes float { 0%,100%{transform:translateY(0)}50%{transform:translateY(-11px)} }
@keyframes orbit { to { transform: rotate(360deg); } }
@keyframes wave-left { 0%,100%{transform:rotate(0)}35%,55%{transform:rotate(-8deg)} }
@keyframes wave-right { 0%,100%{transform:rotate(0)}35%,55%{transform:rotate(8deg)} }
@keyframes pulse-wave { 0%,100%{opacity:.35;transform:scale(.92)}50%{opacity:1;transform:scale(1.04)} }
@keyframes sparkle { 0%,100%{opacity:.5;transform:scale(.9)}50%{opacity:1;transform:scale(1.05)} }
@media (max-width: 1050px) {
  .nav-links { gap: 17px; }.nav-links a { font-size: .82rem; }
  .hero-grid { gap: 30px; }.hero h1 { font-size: clamp(3.2rem, 6vw, 5rem); }
  .floating-note { display: none; }
  .flow-grid { grid-template-columns: 1fr 1fr; }.flow-arrow { display: none; }
  .architecture { grid-template-columns: 1fr .45fr 1fr .45fr 1fr; }.architecture > :nth-child(6), .architecture > :nth-child(7) { display: none; }
  .innovation-grid { grid-template-columns: 1fr 1fr; }.innovation-card.featured { transform: none; }
}
@media (max-width: 820px) {
  :root { --container: min(100% - 28px, 680px); }
  .site-header { background: rgba(255,253,248,.96); }
  .menu-toggle { display: block; }
  .nav-links { position: absolute; inset: 78px 14px auto; padding: 18px; display: none; flex-direction: column; align-items: stretch; gap: 0; background: white; border: 1px solid var(--line); border-radius: 18px; box-shadow: var(--shadow); }
  .nav-links.open { display: flex; }.nav-links a { padding: 11px; }.nav-links .nav-cta { margin-top: 7px; text-align: center; }
  .hero { min-height: auto; padding-top: 125px; }.hero-grid { grid-template-columns: 1fr; }.hero-visual { min-height: 520px; }.robot-card { max-width: 440px; }.orbit-one { width: 520px; height: 520px; }
  .judge-bar { margin-top: 0; }.judge-bar-grid { grid-template-columns: 1fr 1fr; }.judge-bar p:nth-child(2){border-right:0}.judge-bar p { border-bottom: 1px solid rgba(255,255,255,.14); }
  .section { padding: 90px 0; }.split-heading { grid-template-columns: 1fr; gap: 15px; }.challenge-grid { grid-template-columns: 1fr; }.challenge-card { min-height: auto; }
  .learning-grid, .impact-grid, .judges-card, .validation-card { grid-template-columns: 1fr; gap: 45px; }.demo-console { max-width: 650px; width: 100%; }
  .architecture { grid-template-columns: 1fr; gap: 10px; }.architecture-line { height: 37px; }.architecture-line i { width: 2px; height: 28px; margin: 0 auto; }.architecture-line i::after { left: -4px; right: auto; top: auto; bottom: -1px; border-left: 5px solid transparent; border-right: 5px solid transparent; border-top: 7px solid var(--yellow); border-bottom: 0; }.architecture-line b { display: none; }.architecture > :nth-child(6), .architecture > :nth-child(7){display:block}.output-stack { grid-template-columns: 1fr 1fr; }.main-node { transform:none; }
  .tech-bottom { grid-template-columns: 1fr; }.timeline { grid-template-columns: 1fr 1fr; }.timeline::before { display: none; }
  .viability-steps, .team-grid { grid-template-columns: 1fr; }.team-card p { min-height: auto; }.qr-card { grid-template-columns: 1fr; gap: 35px; }.qr-box { justify-self: center; }.footer-grid { grid-template-columns: 1fr 1fr; }.footer-brand { grid-column: 1 / 3; }
}
@media (max-width: 560px) {
  .hero h1 { font-size: 3.15rem; }.hero-proof { gap: 14px; }.hero-proof div { grid-template-columns: 1fr; gap: 3px; }.hero-proof span { max-width: none; }.hero-visual { min-height: 430px; }.robot-card { padding: 5px; }.orbit-one { width: 430px; height: 430px; }.orbit-two { width: 340px; height: 340px; }
  .judge-bar-grid { grid-template-columns: 1fr; }.judge-bar p { border-right: 0; }
  .goal-banner { align-items: flex-start; padding: 23px; }.flow-grid, .innovation-grid, .judge-checks { grid-template-columns: 1fr; }
  .mode-tabs { grid-template-columns: 1fr; }.mode-tab span { display: inline; margin-right: 5px; }.console-body { padding: 20px; }.robot-message { grid-template-columns: 1fr; }.mini-sloth { width: 50px; height: 50px; }
  .check-list { grid-template-columns: 1fr; }.impact-visual { min-height: 460px; padding: 24px; }.museum-scene { height: 330px; }.timeline { grid-template-columns: 1fr; }
  .validation-card, .qr-card { padding: 28px; }.teamwork-note { align-items: flex-start; }.qr-box { width: 100%; }.qr-box #qr-code { width: min(230px, 100%); height: auto; aspect-ratio: 1; margin: auto; }.footer-grid { grid-template-columns: 1fr; }.footer-brand { grid-column: auto; }.footer-bottom { flex-direction: column; gap: 12px; }
}
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after { scroll-behavior: auto !important; animation-duration: .01ms !important; animation-iteration-count: 1 !important; transition-duration: .01ms !important; }
  .reveal { opacity: 1; transform: none; }
}
@media print {
  .site-header, .hero-actions, .console-button, .qr-section, .footer, .presentation-toast { display: none !important; }
  body { background: white; color: black; }.hero, .section, .learning, .technology, .judges { background: white !important; color: black !important; padding: 40px 0; }.section h2, .hero h1, .learning h2, .technology h2, .judges h2 { color: #15392b !important; }.reveal { opacity: 1 !important; transform: none !important; }.judge-bar { margin: 0; }.judge-bar-grid { box-shadow: none; }
}
</style>
