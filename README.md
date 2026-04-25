<p align="center">
  <img src="Evidencias/logo-uide.webp" width="220" alt="Logo UIDE">
</p>

<h1 align="center">Laboratorio 3 - Grupo 6</h1>

<p align="center">
  <b>MCIB-B</b><br>
  Trabajo grupal enfocado en el tratamiento de datos, análisis exploratorio de datos(EDA) y visualización de datos.
</p>
<h2>Integrantes</h2>

<ul>
  <li>AMAGUA OSCAR</li>
  <li>OJEDA ALAN</li>
  <li>SUNTAXI DIEGO</li>
</ul>
<hr>

<h2>Introducción</h2>
<p>
En el presente proyecto se desarrolla un análisis de datos a partir de un conjunto obtenido de Kaggle, el cual se enfoca en el estudio del tráfico generado en entornos de dispositivos interconectados. Este tipo de información resulta especialmente relevante en la actualidad debido al crecimiento de ecosistemas digitales donde múltiples dispositivos intercambian datos de manera constante, generando grandes volúmenes de información susceptibles de análisis.

El dataset seleccionado contiene registros estructurados de actividad en red, incluyendo características relacionadas con flujos de comunicación, protocolos y métricas de transmisión. Además, incorpora tanto comportamientos normales como eventos asociados a actividades maliciosas, lo que permite abordar problemas de clasificación y detección de anomalías en contextos reales. En particular, este tipo de datos es ampliamente utilizado en el desarrollo de sistemas de detección de intrusos y modelos de ciberseguridad basados en aprendizaje automático .

A partir de este conjunto de datos, se llevó a cabo un proceso de preparación que incluyó la limpieza, transformación y adecuación de las variables, asegurando la consistencia y calidad necesarias para el análisis. Posteriormente, se realizó un Análisis Exploratorio de Datos (EDA) con el objetivo de identificar patrones de comportamiento, distribuciones relevantes y posibles irregularidades dentro del tráfico analizado.

Como complemento, se desarrollaron visualizaciones que permiten interpretar de forma clara las dinámicas presentes en los datos, facilitando la identificación de tendencias y relaciones entre variables. Finalmente, todo el proceso fue documentado en un repositorio de GitHub, donde se detallan los pasos realizados, los principales hallazgos y las conclusiones obtenidas.

Este proyecto no solo busca aplicar técnicas de análisis de datos, sino también comprender cómo la información generada en entornos de red puede ser utilizada para identificar comportamientos anómalos y contribuir al desarrollo de soluciones en el ámbito de la ciberseguridad.
</p>

<hr>

<h2>Objetivo</h2>
<p>
Analizar y procesar datos de tráfico de red en entornos IoT para identificar patrones de comunicación, diferenciar comportamientos normales de anómalos y generar insights que contribuyan a la comprensión y detección de posibles amenazas en sistemas interconectados.
</p>

<hr>

<h2>Parte 1 – Desarrollo</h2>

<h3>Selección del dataset - ToN_IoT Dataset</h3>
<ul>
  <li>URL: https://www.kaggle.com/datasets/amineipad/ioittt</li>
  <li>Dataset de telemetría de red orientado a la detección de amenazas en entornos IoT.</li>
  <li>Incluye tráfico benigno y múltiples tipos de ataques como DDoS, Backdoors, Inyección y Ransomware.</li>
</ul>

<p>
El dataset ToN_IoT es ampliamente utilizado en investigación académica en ciberseguridad, ya que simula escenarios reales de ataque en infraestructuras híbridas (Cloud, Edge y redes locales). Su principal utilidad es el entrenamiento y validación de sistemas de detección de intrusos (IDS).
</p>

<hr>

<h3>Procesamiento de datos</h3>

<p>
Para garantizar la calidad del análisis, se realizó un proceso de limpieza y transformación de los datos enfocado en evitar sesgos y mejorar la capacidad analítica:
</p>

