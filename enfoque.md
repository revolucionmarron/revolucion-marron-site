---
layout: default
title: Enfoque - Arquitectura Productiva Regenerativa
description: Los productores que rediseñan hoy tienen ventaja competitiva de 3-5 años
---

<style>
/* Hero Section */
.enfoque-hero {
  background: linear-gradient(135deg, var(--soil) 0%, var(--soil-dark) 100%);
  color: white;
  padding: 100px 40px 80px;
  text-align: center;
  border-radius: 16px;
  margin-bottom: 80px;
  box-shadow: var(--shadow-xl);
}

.enfoque-hero h1 {
  font-size: clamp(36px, 5vw, 56px);
  margin-bottom: 24px;
  color: white;
}

.enfoque-hero p {
  font-size: clamp(16px, 2vw, 20px);
  line-height: 1.8;
  max-width: 900px;
  margin: 0 auto 20px;
  color: rgba(255,255,255,0.95);
}

.enfoque-hero .highlight-question {
  font-size: clamp(18px, 2.5vw, 24px);
  font-weight: 700;
  color: var(--accent-green);
  margin-top: 32px;
  font-style: italic;
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
  
  .enfoque-hero {
    padding: 60px 24px 50px;
  }
  
  .section-white, .section-sand, .section-dark {
    padding: 60px 24px;
  }
}
</style>

<!-- Hero Section -->
<div class="enfoque-hero">
  <h1>Qué es Revolución Marrón</h1>
  <p>
    Revolución Marrón es un think tank técnico dedicado a rediseñar sistemas productivos silvoagropecuarios mediante <strong>Arquitectura Productiva Regenerativa</strong>.
  </p>
  <p>
    No somos una ONG ambiental. Somos un espacio de pensamiento y acción técnica que trabaja con productores, empresas y organizaciones que entienden que <strong>la agricultura regenerativa es una estrategia de negocio superior</strong>, no una postura ideológica.
  </p>
  <p>
    Fundado por Jaime Fernández López en 2024, nace de la experiencia directa en dirección de proyectos públicos y privados, gerencia de empresas agropecuarias, y producción certificada nacional e internacional.
  </p>
  <p class="highlight-question">
    "¿Por qué los productores siguen usando un modelo que los empobrece?"
  </p>
</div>

<!-- Sección Por Qué Cambiar -->
<div class="section-white">
  <h2 class="section-title">Por qué el modelo convencional está cambiando</h2>
  <p class="section-subtitle">
    Los productores que están rediseñando sus sistemas hoy tienen una ventaja competitiva de 3-5 años sobre quienes esperan. Esto no es ideología: es economía básica.
  </p>
  
  <div class="problema-grid">
    
    <div class="problema-card">
      <h3>Suelos: de pasivo a activo productivo</h3>
      <div class="stat-highlight">36,5M ha</div>
      <p>En Chile, <strong>36,5 millones de hectáreas tienen potencial de mejora</strong> en estructura, materia orgánica e infiltración. Esto representa la mayor oportunidad de captura de valor sin expandir superficie.</p>
      <div class="stat-highlight">78%</div>
      <p>Productores que invierten en biología del suelo están viendo <strong>márgenes brutos 78% mayores</strong> que vecinos convencionales. La diferencia no está en producir más: está en producir con menos costo.</p>
      <p>Un caso documentado en sistemas similares muestra cómo suelos regenerados pueden recuperar <strong>capacidad productiva en 3-5 años</strong>, convirtiendo un pasivo (tierra degradada) en el activo más valioso del negocio.</p>
    </div>
    
    <div class="problema-card">
      <h3>Independencia de insumos: ventaja competitiva</h3>
      <div class="stat-highlight">30-50%</div>
      <p>Los productores que están reduciendo dependencia de fertilizantes sintéticos están capturando <strong>ahorros de 30-50% en costos directos</strong>, inmediatamente traducibles a mayor margen.</p>
      <p>Mientras más del <strong>60% de suelos chilenos requieren fertilización correctiva continua</strong>, algunos productores ya están generando fertilidad propia mediante micorrizas, fijación biológica y manejo de coberturas.</p>
      <p>La pregunta no es si los insumos importados seguirán subiendo. La pregunta es: <strong>¿cuánto dinero dejas de depender del dólar cada temporada?</strong></p>
    </div>
    
    <div class="problema-card">
      <h3>Productores regenerativos: márgenes superiores</h3>
      <div class="stat-highlight">+78%</div>
      <p>Datos de sistemas regenerativos en EE.UU. muestran <strong>márgenes brutos 78% mayores</strong> que vecinos convencionales. No es magia: es matemática simple.</p>
      <p>Cuando reduces costos de insumos en 30-50% y mantienes o aumentas ligeramente el precio de venta (certificaciones, mercados premium), <strong>el margen se multiplica</strong>.</p>
      <p>Fincas regenerativas en Cataluña produjeron <strong>el mismo volumen con 30% menos costo</strong> en cultivos hortícolas. Esa diferencia va directo al bolsillo del productor, no al proveedor de agroquímicos.</p>
      <p>La ventana de oportunidad está abierta ahora: <strong>quienes rediseñan primero capturan la prima de precio en mercados premium</strong> antes que se sature la oferta.</p>
    </div>
    
  </div>
