---
layout: home
---

<div style="text-align: justify; line-height: 1.6; margin-bottom: 20px;">
  <h1 style="text-align: left;">🚀 Portafolio Profesional</h1>
  <p>
    ¡Bienvenido! Soy <strong>Matemático</strong> especializado en <strong>Data Science</strong>. 
    Mi enfoque se centra en transformar datos complejos en soluciones estratégicas, con especial énfasis en 
    modelado de riesgo, optimización matemática y aprendizaje automático. Aquí encontrarás una 
    selección de mis proyectos más relevantes y certificaciones técnicas.
  </p>
</div>

<hr>

<div style="display: block; clear: both; overflow: auto; margin-bottom: 20px;">
  <h2>🎓 Formación Académica</h2>
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;">
    
    <div style="background: #161b22; padding: 20px; border-radius: 12px; border: 1px solid #30363d; border-left: 4px solid #58a6ff;">
      <h3 style="margin: 0; color: #58a6ff; font-size: 1.1em;">Matemáticas</h3>
      <p style="margin: 5px 0; font-size: 0.9em; font-weight: bold; color: #8b949e;">Universidad Nacional de Colombia</p>
      <p style="margin: 0; font-size: 0.85em; color: #c9d1d9;">Bogotá D.C. | <strong>En curso</strong></p>
    </div>

    <div style="background: #161b22; padding: 20px; border-radius: 12px; border: 1px solid #30363d; border-left: 4px solid #58a6ff;">
      <h3 style="margin: 0; color: #58a6ff; font-size: 1.1em;">Diplomado en Machine Learning and Data Science</h3>
      <p style="margin: 5px 0; font-size: 0.9em; font-weight: bold; color: #8b949e;">Universidad Nacional de Colombia</p>
      <p style="margin: 0; font-size: 0.85em; color: #c9d1d9;">Bogotá D.C. | <strong>En curso</strong></p>
    </div>

    <div style="background: #161b22; padding: 20px; border-radius: 12px; border: 1px solid #30363d; border-left: 4px solid #58a6ff;">
      <h3 style="margin: 0; color: #58a6ff; font-size: 1.1em;">Seminario de Análisis de Datos</h3>
      <p style="margin: 5px 0; font-size: 0.9em; font-weight: bold; color: #8b949e;">Universidad Nacional de Colombia</p>
      <p style="margin: 0; font-size: 0.85em; color: #c9d1d9;">Finalizado | <strong>2022</strong></p>
    </div>

  </div>
</div>

<hr>

<section style="clear: both; overflow: auto; margin-bottom: 20px;">
  <h2>🔬 Proyectos</h2>
  <div class="projects-grid"> 
    {% for p in site.projects %}
      <div class="project-item">
        {% if p.image %}
          <a href="{{ p.url | relative_url }}" class="project-link">
            <img src="{{ p.image | relative_url }}" alt="{{ p.title }}">
          </a>
        {% endif %}
        <div class="project-info">
          <h3>
            <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
          </h3>
          <p>{{ p.description }}</p>
        </div>
      </div>
    {% endfor %}
  </div>
</section>

<hr>

<section style="clear: both; overflow: hidden;">
  <div style="display: block; clear: both; overflow: auto; margin-bottom: 20px;">
    <h2>📜 Certificaciones</h2>
    
    <div style="display: flex; flex-direction: column; gap: 10px;">
      {% assign sorted_certs = site.certificates | reverse %}
      {% for cert in sorted_certs %}
        
        <details style="background: #161b22; border: 1px solid #30363d; border-radius: 8px; overflow: hidden;">
          <summary style="padding: 15px; cursor: pointer; color: #58a6ff; font-weight: bold; list-style: none; display: flex; justify-content: space-between; align-items: center;">
            <span>🎓 {{ cert.title }}</span>
            <span style="font-size: 0.8em; color: #8b949e;">Ver detalles ▾</span>
          </summary>
          
          <div style="padding: 0 15px 15px 15px; border-top: 1px solid #30363d; background: #0d1117;">
            <p style="margin: 15px 0 5px 0; font-size: 0.85em; color: #8b949e; font-weight: bold; text-transform: uppercase;">
              {{ cert.organization }}
            </p>
            <p style="margin: 0 0 15px 0; font-size: 0.95em; color: #c9d1d9; line-height: 1.5;">
              {{ cert.description }}
            </p>
            
            <a href="{{ cert.pdf_link | relative_url }}" target="_blank" 
               style="display: inline-block; padding: 8px 20px; background: #21262d; color: #58a6ff; border: 1px solid #30363d; border-radius: 6px; text-decoration: none; font-size: 0.85em; font-weight: bold; transition: 0.2s;">
               📄 Ver Certificado PDF
            </a>
          </div>
        </details>

      {% endfor %}
    </div>
  </div>
</section>

<hr>

