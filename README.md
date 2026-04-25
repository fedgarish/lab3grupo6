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

<h3>Selección del dataset - Network IoT Dataset</h3>
<ul>
  
  <li>URL: https://www.kaggle.com/datasets/amineipad/ioittt?resource=download</li>
  <li>Interfaz web basada en HTML que consume el API y permite la búsqueda de establecimientos desde un mapa interactivo</li>

</ul>

<h3>API funcional</h3>
<ul>
  <li>FastAPI</li>
  <li>Uvicornli>
  <li>Pydantic</li>
  <li>Requests</li>
  <li>Google Maps / Google Places API</li>
  <li>Jinja2</li>
  <li>Python</li>
</ul>

<h3>Creatividad/Dificultad</h3>
<ul>
  
<li>Integración con APIs externas</li>
<li>Procesamiento de datos</li>
<li>Demos de Soluciones tecnologicas</li>
</ul>

<h3>Evidencia</h3>
<h5>Construcción del API </h5>
<h5>API de búsqueda geolocalizada</h5>
<ul>
<li>El código implementa una API con FastAPI que consume la API de Google Places para buscar establecimientos cercanos según ubicación, radio y tipo de lugar. Procesa los resultados para extraer información relevante como nombre, dirección, calificación, horario actual y una imagen representativa, y expone estos datos mediante un endpoint GET y una interfaz web basada en plantillas HTML.</li>
</ul>
<p align="center">
  <img src="Evidencias/Parte1_10.PNG" width="500">
  <img src="Evidencias/Parte1_11.PNG" width="500">
  <img src="Evidencias/Parte1_12.PNG" width="500">
  
</p>
<h5>Codificación de la interfaz web para consulta de establecimientos desde el mapa</h5>
<ul>
<li>El código implementa una interfaz web interactiva que utiliza Google Maps para seleccionar una ubicación mediante clic y consultar establecimientos cercanos a través de un endpoint del API. Los resultados se obtienen usando fetch, se procesan dinámicamente y se muestran en tarjetas con información relevante y enlaces directos a Google Maps.
</li>
</ul>
<p align="center">
  <img src="Evidencias/Parte1_13.PNG" width="500">
  <img src="Evidencias/Parte1_14.PNG" width="500">
  <img src="Evidencias/Parte1_15.PNG" width="500">
  <img src="Evidencias/Parte1_16.PNG" width="500">
  
</p>
<h5>Resultados visuales de búsqueda geolocalizada de establecimientos
</h5>
<ul>
<li>La interfaz web permite seleccionar una ubicación directamente en el mapa, definir un radio de búsqueda y elegir el tipo de establecimiento. A partir de estos parámetros, la aplicación consulta el API local y muestra los resultados de forma dinámica, facilitando la exploración de lugares cercanos como bancos, farmacias o restaurantes.
</li>
</ul>
<p align="center">
  <img src="Evidencias/Parte1_1.jpeg" width="500">
  <img src="Evidencias/Parte1_2.jpeg" width="500">
  <img src="Evidencias/Parte1_3.jpeg" width="500">
  <img src="Evidencias/Parte1_4.jpeg" width="500">
  <img src="Evidencias/Parte1_5.jpeg" width="500">
</p>
<h5>Habilitación de Google Maps JavaScript API</h5>
<ul>
<li>La imagen muestra la activación de la API de Google Maps JavaScript en la consola de Google Cloud, la cual permite integrar mapas interactivos en la aplicación web. Esta configuración es fundamental para visualizar el mapa, capturar la ubicación seleccionada por el usuario y habilitar la interacción geográfica utilizada por el API del proyecto.
</li>
</ul>
<p align="center">
  <img src="Evidencias/Parte1_6.jpeg" width="500">
</p>
<h5>Habilitación de Google Places API
</h5>
<ul>
<li>La imagen muestra la activación de la API de Google Places en la consola de Google Cloud, necesaria para obtener información detallada de establecimientos como nombre, dirección, calificación y horarios. Esta API es utilizada por el backend del proyecto para realizar búsquedas geolocalizadas y alimentar los resultados consultados desde el API y la interfaz web.
</li>
</ul>
<p align="center">
  <img src="Evidencias/Parte1_7.jpeg" width="500">
