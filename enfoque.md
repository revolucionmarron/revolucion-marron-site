---
layout: default
title: Enfoque - Arquitectura Productiva Regenerativa
description: Los productores que rediseñan hoy tienen ventaja competitiva de 3-5 años
---

<style>
/* Hero Section */
.enfoque-hero {
  position: relative;
  background: linear-gradient(rgba(30, 20, 12, 0.85), rgba(30, 20, 12, 0.85)),
              url('{{ '/assets/images/enfoque-hero-cerdos-huerto.png' | relative_url }}');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  color: white;
  padding: 140px 40px 100px;
  text-align: center;
  border-radius: 16px;
  margin-bottom: 80px;
  box-shadow: var(--shadow-xl);
  min-height: 85vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.enfoque-hero-content {
  position: relative;
  z-index: 2;
  max-width: 900px;
}

.enfoque-hero h1 {
  font-size: clamp(36px, 5vw, 56px);
  margin-bottom: 28px;
  color: white;
  text-shadow: 0 4px 16px rgba(0,0,0,0.8);
  font-weight: 700;
}

.enfoque-hero p {
  font-size: clamp(17px, 2vw, 22px);
  line-height: 1.7;
  max-width: 850px;
  margin: 0 auto 24px;
  color: rgba(255,255,255,0.98);
  text-shadow: 0 3px 12px rgba(0,0,0,0.7);
  font-weight: 500;
}

.enfoque-hero .highlight-question {
  font-size: clamp(20px, 2.8vw, 28px);
  font-weight: 800;
  color: #8bc34a;
  margin-top: 36px;
  font-style: italic;
  text-shadow: 0 3px 16px rgba(0,0,0,0.9);
  background: rgba(0,0,0,0.3);
  padding: 16px 24px;
  border-radius: 8px;
  display: inline-block;
}

/* Secciones con fondo */
.section-white {
  background: white;
  padding: 80px 40px;
  margin-bottom: 0;
}

.section-sand {
  background: var(--sand);
  padding: 80px 40px;
  margin-bottom: 0;
}

.section-dark {
  background: var(--soil);
  color: white;
  padding: 80px 40px;
  margin-bottom: 0;
}

.section-title {
  font-size: clamp(32px, 4vw, 48px);
  text-align: center;
  margin-bottom: 24px;
  color: var(--soil-dark);
}

.section-dark .section-title {
  color: white;
}

.section-subtitle {
  font-size: clamp(16px, 2vw, 20px);
  text-align: center;
  max-width: 800px;
  margin: 0 auto 60px;
  color: var(--text-light);
  line-height: 1.7;
}

.section-dark .section-subtitle {
  color: rgba(255,255,255,0.9);
}

/* Stats Grid - Oportunidad */
.problema-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto;
}

.problema-card {
  background: white;
  border: 2px solid rgba(107, 68, 35, 0.1);
  border-radius: 16px;
  padding: 40px 32px;
  box-shadow: var(--shadow-md);
  transition: all var(--transition-normal);
}

.problema-card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-xl);
  border-color: var(--accent-green);
}

.problema-card h3 {
  font-size: 24px;
  color: var(--soil-dark);
  margin-bottom: 20px;
  padding-bottom: 16px;
  border-bottom: 3px solid var(--accent-green);
}

.problema-card .stat-highlight {
  font-size: 42px;
  font-weight: 700;
  color: var(--accent-green);
  margin: 20px 0 12px;
  line-height: 1;
}

.problema-card p {
  font-size: 16px;
  line-height: 1.7;
  color: var(--text-light);
  margin-bottom: 16px;
}

/* Tabla Comparativa */
.comparison-container {
  max-width: 1000px;
  margin: 0 auto;
}

.comparison-table {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  margin-bottom: 40px;
}

.comparison-column {
  background: white;
  border-radius: 16px;
  padding: 40px 32px;
  box-shadow: var(--shadow-md);
}

.comparison-column.conventional {
  border-left: 5px solid #c44536;
}

.comparison-column.regenerative {
  border-left: 5px solid var(--accent-green);
  background: linear-gradient(135deg, white 0%, var(--sand-light) 100%);
}

