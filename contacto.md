---
layout: default
title: Contacto - Revolución Marrón
description: Conversemos sobre cómo rediseñar tu sistema productivo
---

<style>
/* Hero Section */
.contacto-hero {
  position: relative;
  background: linear-gradient(rgba(61, 40, 23, 0.65), rgba(61, 40, 23, 0.65)),
              url('{{ '/assets/images/contacto-hero-manos-tierra.png' | relative_url }}');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  color: white;
  padding: 140px 40px 100px;
  text-align: center;
  margin-bottom: 80px;
  min-height: 60vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.contacto-hero-content {
  position: relative;
  z-index: 2;
  max-width: 900px;
}

.contacto-hero h1 {
  font-size: clamp(36px, 5vw, 56px);
  margin-bottom: 24px;
  color: white;
  text-shadow: 0 4px 16px rgba(0,0,0,0.8);
  font-weight: 700;
}

.contacto-hero p {
  font-size: clamp(17px, 2vw, 22px);
  line-height: 1.7;
  max-width: 850px;
  margin: 0 auto;
  color: rgba(255,255,255,0.98);
  text-shadow: 0 3px 12px rgba(0,0,0,0.7);
  font-weight: 500;
}

/* Contact Options Grid */
.contact-options-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 32px;
  max-width: 1200px;
  margin: 0 auto 80px;
  padding: 0 40px;
}

.contact-option {
  background: white;
  border: 2px solid rgba(107, 68, 35, 0.1);
  border-radius: 16px;
  padding: 40px 36px;
  box-shadow: var(--shadow-md);
  transition: all var(--transition-normal);
  text-align: center;
  position: relative;
  overflow: hidden;
}

.contact-option:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 6px;
  height: 100%;
  background: linear-gradient(180deg, var(--accent-green) 0%, #5a7a1e 100%);
  opacity: 0;
  transition: all var(--transition-normal);
}

.contact-option:hover {
  transform: translateY(-6px);
  box-shadow: var(--shadow-xl);
  border-color: var(--accent-green);
}

.contact-option:hover:before {
  opacity: 1;
}

.contact-icon {
  width: 64px;
  height: 64px;
  background: linear-gradient(135deg, var(--accent-green) 0%, #5a7a1e 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 24px;
  font-size: 28px;
  box-shadow: var(--shadow-md);
  transition: all var(--transition-normal);
}

.contact-option:hover .contact-icon {
  transform: scale(1.1);
  box-shadow: 0 8px 24px rgba(107, 142, 35, 0.4);
}

.contact-option h3 {
  font-size: 22px;
  color: var(--soil-dark);
  margin-bottom: 12px;
  font-weight: 700;
}

.contact-option p {
  font-size: 16px;
  line-height: 1.7;
  color: var(--text-light);
  margin-bottom: 24px;
}

.contact-option a {
  display: inline-block;
  background: linear-gradient(135deg, var(--accent-green) 0%, #5a7a1e 100%);
  color: white;
  padding: 12px 32px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  font-size: 15px;
  transition: all var(--transition-normal);
  box-shadow: var(--shadow-md);
}

.contact-option a:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-xl);
}

/* Calendly Section */
.calendly-section {
  background: var(--sand);
  padding: 80px 40px;
  border-radius: 16px;
  margin: 0 auto 80px;
  max-width: 1200px;
}

.calendly-section h2 {
  font-size: clamp(32px, 4vw, 42px);
  text-align: center;
  margin-bottom: 16px;
  color: var(--soil-dark);
}

.calendly-section p {
  font-size: 18px;
  text-align: center;
  max-width: 700px;
  margin: 0 auto 40px;
  color: var(--text-light);
  line-height: 1.7;
}

.calendly-container {
  background: white;
  border-radius: 12px;
  padding: 40px;
  box-shadow: var(--shadow-md);
  max-width: 900px;
  margin: 0 auto;
}

.calendly-embed {
  min-height: 630px;
  width: 100%;
  border-radius: 8px;
  overflow: hidden;
}

/* Additional Info */
.additional-info {
  max-width: 900px;
  margin: 0 auto 80px;
  padding: 0 40px;
}

.info-box {
  background: var(--sand-light);
  border-left: 4px solid var(--accent-green);
  padding: 32px 40px;
  border-radius: 12px;
  margin-bottom: 24px;
}

.info-box h3 {
  font-size: 20px;
  color: var(--soil-dark);
  margin-bottom: 12px;
  font-weight: 700;
}

.info-box p {
  font-size: 16px;
  line-height: 1.7;
  color: var(--text-light);
  margin: 0;
}

.info-box ul {
  list-style: none;
  padding: 0;
  margin: 12px 0 0 0;
}

.info-box li {
  padding: 8px 0 8px 24px;
  position: relative;
  font-size: 16px;
  color: var(--text-light);
  line-height: 1.6;
}

.info-box li:before {
  content: "✓";
  position: absolute;
  left: 0;
  color: var(--accent-green);
  font-weight: 700;
  font-size: 18px;
}