</div>

<!-- Sección Solución -->
<div class="section-sand">
  <h2 class="section-title">La solución: Arquitectura Productiva Regenerativa</h2>
  <p class="section-subtitle">
    <strong>Arquitectura Productiva Regenerativa (APR)</strong> es el diseño integral del sistema productivo: qué produces, dónde, cómo, cuándo y con qué recursos. Todo calculado para <strong>maximizar rentabilidad usando la biología del suelo como herramienta productiva</strong>.
  </p>
  <p class="section-subtitle">
    No vendemos técnicas aisladas (cultivos de cobertura, compost, rotaciones). Diseñamos <strong>sistemas completos</strong> donde cada elemento genera valor económico usando herramientas de la naturaleza.
  </p>
  
  <div class="comparison-container">
    <div class="comparison-table">
      
      <div class="comparison-column conventional">
        <h3>Modelo Convencional</h3>
        <ul>
          <li>Monocultivo o baja diversidad</li>
          <li>Dependencia de insumos sintéticos</li>
          <li>Labranza intensiva</li>
          <li>Costos crecientes de insumos</li>
          <li>Degradación progresiva del activo</li>
          <li>Vulnerabilidad climática</li>
        </ul>
      </div>
      
      <div class="comparison-column regenerative">
        <h3>Arquitectura Productiva Regenerativa</h3>
        <ul>
          <li>Diversidad funcional integrada</li>
          <li>Producción propia de fertilidad</li>
          <li>Mínima perturbación del suelo</li>
          <li>Reducción 30-50% costos insumos</li>
          <li>Regeneración medible del activo</li>
          <li>Resiliencia ante eventos extremos</li>
        </ul>
      </div>
      
    </div>
    
    <div class="principle-box">
      <p>No es "ser regenerativo". Es reducir costos y aumentar margen operacional.</p>
    </div>
  </div>
</div>