<ul>
  <li>Transformación de valores inválidos ("-") a valores nulos y posterior imputación.</li>
  <li>Eliminación de variables irrelevantes como direcciones IP y puertos para evitar overfitting.</li>
  <li>Codificación de variables categóricas como protocolos y estados de conexión.</li>
  <li>Preparación del dataset para análisis exploratorio y modelado.</li>
</ul>

<hr>

<h3>Análisis Exploratorio de Datos (EDA)</h3>

<p>
El análisis exploratorio permitió identificar patrones clave en el comportamiento del tráfico de red, diferenciando claramente entre tráfico benigno y actividades maliciosas.
</p>

<ul>
  <li>Distribución de diferentes tipos de ataques en el dataset.</li>
  <li>Identificación de patrones específicos de ataques como Ransomware.</li>
  <li>Análisis de volumen de datos transmitidos y duración de conexiones.</li>
  <li>Detección de anomalías en el tráfico de red.</li>
</ul>

<hr>

<h3>Visualización de datos</h3>

<p>
Se generaron visualizaciones que permiten interpretar de forma clara los patrones identificados:
</p>

<ul>
  <li>Distribución de ataques (gráfico de barras).</li>
  <li>Comparación de volumen de datos entre tráfico normal y malicioso (boxplot).</li>
  <li>Análisis de estados de conexión en ataques específicos.</li>
  <li>Detección de anomalías mediante gráficos de dispersión.</li>
</ul>

<hr>

<h3>Principales hallazgos</h3>

<ul>
  <li>El tráfico malicioso presenta patrones claramente diferenciables respecto al tráfico benigno.</li>
  <li>El Ransomware se caracteriza por conexiones persistentes en protocolo TCP.</li>
  <li>Se detectó un aumento significativo en el volumen de datos enviados en ataques de exfiltración.</li>
  <li>Los ataques generan comportamientos anómalos visibles en la relación entre datos enviados y recibidos.</li>
</ul>

<hr>

<h3>Modelo de Machine Learning</h3>

<p>
Como valor agregado, se implementó un modelo de clasificación basado en Random Forest para la detección de amenazas.
</p>

<ul>
  <li>Separación del dataset: 80% entrenamiento, 20% prueba.</li>
  <li>Entrenamiento del modelo con variables relevantes del tráfico.</li>
  <li>Evaluación mediante matriz de confusión.</li>
</ul>

<p>
El modelo permitió identificar ataques con un alto nivel de precisión, demostrando el potencial del uso de Machine Learning en sistemas IDS.
</p>

<hr>

<h3>Evidencia</h3>

<p align="center">
  <img src="Evidencias/distribucion_ataques.png" width="500">
  <img src="Evidencias/boxplot_ransomware.png" width="500">
</p>

<p align="center">
  <img src="Evidencias/pie_estados.png" width="500">
  <img src="Evidencias/anomalias_bytes.png" width="500">
</p>

<p align="center">
  <img src="Evidencias/matriz_confusion.png" width="500">
  <img src="Evidencias/importancia_variables.png" width="500">
</p>

<hr>
<hr>

<h3>Interpretación de Resultados</h3>

<h4>1. Distribución de tipos de tráfico</h4>
<p>
El gráfico de distribución muestra que el tráfico normal representa la mayor proporción del dataset, seguido por diferentes tipos de ataques como DDoS, DoS, ransomware e inyección. 
</p>
<p>
Esto evidencia que el dataset está relativamente balanceado para el entrenamiento de modelos de detección, permitiendo identificar múltiples tipos de amenazas sin sesgos extremos hacia una sola clase.
</p>

<hr>

<h4>2. Anomalías en el volumen de datos (Scatter Plot)</h4>
<p>
El análisis de dispersión entre <b>src_bytes</b> y <b>dst_bytes</b> revela la presencia de clústeres diferenciados entre tráfico normal y malicioso.
</p>
<p>
Los ataques tienden a concentrarse en regiones con volúmenes atípicos de datos, mostrando patrones claramente separados del comportamiento normal. Esto confirma que el volumen de tráfico es un indicador clave para la detección de anomalías.
</p>