<section style="clear: both; overflow: hidden;">
  <div style="display: block; clear: both; overflow: auto; margin-bottom: 20px;">
    <h2>📅 Eventos y Reconocimientos</h2>
    
    <div style="display: flex; flex-direction: column; gap: 10px;">
      {% assign sorted_events = site.events | reverse %}
      {% for event in sorted_events %}
        
        <details style="background: #161b22; border: 1px solid #30363d; border-radius: 8px; overflow: hidden;">
          <summary style="padding: 15px; cursor: pointer; color: #58a6ff; font-weight: bold; list-style: none; display: flex; justify-content: space-between; align-items: center;">
            <span>🏆 {{ event.title }}</span>
            <span style="font-size: 0.8em; color: #8b949e;">Ver detalles ▾</span>
          </summary>
          
          <div style="padding: 0 15px 15px 15px; border-top: 1px solid #30363d; background: #0d1117;">
            <p style="margin: 15px 0 5px 0; font-size: 0.85em; color: #8b949e; font-weight: bold; text-transform: uppercase;">
              {{ event.organization }}
            </p>
            <p style="margin: 0 0 15px 0; font-size: 0.95em; color: #c9d1d9; line-height: 1.5;">
              {{ event.description }}
            </p>
            
            <a href="{{ event.pdf_link | relative_url }}" target="_blank" 
               style="display: inline-block; padding: 8px 20px; background: #21262d; color: #58a6ff; border: 1px solid #30363d; border-radius: 6px; text-decoration: none; font-size: 0.85em; font-weight: bold; transition: 0.2s;">
               📄 Ver Constancia PDF
            </a>
          </div>
        </details>

      {% endfor %}
    </div>
  </div>
</section>

<hr>

<section style="clear: both; overflow: hidden;">
  <div style="display: block; clear: both; overflow: auto; margin-bottom: 20px;"> 
    <h2>📐 Habilidades Matemáticas</h2>
    
    <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px;">
      <div style="background: #161b22; padding: 15px; border-radius: 8px; border: 1px solid #30363d;">
        <h4 style="color: #58a6ff; margin-top: 0;">📊 Estadística y Probabilidad</h4>
        <ul style="font-size: 0.9em; padding-left: 20px;">
          <li>Inferencia Estadística y Pruebas de Hipótesis.</li>
          <li>Modelos Estocásticos y Teorema de Bayes.</li>
          <li>Análisis de Regresión (Lineal, Logística, Poisson).</li>
        </ul>
      </div>

      <div style="background: #161b22; padding: 15px; border-radius: 8px; border: 1px solid #30363d;">
        <h4 style="color: #58a6ff; margin-top: 0;">⚙️ Optimización y Cálculo</h4>
        <ul style="font-size: 0.9em; padding-left: 20px;">
          <li>Optimización Convexa y Descenso de Gradiente.</li>
          <li>Cálculo Multivariado para Redes Neuronales.</li>
          <li>Programación Lineal, Binaria y Entera.</li>
        </ul>
      </div>

      <div style="background: #161b22; padding: 15px; border-radius: 8px; border: 1px solid #30363d;">
        <h4 style="color: #58a6ff; margin-top: 0;">🧬 Álgebra Lineal y Computacional</h4>
        <ul style="font-size: 0.9em; padding-left: 20px;">
          <li>Descomposición de Matrices (SVD, PCA, Autovalores).</li>
          <li>Teoría de Grafos para Análisis de Redes.</li>
          <li>Análisis Numérico y Estabilidad de Algoritmos.</li>
        </ul>
      </div>

      <div style="background: #161b22; padding: 15px; border-radius: 8px; border: 1px solid #30363d;">
        <h4 style="color: #58a6ff; margin-top: 0;">🤖 Machine Learning y Riesgo</h4>
        <ul style="font-size: 0.9em; padding-left: 20px;">
          <li>Scoring y fraude (XGBoost, LightGBM).</li>
          <li>Estimación de parámetros PD y LGD.</li>
          <li>Modelado de Churn y Life-time Value.</li>
          <li>Valor en Riesgo (VaR) y Monte Carlo.</li>
        </ul>
      </div>
    </div>
  </div> </section>

<hr> 

<section style="clear: both; overflow: hidden;">
  <h2>🛠️ Herramientas de Software</h2>
  <div style="background: #161b22; padding: 20px; border-radius: 8px; border: 1px solid #30363d;">
    <div style="margin-bottom: 20px;">
      <h4 style="color: #c9d1d9; margin-bottom: 10px;">💻 Lenguajes & Bases de Datos</h4>
      <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
      <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL">
      <img src="https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white" alt="R">
    </div>
    <div style="margin-bottom: 20px;">
      <h4 style="color: #c9d1d9; margin-bottom: 10px;">🧪 Data Science & Machine Learning</h4>
      <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
      <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy">
      <img src="https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit Learn">
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch">
    </div>
    <div style="margin-bottom: 20px;">
      <h4 style="color: #c9d1d9; margin-bottom: 10px;">📊 Visualización de Datos</h4>
      <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=power-bi&logoColor=black" alt="Power BI">
      <img src="https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white" alt="Tableau">
      <img src="https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white" alt="Plotly">
    </div>
    <div>
      <h4 style="color: #c9d1d9; margin-bottom: 10px;">⚙️ Ingeniería & DevOps</h4>
      <img src="https://img.shields.io/badge/GIT-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git">
      <img src="https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white" alt="Azure">
      <img src="https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white" alt="GCP">
    </div>
  </div>
</section>