.comparison-column h3 {
  font-size: 26px;
  margin-bottom: 24px;
  text-align: center;
}

.comparison-column.conventional h3 {
  color: #c44536;
}

.comparison-column.regenerative h3 {
  color: var(--accent-green);
}

.comparison-column ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.comparison-column li {
  padding: 14px 0 14px 32px;
  margin-bottom: 12px;
  position: relative;
  font-size: 16px;
  line-height: 1.6;
  color: var(--text-light);
}

.comparison-column.conventional li:before {
  content: "✕";
  position: absolute;
  left: 0;
  color: #c44536;
  font-size: 20px;
  font-weight: 700;
}

.comparison-column.regenerative li:before {
  content: "✓";
  position: absolute;
  left: 0;
  color: var(--accent-green);
  font-size: 20px;
  font-weight: 700;
}

/* Principle Box */
.principle-box {
  background: linear-gradient(135deg, var(--soil) 0%, var(--soil-dark) 100%);
  color: white;
  padding: 40px 50px;
  border-radius: 16px;
  text-align: center;
  box-shadow: var(--shadow-xl);
  max-width: 900px;
  margin: 0 auto;
}

.principle-box p {
  font-size: clamp(20px, 3vw, 28px);
  font-weight: 700;
  margin: 0;
  line-height: 1.5;
  font-style: italic;
  color: white;
}

/* Pilares Grid */
.pilares-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 32px;
  max-width: 1200px;
  margin: 0 auto;
}

.pilar-card-enfoque {
  background: white;
  border: 2px solid rgba(107, 68, 35, 0.1);
  border-radius: 16px;
  padding: 36px 28px;
  box-shadow: var(--shadow-md);
  transition: all var(--transition-normal);
  position: relative;
  overflow: hidden;
}

.pilar-card-enfoque:hover {
  transform: translateY(-6px);
  box-shadow: var(--shadow-xl);
  border-color: var(--accent-green);
}

.pilar-card-enfoque:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 6px;
  height: 100%;
  background: linear-gradient(180deg, var(--accent-green) 0%, #5a7a1e 100%);
}

.pilar-number {
  width: 56px;
  height: 56px;
  background: linear-gradient(135deg, var(--accent-green) 0%, #5a7a1e 100%);
  color: white;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 28px;
  font-weight: 700;
  margin-bottom: 20px;
  box-shadow: var(--shadow-md);
}

.pilar-card-enfoque h3 {
  font-size: 22px;
  color: var(--soil-dark);
  margin-bottom: 16px;
  line-height: 1.3;
}

.pilar-card-enfoque p {
  font-size: 16px;
  line-height: 1.7;
  color: var(--text-light);
  margin-bottom: 16px;
}

.pilar-card-enfoque h4 {
  font-size: 18px;
  color: var(--soil);
  margin: 24px 0 16px;
  font-weight: 700;
}

.pilar-card-enfoque strong {
  color: var(--soil-dark);
}

.pilar-card-enfoque.destacado {
  grid-column: span 2;
  background: linear-gradient(135deg, white 0%, var(--sand-light) 100%);
}

/* Ciclos Grid */
.ciclos-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 20px;
  margin: 24px 0;
}

.ciclo-item {
  background: rgba(107, 142, 35, 0.08);
  border-left: 4px solid var(--accent-green);
  padding: 20px;
  border-radius: 8px;
}

.ciclo-item strong {
  display: block;
  font-size: 16px;
  color: var(--accent-green);
  margin-bottom: 8px;
  font-weight: 700;
}

.ciclo-item p {
  margin: 0;
  font-size: 14px;
  line-height: 1.6;
  color: var(--text-light);
}

/* Beneficios Grid */
.beneficios-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 32px;
  max-width: 1200px;
  margin: 0 auto;
}

.beneficio-card {
  background: rgba(255,255,255,0.1);
  border: 2px solid rgba(255,255,255,0.2);
  border-radius: 16px;
  padding: 36px 28px;
  transition: all var(--transition-normal);
}

