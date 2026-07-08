::: {align="center"}
# 🌡️ Sistema IoT Multiestación para Supervisión de Confort Térmico con Lógica Difusa

### ATOM S3 Lite · ESP-NOW · MQTT · Node-RED · ThingSpeak · MATLAB Analytics

![IoT](https://img.shields.io/badge/Proyecto-IoT-blue?style=for-the-badge)
![ESP-NOW](https://img.shields.io/badge/ESP--NOW-Comunicación-green?style=for-the-badge)
![MQTT](https://img.shields.io/badge/MQTT-HiveMQ-orange?style=for-the-badge)
![Node-RED](https://img.shields.io/badge/Node--RED-Dashboard-red?style=for-the-badge)
![ThingSpeak](https://img.shields.io/badge/ThingSpeak-Cloud-lightgrey?style=for-the-badge)
![MATLAB](https://img.shields.io/badge/MATLAB-Analytics-blueviolet?style=for-the-badge)
:::

------------------------------------------------------------------------

# 📌 Descripción del Proyecto

```{=html}
<p align="justify">
```
Este proyecto presenta el diseño e integración de un sistema IoT
multiestación para el monitoreo y control térmico de tres estaciones de
trabajo con condiciones ambientales diferenciadas. Cada estación
incorpora un nodo M5Stack AtomS3 Lite, un sensor DHT22, un módulo de
relé y un calefactor independiente. El control local se ejecuta mediante
histéresis, mientras que el control remoto puede realizarse desde
Node‑RED o desde una interfaz web implementada sobre ThingSpeak.

Los nodos intercambian información mediante ESP‑NOW. El nodo maestro es
el único conectado a la red WiFi y actúa como pasarela entre la red de
sensores y Node‑RED mediante HTTP bidireccional. Posteriormente,
Node‑RED sincroniza datos y comandos con ThingSpeak mediante MQTT.

MATLAB Analysis ejecuta periódicamente el cálculo de Heat Index, Punto
de Rocío, Bulbo Húmedo Estimado, WBGT Estimado, Índice de Disconfort,
PMV, PPD y otros indicadores térmicos. Mediante lógica difusa se
clasifica el riesgo térmico y se generan alertas automáticas y reportes
por correo electrónico.

```{=html}
</p>
```

------------------------------------------------------------------------

# 🖼️ Componentes del Sistema

```{=html}
<p align="center">
```
`<img src="images/01_Componentes_del_sistema.png" width="950">`{=html}
```{=html}
</p>
```

------------------------------------------------------------------------

# 🎥 Videos Demostrativos

  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                                                      Estación 1                                                                                                                                          Estación 2                                                                                                                                          Estación 3
  --------------------------------------------------------------------------------------------------------------------------------------------------- --------------------------------------------------------------------------------------------------------------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------
                                                                   **Nodo Maestro**                                                                                                                                    **Nodo Esclavo**                                                                                                                                    **Nodo Esclavo**

   `<a href="https://www.youtube.com/shorts/dlZtpzraf4g">`{=html}`<img src="images/01_Componentes_del_sistema.png" width="260">`{=html}`</a>`{=html}   `<a href="https://www.youtube.com/shorts/fxgREKSWUAM">`{=html}`<img src="images/01_Componentes_del_sistema.png" width="260">`{=html}`</a>`{=html}   `<a href="https://www.youtube.com/shorts/SZaQv0HgcMM">`{=html}`<img src="images/01_Componentes_del_sistema.png" width="260">`{=html}`</a>`{=html}

                                               [▶ Ver Video](https://www.youtube.com/shorts/dlZtpzraf4g)                                                                                           [▶ Ver Video](https://www.youtube.com/shorts/fxgREKSWUAM)                                                                                           [▶ Ver Video](https://www.youtube.com/shorts/SZaQv0HgcMM)
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

# 🧩 Tecnologías Utilizadas

  Tecnología            Aplicación
  --------------------- --------------------------------------
  M5Stack AtomS3 Lite   Nodo de adquisición y control
  DHT22                 Medición de temperatura y humedad
  ESP-NOW               Comunicación entre estaciones
  WiFi                  Conectividad del nodo maestro
  HTTP                  Comunicación con Node‑RED
  MQTT / HiveMQ         Intercambio de datos IoT
  Node‑RED              Dashboard y control
  ThingSpeak            Nube y almacenamiento
  MATLAB Analysis       Indicadores térmicos y lógica difusa

------------------------------------------------------------------------

# 🚀 Funcionalidades Principales

  -----------------------------------------------------------------------
  Funcionalidad                       Descripción
  ----------------------------------- -----------------------------------
  🌡️ Monitoreo Multiestación          Supervisión simultánea de tres
                                      estaciones.

  📊 Temperatura y Humedad            Lectura continua mediante DHT22.

  🔥 Control por Histéresis           Control automático del calefactor.

  🎮 Modo Manual y Automático         Cambio remoto desde Node‑RED y
                                      ThingSpeak.

  📡 ESP‑NOW                          Comunicación inalámbrica entre
                                      nodos.

  ☁️ MQTT                             Integración con ThingSpeak.

  🖥️ Dashboard                        Supervisión en tiempo real mediante
                                      Node‑RED.

  📈 Histórico                        Registro de variables ambientales.

  🧠 MATLAB Analysis                  Cálculo de indicadores térmicos.

  🚨 Lógica Difusa                    Clasificación automática del
                                      riesgo.

  📧 Alertas                          Envío automático de correos
                                      electrónicos.

  🔄 Arquitectura Modular             Sistema escalable y replicable.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# 🧠 Indicadores Calculados

-   Heat Index
-   Punto de Rocío
-   Bulbo Húmedo Estimado
-   WBGT Estimado
-   Índice de Disconfort
-   PMV
-   PPD
-   Tendencia Térmica
-   Exposición Reciente
-   RiskScore Difuso

------------------------------------------------------------------------

# 📂 Estructura del Repositorio

``` text
Sistema-IoT
│
├── images
│   └── 01_Componentes_del_sistema.png
├── PROGRAMACIÓN NODE RED
├── PROGRAMACIÓN THINGSPEAK
├── PROGRAMACIÓN UIFLOW
└── README.md
```

------------------------------------------------------------------------

# 👨‍💻 Autor

**Diego Ayala**

-   Ingeniero de Petróleos
-   Doctor en Ciencias de la Tierra
-   Máster en Petróleos
-   Máster en Energías Renovables
-   Maestrante en Robótica y Automatización

Ecuador 🇪🇨

------------------------------------------------------------------------

::: {align="center"}
### ⭐ Proyecto académico de IoT, Automatización y Supervisión Térmica Inteligente
:::