<hr>

<h4>3. Comparación de volumen: Ransomware vs Tráfico Normal (Boxplot)</h4>
<p>
El boxplot evidencia que el tráfico asociado a ransomware presenta valores significativamente más altos de <b>src_bytes</b> en comparación con el tráfico normal.
</p>
<p>
Esto sugiere que los ataques de ransomware pueden involucrar procesos de exfiltración de datos o transferencias anómalas antes del cifrado, lo que los convierte en detectables mediante análisis de volumen.
</p>

<hr>

<h4>4. Estados de conexión en ataques de Ransomware</h4>
<p>
El gráfico de pastel muestra que el estado <b>OTH</b> domina ampliamente en el tráfico de ransomware, seguido por estados como <b>S0</b>, <b>SH</b> y <b>RSTRH</b>.
</p>
<p>
Esto indica que los ataques generan conexiones persistentes o no convencionales, lo cual es característico de comunicaciones con servidores de comando y control (C2).
</p>

<hr>

<h4>5. Importancia de variables (Feature Importance)</h4>
<p>
El modelo de Random Forest identificó que variables como <b>src_pkts</b>, <b>src_ip_bytes</b> y <b>dns_query</b> son las más relevantes para la detección de ataques.
</p>
<p>
Esto demuestra que tanto el volumen de tráfico como el comportamiento de las consultas DNS son factores críticos en la identificación de actividades maliciosas.
</p>

<hr>

<h4>6. Evaluación del modelo (Matriz de confusión)</h4>
<p>
La matriz de confusión muestra un alto nivel de precisión en la clasificación, con una baja cantidad de falsos positivos y falsos negativos.
</p>

<ul>
  <li>Alta detección correcta de tráfico normal</li>
  <li>Alta detección correcta de ataques</li>
  <li>Bajo nivel de errores de clasificación</li>
</ul>

<p>
Esto confirma que el modelo es efectivo para su uso en sistemas de detección de intrusos (IDS), con un buen equilibrio entre precisión y capacidad de generalización.
</p>

<hr>

<h3>Conclusión Analítica</h3>

<p>
El análisis realizado demuestra que el tráfico malicioso en entornos IoT presenta patrones claramente diferenciables en términos de volumen, comportamiento de conexión y uso de protocolos.
</p>

<p>
Las variables relacionadas con el volumen de datos y la duración de las conexiones son los indicadores más relevantes para la detección de amenazas, lo que permite diseñar sistemas de seguridad eficientes incluso en dispositivos con recursos limitados.
</p>

<p>
Finalmente, la implementación de modelos de Machine Learning como Random Forest confirma que es posible automatizar la detección de intrusiones con alta precisión, contribuyendo al desarrollo de soluciones de ciberseguridad modernas y escalables.
</p>

<hr>
<h3>Comentario</h3>

<p>
El desarrollo del análisis permitió comprender la importancia del tratamiento de datos en entornos de ciberseguridad. La combinación de técnicas de limpieza, análisis exploratorio y visualización permitió identificar patrones relevantes y comportamientos anómalos en el tráfico IoT.
</p>

<p>
Adicionalmente, la implementación de un modelo de Machine Learning demuestra cómo estos análisis pueden ser llevados a sistemas reales de detección de intrusiones, optimizando la seguridad en infraestructuras modernas.
</p>

<hr>

<h2>Conclusiones</h2>

<ul>
  <li>El análisis de tráfico IoT permite identificar patrones clave en la detección de amenazas.</li>
  <li>El volumen de datos y la duración de las conexiones son indicadores críticos en ataques como Ransomware.</li>
  <li>Los modelos de Machine Learning pueden mejorar significativamente la detección de intrusiones.</li>
  <li>Es posible implementar soluciones ligeras de seguridad basadas en variables clave en entornos Edge.</li>
  <li>El uso de herramientas de análisis de datos facilita la toma de decisiones en ciberseguridad.</li>
</ul>

<hr>