<!-- Sección 5 Pilares -->
<div class="section-white">
  <h2 class="section-title">Los 5 pilares del enfoque</h2>
  
  <div class="pilares-grid">
    
    <div class="pilar-card-enfoque">
      <div class="pilar-number">1</div>
      <h3>Análisis económico primero</h3>
      <p>Identificamos dónde se va tu dinero. <strong>El 70-80% de los costos operacionales</strong> en sistemas convencionales están concentrados en 3-5 rubros: fertilizantes, pesticidas, combustible, agua, mano de obra.</p>
      <p>Hacemos análisis de estructura de costos, identificamos dependencias críticas, y diseñamos estrategias de sustitución por procesos biológicos que generen los mismos servicios a menor costo.</p>
      <p><strong>No comenzamos con el suelo. Comenzamos con tu balance financiero.</strong></p>
    </div>
    
    <div class="pilar-card-enfoque destacado">
      <div class="pilar-number">2</div>
      <h3>Herramientas de la naturaleza</h3>
      <p>Hongos micorrízicos, bacterias fijadoras de nitrógeno, fauna del suelo, coberturas vivas, y <strong>animales integrados al sistema</strong>. No son conceptos abstractos: son <strong>insumos productivos</strong> que reemplazan fertilizantes y pesticidas.</p>
      <p>Un hongo micorrízico bien establecido puede <strong>incrementar la absorción de fósforo en 30-40%</strong>, eliminando o reduciendo drásticamente la necesidad de fertilización fosforada. Una pradera con leguminosas puede <strong>fijar 100-200 kg N/ha/año</strong> sin costo de insumo.</p>
      
      <h4>Los animales: pieza fundamental del sistema</h4>
      <p>La integración animal no es opcional: es <strong>fundamental para restablecer los ciclos del agua, minerales, nutrientes y energía</strong>.</p>
      
      <div class="ciclos-grid">
        <div class="ciclo-item">
          <strong>Ciclo del agua</strong>
          <p>El pastoreo rotativo estimula crecimiento radicular profundo, aumenta infiltración y reduce escorrentía. Las pezuñas rompen costras superficiales.</p>
        </div>
        
        <div class="ciclo-item">
          <strong>Ciclo de nutrientes</strong>
          <p>Los animales concentran nutrientes dispersos en el paisaje (forraje) y los devuelven al suelo en forma altamente disponible (estiércol, orina).</p>
        </div>
        
        <div class="ciclo-item">
          <strong>Ciclo de minerales</strong>
          <p>La orina aporta N, P, K y micronutrientes. El estiércol incorpora materia orgánica y alimenta la biología del suelo. Sin costo de insumo.</p>
        </div>
        
        <div class="ciclo-item">
          <strong>Ciclo de energía</strong>
          <p>Los animales convierten energía solar capturada por plantas en proteína animal de alto valor, estimulando rebrote y captura de carbono.</p>
        </div>
      </div>
      
      <p><strong>Estas no son promesas: son procesos biológicos medibles y replicables.</strong></p>
    </div>
    
    <div class="pilar-card-enfoque">
      <div class="pilar-number">3</div>
      <h3>Diseño de sistema completo</h3>
      <p>No parches. No técnicas aisladas. <strong>Rediseño integral</strong>: flujos de agua (diseño Keyline, infiltración), flujos de energía (radiación solar, fotosíntesis), flujos de nutrientes (ciclos cerrados), integración animal (pastoreo rotativo, gallinas móviles).</p>
      <p>Cada elemento cumple <strong>múltiples funciones</strong>. Las ovejas no solo producen carne y lana: controlan malezas, fertilizan, estimulan rebrote, aumentan infiltración.</p>
      <p>Diseñamos para que el sistema genere servicios ecosistémicos que antes comprabas como insumos.</p>
    </div>
    
    <div class="pilar-card-enfoque">
      <div class="pilar-number">4</div>
      <h3>Datos y medición</h3>
      <p><strong>Si no se mide, no se puede mejorar.</strong></p>
      <p>Establecemos líneas base y monitoreamos indicadores clave:</p>
      <ul style="list-style: disc; padding-left: 20px; margin: 16px 0;">
        <li>Carbono orgánico del suelo (laboratorio)</li>
        <li>Tasa de infiltración (prueba de campo)</li>
        <li>Producción de biomasa (kg MS/ha)</li>
        <li>Estructura de costos ($/unidad productiva)</li>
        <li>Margen operacional (costos-ingresos)</li>
      </ul>
      <p>Medimos cada 6-12 meses. Los datos guían las decisiones, no las intuiciones.</p>
    </div>
    
    <div class="pilar-card-enfoque">
      <div class="pilar-number">5</div>
      <h3>Transición rentable</h3>
      <p><strong>No quebrar mientras regeneras.</strong></p>
      <p>La transición toma 1-3 años dependiendo del estado inicial del suelo y el sistema productivo. Durante este período:</p>
      <ul style="list-style: disc; padding-left: 20px; margin: 16px 0;">
        <li>Planificación de flujo de caja mensual</li>
        <li>Timing de inversiones (no todo al inicio)</li>
        <li>Manejo de riesgo (diversificación)</li>
        <li>Horizonte 36 meses para evaluación completa</li>
      </ul>
      <p>Priorizamos cambios de <strong>alto impacto, bajo costo</strong> en los primeros 12 meses para generar ahorros inmediatos que financien inversiones posteriores.</p>
    </div>
    
  </div>
