<div align="center">

# 🌡️ Sistema IoT Multiestación

## Supervisión de Confort Térmico con ATOM S3 Lite, MQTT, Node-RED y ThingSpeak

![MicroPython](https://img.shields.io/badge/MicroPython-ESP32--S3-blue?style=for-the-badge)
![Node-RED](https://img.shields.io/badge/Node--RED-Dashboard-red?style=for-the-badge)
![MQTT](https://img.shields.io/badge/MQTT-HiveMQ-green?style=for-the-badge)
![ThingSpeak](https://img.shields.io/badge/ThingSpeak-MATLAB-orange?style=for-the-badge)
![IoT](https://img.shields.io/badge/Project-IoT-blueviolet?style=for-the-badge)

</div>

---

## 📌 Descripción del Proyecto

Este proyecto implementa un **sistema IoT multiestación** para la supervisión de confort térmico en oficinas, integrando sensores ambientales, comunicación MQTT, almacenamiento en la nube, visualización web y control automático del calefactor.

El sistema permite monitorear variables ambientales en tiempo real, visualizar datos históricos y ejecutar acciones de control mediante plataformas IoT como **Node-RED**, **ThingSpeak** y **HiveMQ**.

---

## 🖼️ Componentes del Sistema

<p align="center">
  <img src="images/01_Componentes_del_sistema.png" width="950">
</p>

---

## 🎥 Videos Demostrativos

<table>
<tr>

<td align="center" width="33%">

### ▶️ Video 1  
**Funcionamiento General**

<a href="https://www.youtube.com/shorts/dlZtpzraf4g">
  <img src="images/01_Componentes_del_sistema.png" width="280">
</a>

[Ver video](https://www.youtube.com/shorts/dlZtpzraf4g)

</td>

<td align="center" width="33%">

### ▶️ Video 2  
**Dashboard y Control**

<a href="https://www.youtube.com/shorts/fxgREKSWUAM">
  <img src="images/01_Componentes_del_sistema.png" width="280">
</a>

[Ver video](https://www.youtube.com/shorts/fxgREKSWUAM)

</td>

<td align="center" width="33%">

### ▶️ Video 3  
**Integración IoT**

<a href="https://www.youtube.com/shorts/SZaQv0HgcMM">
  <img src="images/01_Componentes_del_sistema.png" width="280">
</a>

[Ver video](https://www.youtube.com/shorts/SZaQv0HgcMM)

</td>

</tr>
</table>

---

## ⚙️ Arquitectura del Sistema

```text
                 DHT22
                   │
                   ▼
             ATOM S3 Lite
                   │
              WiFi / MQTT
                   │
                   ▼
              HiveMQ Broker
              ┌────┴────┐
              │         │
              ▼         ▼
          Node-RED   ThingSpeak
              │         │
              ▼         ▼
        Dashboard   MATLAB Analytics
              │
              ▼
      Control del Calefactor
```

---

## 🧩 Tecnologías Utilizadas

| Tecnología | Aplicación |
|----------|------------|
| **ATOM S3 Lite** | Unidad principal de adquisición y control |
| **DHT22** | Medición de temperatura y humedad |
| **MicroPython / UIFlow 2.0** | Programación del microcontrolador |
| **MQTT** | Comunicación IoT |
| **HiveMQ** | Broker MQTT |
| **Node-RED** | Dashboard y lógica de supervisión |
| **ThingSpeak** | Almacenamiento y análisis de datos |
| **MATLAB Analytics** | Procesamiento y alertas |

---

## 🚀 Funcionalidades Principales

✅ Monitoreo de temperatura en tiempo real  

✅ Monitoreo de humedad relativa  

✅ Control manual del calefactor  

✅ Control automático mediante lógica de decisión  

✅ Comunicación MQTT con HiveMQ  

✅ Visualización profesional en Node-RED  

✅ Registro histórico de datos en ThingSpeak  

✅ Integración con MATLAB Analytics y alertas  

---

## 📂 Estructura del Repositorio

```text
Sistema-IoT
│
├── images
│   └── 01_Componentes_del_sistema.png
│
├── PROGRAMACIÓN NODE RED
│
├── PROGRAMACIÓN THINGSPEAK
│
├── PROGRAMACIÓN UIFLOW
│
└── README.md
```

---

## 📊 Flujo General de Operación

1. El sensor **DHT22** mide temperatura y humedad.
2. El **ATOM S3 Lite** procesa los datos.
3. Los datos son enviados mediante **MQTT**.
4. **Node-RED** recibe, visualiza y controla el sistema.
5. **ThingSpeak** almacena los datos históricos.
6. El sistema permite operar el calefactor en modo manual o automático.

---

## 👨‍💻 Autor

**Diego Ayala**  
Ingeniero de Petróleos  
Doctor en Ciencias de la Tierra  
Máster en Petróleos  
Máster en Energías Renovables  
Maestrante en Robótica y Automatización  

Ecuador 🇪🇨

---

<div align="center">

### ⭐ Proyecto académico de IoT, automatización y supervisión térmica

</div>