.beneficio-card:hover {
  background: rgba(255,255,255,0.15);
  transform: translateY(-4px);
  box-shadow: 0 12px 32px rgba(0,0,0,0.3);
}

.beneficio-number {
  font-size: clamp(36px, 4vw, 48px);
  font-weight: 700;
  color: white;
  margin-bottom: 8px;
  line-height: 1;
}

.beneficio-label {
  font-size: 18px;
  font-weight: 700;
  color: rgba(255,255,255,0.95);
  margin-bottom: 16px;
  line-height: 1.3;
}

.beneficio-card p {
  font-size: 15px;
  line-height: 1.7;
  color: rgba(255,255,255,0.90);
  margin: 0;
}

.beneficio-card ul {
  list-style: none;
  padding: 0;
  margin: 12px 0 0 0;
}

.beneficio-card li {
  padding: 6px 0 6px 20px;
  position: relative;
  font-size: 14px;
  color: rgba(255,255,255,0.85);
}

.beneficio-card li:before {
  content: "•";
  position: absolute;
  left: 0;
  color: var(--accent-green);
  font-size: 20px;
}

/* CTA Section */
.cta-section {
  max-width: 800px;
  margin: 0 auto;
}

.cta-box {
  background: white;
  border: 3px solid var(--accent-green);
  border-radius: 16px;
  padding: 50px 40px;
  text-align: center;
  box-shadow: var(--shadow-xl);
  margin-bottom: 40px;
}

.cta-box p {
  font-size: 20px;
  line-height: 1.7;
  color: var(--soil-dark);
  margin-bottom: 24px;
}

.cta-box p:last-of-type {
  margin-bottom: 0;
}

.cta-box .button {
  display: inline-block;
  background: linear-gradient(135deg, var(--accent-green) 0%, #5a7a1e 100%);
  color: white;
  padding: 16px 40px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 18px;
  transition: all var(--transition-normal);
  box-shadow: var(--shadow-md);
}

.cta-box .button:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-xl);
}

.contact-options {
  background: rgba(107, 68, 35, 0.05);
  border-radius: 12px;
  padding: 32px;
  text-align: center;
}

.contact-options p {
  font-size: 18px;
  color: var(--soil);
  margin-bottom: 16px;
  font-weight: 600;
}

.contact-options ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.contact-options li {
  margin: 12px 0;
  font-size: 16px;
}

.contact-options a {
  color: var(--accent-green);
  text-decoration: none;
  font-weight: 600;
  transition: all var(--transition-normal);
}

.contact-options a:hover {
  color: var(--soil-dark);
  text-decoration: underline;
}

/* Responsive */
@media (max-width: 768px) {
  .enfoque-hero {
    background-attachment: scroll !important;
    padding: 100px 24px 80px !important;
    min-height: 70vh !important;
  }
  
  .comparison-table {
    grid-template-columns: 1fr;
    gap: 24px;
  }
  
  .pilar-card-enfoque.destacado {
    grid-column: span 1;
  }
  
  .ciclos-grid {
    grid-template-columns: 1fr;
  }
  
  .section-white, .section-sand, .section-dark {
    padding: 60px 24px;
  }
}

@media (max-width: 480px) {
  .enfoque-hero {
    padding: 80px 20px 60px !important;
    min-height: 60vh !important;
  }
}
</style>

<!-- Hero Section -->
<div class="enfoque-hero">
  <div class="enfoque-hero-content">
    <h1>Arquitectura Productiva Regenerativa</h1>
    <p>
      Think tank técnico que rediseña sistemas silvoagropecuarios para <strong>maximizar rentabilidad</strong> usando la biología del suelo como herramienta productiva.
    </p>
    <p class="highlight-question">
      "¿Por qué los productores siguen usando un modelo que los empobrece?"
    </p>
  </div>
</div>