</div>

<!-- Sección Beneficios -->
<div class="section-dark">
  <h2 class="section-title">Beneficios de la Arquitectura Productiva Regenerativa</h2>
  <p class="section-subtitle">
    Ventajas económicas y operacionales respaldadas por evidencia científica
  </p>
  
  <div class="beneficios-grid">
    
    <div class="beneficio-card">
      <div class="beneficio-number">30-50%</div>
      <div class="beneficio-label">Reducción costos insumos</div>
      <p>Menor dependencia de fertilizantes y pesticidas sintéticos. Fincas regenerativas en Cataluña lograron 30% de ahorro en cultivos hortícolas manteniendo la misma producción.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number" style="font-size: 32px;">Independencia</div>
      <div class="beneficio-label">Menor volatilidad externa</div>
      <p>Reducción de exposición a fluctuaciones de dólar y mercado internacional. Producción propia en finca de compost, biofertilizantes, y manejo biológico de plagas.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number" style="font-size: 32px;">+Resiliencia</div>
      <div class="beneficio-label">Mayor estabilidad climática</div>
      <p>Sistemas más resistentes ante sequías, heladas y eventos extremos. Suelos con mayor materia orgánica retienen hasta 20.000 litros más de agua por hectárea.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number">+30%</div>
      <div class="beneficio-label">Mercados premium</div>
      <p>Acceso a certificaciones internacionales:</p>
      <ul>
        <li>Regenerative Organic Certified (ROC)</li>
        <li>Land to Market (Savory Institute)</li>
        <li>Regenagri (Control Union)</li>
      </ul>
      <p>Prima de precio de hasta +30% en mercados exigentes proyectada para 2035.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number" style="font-size: 28px;">Igual/Superior</div>
      <div class="beneficio-label">Rentabilidad</div>
      <p>Mayor rentabilidad que sistema convencional, incluso con producción algo menor, debido a reducción significativa de costos. Sistemas regenerativos en EE.UU. muestran márgenes brutos 78% mayores.</p>
    </div>
    
    <div class="beneficio-card">
      <div class="beneficio-number" style="font-size: 28px;">Bonos carbono</div>
      <div class="beneficio-label">Ingresos adicionales</div>
      <p>Acceso a mercados de carbono mediante captura y secuestro en suelo. Compensaciones por servicios ecosistémicos (retención hídrica, biodiversidad, control de erosión).</p>
    </div>
    
  </div>
</div>

<!-- Sección CTA -->
<div class="section-sand">
  <h2 class="section-title">Próximos pasos</h2>
  <p class="section-subtitle" style="margin-bottom: 50px;">
    ¿Listo para rediseñar tu sistema productivo?
  </p>
  
  <div class="cta-section">
    <div class="cta-box">
      <p><strong>Agenda una conversación de 30 minutos</strong> para revisar tu sistema actual, identificar dependencias críticas, y explorar oportunidades de transición rentable.</p>
      <p><a href="https://calendly.com/jaime-revolucionmarron/30min" target="_blank" rel="noopener" class="button">Agendar conversación →</a></p>
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
