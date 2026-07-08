<div align="center">

# 🌡️ Sistema IoT Multiestación para Supervisión de Confort Térmico con Lógica Difusa

## Supervisión de Confort Térmico con ATOM S3 Lite, MQTT, Node-RED y ThingSpeak

</div>

---

## 📌 Descripción del Proyecto

Diseño e integración de un sistema IoT multiestación para monitoreo y control térmico en tres estaciones de trabajo con condiciones ambientales diferenciadas. Cada estación incorpora un nodo M5Stack AtomS3 Lite, un sensor DHT22, un relé y un calefactor independiente. La lógica local permite control de temperatura por histéresis en cada estación, mientras que el control remoto se realiza desde un dashboard en Node-RED o desde una página web conectada a ThingSpeak. Los nodos se comunican entre sí mediante ESP-NOW; el nodo maestro es el único con acceso a la red WiFi local y mantiene comunicación bidireccional por HTTP con Node-RED. A su vez, Node-RED intercambia datos bidireccionalmente por MQTT con dispositivos de ThingSpeak creados para cada estación. En la nube se visualizan temperatura, humedad, estado del calefactor, modo de operación, gráficas temporales e indicadores térmicos. El análisis en MATLAB se ejecuta cada 15 minutos y calcula Heat Index, punto de rocío, bulbo húmedo estimado, WBGT estimado e índice de disconfort. Además, combina 	índices térmicos, tendencia y exposición mediante lógica difusa para clasificar el riesgo, mostrar alertas y enviar reportes por correo por estación. El resultado muestra el adecuado funcionamiento del sistema con una arquitectura modular, replicable y orientada a la supervisión térmica simultánea de múltiples puestos de trabajo.

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
**Funcionamiento Estación 1 - Maestro**

<a href="https://www.youtube.com/shorts/dlZtpzraf4g">
  <img src="images/01_Componentes_del_sistema.png" width="280">
</a>

[Ver video](https://www.youtube.com/shorts/dlZtpzraf4g)

</td>

<td align="center" width="33%">

### ▶️ Video 2  
**Funcionamiento Estación 2 - Esclavo**

<a href="https://www.youtube.com/shorts/fxgREKSWUAM">
  <img src="images/01_Componentes_del_sistema.png" width="280">
</a>

[Ver video](https://www.youtube.com/shorts/fxgREKSWUAM)

</td>

<td align="center" width="33%">

### ▶️ Video 3  
**Funcionamiento Estación 3 - Esclavo**

<a href="https://www.youtube.com/shorts/SZaQv0HgcMM">
  <img src="images/01_Componentes_del_sistema.png" width="280">
</a>

[Ver video](https://www.youtube.com/shorts/SZaQv0HgcMM)

</td>

</tr>
</table>

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
| **ThingSpeak** | Dashboard y lógica de supervisión - Almacenamiento y análisis de datos |
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


### ⭐ Proyecto académico de IoT, automatización y supervisión térmica

</div>