<!-- Sección Por Qué Cambiar -->
<div class="section-white">
  <h2 class="section-title">Por qué cambiar ahora</h2>
  <p class="section-subtitle">
    Ventaja competitiva de 3-5 años para quienes rediseñan hoy. Esto es economía básica, no ideología.
  </p>
  
  <div class="problema-grid">
    
    <div class="problema-card">
      <h3>Suelos: activo productivo</h3>
      <div class="stat-highlight">78%</div>
      <p><strong>Márgenes brutos 78% mayores</strong> que vecinos convencionales. La diferencia está en producir con menos costo, no en producir más.</p>
      <p>Suelos regenerados recuperan capacidad productiva en 3-5 años. Conviertes un pasivo en tu activo más valioso.</p>
    </div>
    
    <div class="problema-card">
      <h3>Independencia de insumos</h3>
      <div class="stat-highlight">30-50%</div>
      <p><strong>Ahorros de 30-50% en costos directos</strong>, inmediatamente traducibles a mayor margen.</p>
      <p>La pregunta no es si los insumos seguirán subiendo. Es: <strong>¿cuánto dejas de depender del dólar cada temporada?</strong></p>
    </div>
    
    <div class="problema-card">
      <h3>Márgenes superiores</h3>
      <div class="stat-highlight">+78%</div>
      <p>Reducir costos 30-50% + mantener precio de venta = <strong>margen multiplicado</strong>. Matemática simple.</p>
      <p>Ventana de oportunidad abierta: <strong>quienes rediseñan primero capturan prima de precio</strong> antes que se sature oferta.</p>
    </div>
    
  </div>
</div>

<!-- Sección Solución -->
<div class="section-sand">
  <h2 class="section-title">Qué es APR</h2>
  <p class="section-subtitle">
    Diseño integral del sistema: qué produces, dónde, cómo, cuándo, con qué recursos. Calculado para maximizar rentabilidad usando biología del suelo.
  </p>
  
  <div class="comparison-container">
    <div class="comparison-table">
      
      <div class="comparison-column conventional">
        <h3>Modelo Convencional</h3>
        <ul>
          <li>Monocultivo</li>
          <li>Dependencia insumos sintéticos</li>
          <li>Labranza intensiva</li>
          <li>Costos crecientes</li>
          <li>Degradación del activo</li>
          <li>Vulnerabilidad climática</li>
        </ul>
      </div>
      
      <div class="comparison-column regenerative">
        <h3>APR</h3>
        <ul>
          <li>Diversidad funcional</li>
          <li>Producción propia fertilidad</li>
          <li>Mínima perturbación</li>
          <li>-30-50% costos insumos</li>
          <li>Regeneración del activo</li>
          <li>Resiliencia climática</li>
        </ul>
      </div>
      
    </div>
    
    <div class="principle-box">
      <p>No es "ser regenerativo". Es reducir costos y aumentar margen.</p>
    </div>
  </div>
</div>