</p>
<h5>Creación y gestión de la clave de API de Google Maps Platform
</h5>
<ul>
<li>La imagen muestra la creación y administración de una clave de API en Google Cloud, utilizada para autenticar el acceso a los servicios de Google Maps y Google Places. Esta clave es esencial para que la aplicación pueda consumir las APIs habilitadas de forma segura y controlar su uso mediante restricciones configuradas.
</li>
</ul>
<p align="center">
  <img src="Evidencias/Parte1_8.jpeg" width="500">
</p>
<h5>Consumo del API local desde la interfaz web
</h5>
<ul>
<li>La imagen muestra la ejecución de una consulta desde la interfaz web hacia el API local, visualizada mediante las herramientas de desarrollador del navegador. Se evidencia una petición GET exitosa (HTTP 200) al endpoint del API con parámetros de latitud, longitud, radio y tipo de lugar, confirmando la correcta comunicación entre el frontend y el backend del proyecto.
</li>
</ul>
<p align="center">
  <img src="Evidencias/Parte1_9.jpeg" width="500">
</p>
<h5>Web scraping y exportación de datos
</h5>
<ul>
<li>El código implementa un proceso de web scraping con Selenium y BeautifulSoup para extraer información de establecimientos desde una interfaz web dinámica. Los datos obtenidos se procesan y estructuran con pandas en un DataFrame y finalmente se exportan a formatos CSV y Excel, permitiendo su almacenamiento y análisis posterior.
</li>
</ul>
<p align="center">
  <img src="Evidencias/Parte1_17.PNG" width="500">
  <img src="Evidencias/Parte1_18.PNG" width="500">
  <img src="Evidencias/Parte1_19.PNG" width="500">
</p>


<h5>Historial de commits y control de versiones del proyecto
</h5>
<ul>
<li>La imagen muestra la ejecución de una consulta desde la interfaz web hacia el API local, visualizada mediante las herramientas de desarrollador del navegador. Se evidencia una petición GET exitosa (HTTP 200) al endpoint del API con parámetros de latitud, longitud, radio y tipo de lugar, confirmando la correcta comunicación entre el frontend y el backend del proyecto.
</li>
</ul>
<p align="center">
  <img src="Evidencias/Branch.PNG" width="500">
</p>




<h3>Comentario</h3>
<p>
Las imágenes incluidas documentan visualmente todo el desarrollo del proyecto, desde la configuración de las APIs de Google Maps y Google Places en Google Cloud, la creación y gestión de credenciales, hasta el funcionamiento de la interfaz web y el consumo del API local. Asimismo, se evidencian los resultados obtenidos al realizar búsquedas geolocalizadas de distintos tipos de establecimientos y el historial de commits en GitHub, lo que demuestra la correcta implementación del sistema, el uso de buenas prácticas de desarrollo y el trabajo colaborativo realizado durante el proyecto.
</p>

<h2>Conclusiones</h2>
<ul>
  <li>El proyecto permitió desarrollar una solución completa basada en una API funcional, integrando tecnologías como FastAPI, Google Maps API y Google Places API, logrando una búsqueda geolocalizada de establecimientos de manera eficiente y estructurada.</li>
  <li>A través del uso de web scraping y procesamiento de datos, se obtuvo información relevante que fue limpiada, estructurada y almacenada en formatos estándar como CSV y Excel, facilitando su reutilización y análisis.</li>
  <li>La implementación de una interfaz web interactiva mejoró la usabilidad del sistema, permitiendo al usuario seleccionar ubicaciones directamente desde un mapa y visualizar los resultados de forma clara mediante tarjetas informativas.</li>
  <li>La correcta configuración de credenciales y habilitación de APIs en Google Cloud fue un aspecto clave para garantizar el funcionamiento seguro y estable de los servicios utilizados en el proyecto.</li>
  <li>El uso de GitHub como sistema de control de versiones permitió evidenciar un trabajo colaborativo organizado, con historial de commits, manejo de ramas y resolución de conflictos, reflejando buenas prácticas de desarrollo de software.
</li>
</ul>
<hr>