/* Responsive */
@media (max-width: 968px) {
  .contacto-hero {
    background-attachment: scroll !important;
    padding: 100px 24px 80px !important;
    min-height: 50vh !important;
  }
  
  .contact-options-grid {
    grid-template-columns: 1fr !important;
    padding: 0 24px;
  }
  
  .calendly-section {
    padding: 60px 24px;
  }
  
  .calendly-container {
    padding: 24px;
  }
  
  .additional-info {
    padding: 0 24px;
  }
  
  .info-box {
    padding: 24px 28px;
  }
}

@media (max-width: 480px) {
  .contacto-hero {
    padding: 80px 20px 60px !important;
    min-height: 40vh !important;
  }
  
  .contact-options-grid {
    padding: 0 20px;
  }
  
  .contact-option {
    padding: 32px 24px;
  }
  
  .calendly-section {
    padding: 50px 20px;
  }
  
  .calendly-container {
    padding: 20px;
  }
  
  .additional-info {
    padding: 0 20px;
  }
  
  .info-box {
    padding: 20px 24px;
  }
}
</style>

<!-- Hero Section -->
<div class="contacto-hero">
  <div class="contacto-hero-content">
    <h1>Conversemos</h1>
    <p>
      Trabajamos directamente con productores que buscan reducir costos, aumentar margen operacional y regenerar su activo más valioso: el suelo.
    </p>
  </div>
</div>

<!-- Contact Options -->
<div class="contact-options-grid">
  
  <div class="contact-option">
    <div class="contact-icon">📧</div>
    <h3>Email</h3>
    <p>
      Escríbeme directamente para consultas técnicas, propuestas de colaboración o información sobre servicios.
    </p>
    <a href="mailto:jaime@revolucionmarron.cl">jaime@revolucionmarron.cl</a>
  </div>
  
  <div class="contact-option">
    <div class="contact-icon">💬</div>
    <h3>WhatsApp</h3>
    <p>
      Contacto directo para conversaciones rápidas, consultas urgentes o coordinar visitas a terreno.
    </p>
    <a href="https://wa.me/56948955931" target="_blank" rel="noopener">+56 9 4895 5931</a>
  </div>
  
  <div class="contact-option">
    <div class="contact-icon">🔗</div>
    <h3>LinkedIn</h3>
    <p>
      Conecta conmigo en LinkedIn para seguir publicaciones técnicas, casos de estudio y actualidad del sector.
    </p>
    <a href="https://linkedin.com/in/jaime-fernandez-l" target="_blank" rel="noopener">Jaime Fernández López</a>
  </div>
  
</div>

<!-- Calendly Section -->
<div class="calendly-section">
  <h2>Agenda una conversación de 30 minutos</h2>
  <p>
    Revisamos tu sistema actual, identificamos dependencias críticas de insumos, y exploramos oportunidades de transición rentable hacia un modelo regenerativo.
  </p>
  
  <div class="calendly-container">
    <!-- Calendly inline widget begin -->
    <div class="calendly-inline-widget calendly-embed" 
         data-url="https://calendly.com/jaime-revolucionmarron/30min?hide_gdpr_banner=1&primary_color=6b8e23" 
         style="min-width:320px;height:630px;">
    </div>
    <script type="text/javascript" src="https://assets.calendly.com/assets/external/widget.js" async></script>
    <!-- Calendly inline widget end -->
  </div>
</div>

<!-- Additional Info -->
<div class="additional-info">
  
  <div class="info-box">
    <h3>¿Qué puedo esperar de la conversación inicial?</h3>
    <ul>
      <li>Análisis rápido de estructura de costos operacionales actual</li>
      <li>Identificación de dependencias críticas de insumos sintéticos</li>
      <li>Evaluación preliminar de potencial de transición regenerativa</li>
      <li>Discusión de casos similares y resultados documentados</li>
      <li>Sin compromiso, 100% técnico y confidencial</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3>Con quién trabajo</h3>
    <p>
      Productores agrícolas, ganaderos, vitivinícolas, frutícolas y forestales que buscan:
    </p>
    <ul>
      <li>Reducir dependencia de fertilizantes y pesticidas sintéticos</li>
      <li>Aumentar márgenes operacionales mediante reducción de costos</li>
      <li>Mejorar resiliencia climática y estabilidad productiva</li>
      <li>Acceder a mercados premium con certificaciones regenerativas</li>
      <li>Regenerar la capacidad productiva del suelo como activo</li>
    </ul>
  </div>
  
  <div class="info-box">
    <h3>Ubicación</h3>
    <p>
      <strong>Base de operaciones:</strong> Pirque, Región Metropolitana, Chile<br>
      <strong>Cobertura:</strong> Nacional (visitas a terreno coordinadas)<br>
      <strong>Consultoría remota:</strong> Disponible para todo Chile y Latinoamérica
    </p>
  </div>
  
</div>