<!-- Sección 5 Pilares -->
<div class="section-white">
  <h2 class="section-title">Los 5 pilares</h2>
  
  <div class="pilares-grid">
    
    <div class="pilar-card-enfoque">
      <div class="pilar-number">1</div>
      <h3>Análisis económico primero</h3>
      <p>Identificamos dónde se va tu dinero. <strong>70-80% de costos</strong> en 3-5 rubros: fertilizantes, pesticidas, combustible, agua, mano de obra.</p>
      <p><strong>Comenzamos con tu balance, no con el suelo.</strong></p>
    </div>
    
    <div class="pilar-card-enfoque destacado">
      <div class="pilar-number">2</div>
      <h3>Herramientas de la naturaleza</h3>
      <p>Hongos micorrízicos, bacterias fijadoras, fauna del suelo, animales integrados. <strong>Insumos productivos</strong> que reemplazan fertilizantes y pesticidas.</p>
      
      <h4>Animales: pieza fundamental</h4>
      
      <div class="ciclos-grid">
        <div class="ciclo-item">
          <strong>Ciclo agua</strong>
          <p>Pastoreo rotativo aumenta infiltración. Pezuñas rompen costras.</p>
        </div>
        
        <div class="ciclo-item">
          <strong>Ciclo nutrientes</strong>
          <p>Concentran nutrientes dispersos y los devuelven vía estiércol/orina.</p>
        </div>
        
        <div class="ciclo-item">
          <strong>Ciclo minerales</strong>
          <p>N, P, K, micronutrientes sin costo de insumo.</p>
        </div>
        
        <div class="ciclo-item">
          <strong>Ciclo energía</strong>
          <p>Convierten energía solar en proteína, estimulan rebrote.</p>
        </div>
      </div>
      
      <p><strong>Procesos biológicos medibles y replicables.</strong></p>
    </div>
    
    <div class="pilar-card-enfoque">
      <div class="pilar-number">3</div>
      <h3>Diseño sistema completo</h3>
      <p><strong>Rediseño integral:</strong> agua (Keyline), energía (fotosíntesis), nutrientes (ciclos cerrados), animales (pastoreo rotativo).</p>
      <p>Cada elemento cumple múltiples funciones. El sistema genera servicios que antes comprabas.</p>
    </div>
    
    <div class="pilar-card-enfoque">
      <div class="pilar-number">4</div>
      <h3>Datos y medición</h3>
      <p><strong>Si no se mide, no se mejora.</strong></p>
      <p>Indicadores: carbono orgánico, infiltración, biomasa, estructura costos, margen operacional.</p>
      <p>Medición cada 6-12 meses.</p>
    </div>
    
    <div class="pilar-card-enfoque">
      <div class="pilar-number">5</div>
      <h3>Transición rentable</h3>
      <p><strong>No quebrar mientras regeneras.</strong></p>
      <p>Transición 1-3 años. Flujo caja mensual, timing inversiones, horizonte 36 meses.</p>
      <p>Cambios <strong>alto impacto, bajo costo</strong> primeros 12 meses.</p>
    </div>
    
  </div>
</div>

<!-- Sección Beneficios -->
<div class="section-dark">
  <h2 class="section-title">Beneficios</h2>
  <p class="section-subtitle">
    Ventajas económicas respaldadas por evidencia
  </p>
  
  <div class="beneficios-grid">
    
    <div class="beneficio-card">
      <div class="beneficio-number">30-50%</div>
      <div class="beneficio-label">Reducción costos</div>
      <p>Menor dependencia fertilizantes y pesticidas sintéticos.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number" style="font-size: 32px;">Independencia</div>
      <div class="beneficio-label">Menor volatilidad</div>
      <p>Producción propia: compost, biofertilizantes, manejo biológico.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number" style="font-size: 32px;">+Resiliencia</div>
      <div class="beneficio-label">Estabilidad climática</div>
      <p>+20.000 litros agua/ha. Resistencia sequías y eventos extremos.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number">+30%</div>
      <div class="beneficio-label">Mercados premium</div>
      <p>Certificaciones: ROC, Land to Market, Regenagri. Prima +30% proyectada 2035.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number" style="font-size: 28px;">78% mayor</div>
      <div class="beneficio-label">Rentabilidad</div>
      <p>Márgenes superiores por reducción costos, no aumento producción.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number" style="font-size: 28px;">Bonos CO₂</div>
      <div class="beneficio-label">Ingresos adicionales</div>
      <p>Mercados carbono + compensaciones servicios ecosistémicos.</p>
    </div>
    
  </div>
</div>

<!-- Sección CTA -->
<div class="section-sand">
  <h2 class="section-title">Próximos pasos</h2>
  
  <div class="cta-section">
    <div class="cta-box">
      <p><strong>Conversación 30 minutos:</strong> revisión sistema actual, dependencias críticas, oportunidades transición rentable.</p>
      <p><a href="https://calendly.com/jaime-revolucionmarron/30min" target="_blank" rel="noopener" class="button">Agendar →</a></p>
    </div>
    
    <div class="contact-options">
      <p>Otras formas de contacto:</p>
      <ul>
        <li>Email: <a href="mailto:jaime@revolucionmarron.cl">jaime@revolucionmarron.cl</a></li>
        <li>WhatsApp: <a href="https://wa.me/56948955931" target="_blank" rel="noopener">+56 9 4895 5931</a></li>
        <li>LinkedIn: <a href="https://linkedin.com/in/jaime-fernandez-l" target="_blank" rel="noopener">Jaime Fernández López</a></li>
      </ul>
    </div>
  </div>
</div>
