<div align="center">

# 🌡️ Sistema IoT Multiestación  
## Supervisión de Confort Térmico con Lógica Difusa

### ATOM S3 Lite · ESP-NOW · MQTT · Node-RED · ThingSpeak · MATLAB Analytics

</div>

---

## 📌 Descripción del Proyecto

Este proyecto presenta el diseño e integración de un **sistema IoT multiestación** para el monitoreo y control térmico de tres estaciones de trabajo con condiciones ambientales diferenciadas. Cada estación incorpora un nodo **M5Stack AtomS3 Lite**, un sensor **DHT22**, un módulo de relé y un calefactor independiente.

El sistema ejecuta control local de temperatura mediante **histéresis**, mientras que el control remoto puede realizarse desde un dashboard desarrollado en **Node-RED** o desde una página web conectada a **ThingSpeak**. Los nodos se comunican entre sí mediante **ESP-NOW**; el nodo maestro es el único con acceso a la red WiFi local y actúa como pasarela entre las estaciones y Node-RED mediante comunicación HTTP bidireccional.

A su vez, Node-RED intercambia datos con ThingSpeak mediante **MQTT**, permitiendo visualizar temperatura, humedad, estado del calefactor, modo de operación, gráficas temporales e indicadores térmicos. El análisis en **MATLAB Analysis** se ejecuta cada 15 minutos y calcula indicadores como **Heat Index**, **punto de rocío**, **bulbo húmedo estimado**, **WBGT estimado** e **índice de disconfort**.

Finalmente, el sistema combina índices térmicos, tendencia y exposición mediante **lógica difusa** para clasificar el riesgo térmico, mostrar alertas y enviar reportes por correo electrónico por estación.

---

## 🖼️ Componentes del Sistema

<p align="center">
  <img src="IMAGES/01_Componentes_del_sistema.png" width="950">
</p>

---

## 🎥 Videos Demostrativos

<table>
<tr>
<td align="center" width="33%">

### ▶️ Estación 1  
**Nodo Maestro**

<a href="https://www.youtube.com/shorts/dlZtpzraf4g">
  <img src="IMAGES/01_Componentes_del_sistema.png" width="270">
</a>

[Ver video](https://www.youtube.com/shorts/dlZtpzraf4g)

</td>
<td align="center" width="33%">

### ▶️ Estación 2  
**Nodo Esclavo**

<a href="https://www.youtube.com/shorts/fxgREKSWUAM">
  <img src="IMAGES/01_Componentes_del_sistema.png" width="270">
</a>

[Ver video](https://www.youtube.com/shorts/fxgREKSWUAM)

</td>
<td align="center" width="33%">

### ▶️ Estación 3  
**Nodo Esclavo**

<a href="https://www.youtube.com/shorts/SZaQv0HgcMM">
  <img src="IMAGES/01_Componentes_del_sistema.png" width="270">
</a>

[Ver video](https://www.youtube.com/shorts/SZaQv0HgcMM)

</td>
</tr>
</table>

---

## 🧩 Tecnologías Utilizadas

| Tecnología | Aplicación |
|:----------|:-----------|
| **M5Stack AtomS3 Lite** | Nodo de adquisición, control local y comunicación inalámbrica |
| **DHT22** | Medición de temperatura y humedad relativa |
| **Relé** | Conmutación independiente del calefactor por estación |
| **Calefactor** | Actuador térmico independiente |
| **MicroPython / UIFlow 2.0** | Programación del firmware de cada nodo |
| **ESP-NOW** | Comunicación inalámbrica entre estaciones |
| **WiFi** | Conexión del nodo maestro con la red local |
| **HTTP** | Comunicación bidireccional entre nodo maestro y Node-RED |
| **MQTT / HiveMQ** | Intercambio de datos y comandos IoT |
| **Node-RED** | Dashboard local, supervisión y control |
| **ThingSpeak** | Visualización web, almacenamiento y canalización de datos |
| **MATLAB Analytics** | Cálculo de indicadores térmicos, lógica difusa y alertas |

---

## 🚀 Funcionalidades Principales

| Funcionalidad | Descripción |
|:-------------|:------------|
| 🌡️ **Monitoreo multiestación** | Supervisión simultánea de tres estaciones de trabajo independientes. |
| 📊 **Adquisición ambiental** | Medición en tiempo real de temperatura y humedad relativa mediante sensores DHT22. |
| 🔥 **Control local del calefactor** | Activación y desactivación por estación mediante relé independiente. |
| ⚙️ **Control por histéresis** | Operación automática con umbrales térmicos para reducir conmutaciones innecesarias. |
| 🎮 **Modo manual y automático** | Selección de modo de operación desde Node-RED o ThingSpeak. |
| 📡 **Comunicación ESP-NOW** | Intercambio de datos entre nodos sin conectar todas las estaciones al WiFi. |
| 🌐 **Nodo maestro IoT** | Pasarela entre la red ESP-NOW, Node-RED y la nube. |
| 🔁 **Comunicación HTTP bidireccional** | Transferencia de telemetría y comandos entre el nodo maestro y Node-RED. |
| ☁️ **Comunicación MQTT** | Intercambio bidireccional de datos entre Node-RED y ThingSpeak. |
| 🖥️ **Dashboard en Node-RED** | Interfaz local para visualización, control y seguimiento del sistema. |
| 🌍 **Página web en ThingSpeak** | Supervisión remota de variables, estados e indicadores térmicos. |
| 📈 **Registro histórico** | Almacenamiento de temperatura, humedad, estado del calefactor y modo de operación. |
| 🧠 **MATLAB Analysis** | Cálculo automático cada 15 minutos de indicadores térmicos avanzados. |
| 🌡️ **Índices térmicos** | Cálculo de Heat Index, punto de rocío, bulbo húmedo, WBGT e índice de disconfort. |
| 🚨 **Lógica difusa** | Clasificación del riesgo térmico mediante combinación de índices, tendencia y exposición. |
| 📧 **Alertas por correo** | Envío automático de reportes por estación mediante ThingSpeak Alerts. |
| 🔄 **Arquitectura modular** | Diseño replicable y escalable para incorporar nuevas estaciones de trabajo. |
| 🛡️ **Control autónomo local** | Cada estación mantiene el control térmico básico aunque falle la conexión con la nube. |

---

## 🧠 Indicadores Térmicos Calculados

| Indicador | Uso en el Sistema |
|:---------|:------------------|
| **Heat Index** | Estima la sensación térmica considerando temperatura y humedad relativa. |
| **Punto de Rocío** | Evalúa la carga de humedad ambiental. |
| **Bulbo Húmedo Estimado** | Aproxima el efecto de enfriamiento evaporativo. |
| **WBGT Estimado** | Evalúa la severidad térmica en ambiente interior. |
| **Índice de Disconfort** | Resume la incomodidad térmica percibida. |
| **PMV Estimado** | Evalúa sensación térmica promedio bajo supuestos de confort. |
| **PPD Estimado** | Estima el porcentaje de personas insatisfechas. |
| **Tendencia Térmica** | Detecta incremento o disminución reciente del Heat Index. |
| **Exposición Reciente** | Evalúa el tiempo acumulado en condiciones incómodas. |
| **RiskScore Difuso** | Puntaje final de riesgo térmico por estación. |

---

## 🚦 Clasificación del Riesgo Térmico

| Nivel | Estado | Interpretación |
|:----:|:------|:---------------|
| 0 | 🟢 **Confortable** | Condición térmica estable y aceptable. |
| 1 | 🟡 **Vigilancia** | Se recomienda seguimiento de la evolución térmica. |
| 2 | 🟠 **Precaución** | Condición incómoda o potencialmente riesgosa. |
| 3 | 🔴 **Alto** | Riesgo térmico elevado; requiere acción correctiva. |
| 4 | 🟣 **Crítico** | Condición térmica severa; requiere intervención inmediata. |

---

## 📡 Protocolos de Comunicación

| Tramo | Protocolo | Dirección | Datos principales |
|:-----|:----------|:----------|:------------------|
| Estaciones secundarias ↔ Nodo maestro | ESP-NOW | Bidireccional | Temperatura, humedad, estado del calefactor, modo y comandos |
| Nodo maestro ↔ Node-RED | HTTP sobre WiFi | Bidireccional | Telemetría agregada y control por estación |
| Node-RED ↔ ThingSpeak | MQTT | Bidireccional | Lecturas, estados, parámetros remotos y comandos |
| ThingSpeak → MATLAB Analysis | API interna | Periódica | Histórico por estación e indicadores térmicos |
| MATLAB Analysis → Correo | ThingSpeak Alerts | Salida | Nivel de riesgo, indicadores y recomendación |

---

## 🔄 Flujo General de Operación

```text
1. Cada estación mide temperatura y humedad relativa.
2. El nodo local procesa las lecturas del sensor DHT22.
3. El calefactor se controla por histéresis o por comando manual.
4. Las estaciones esclavas envían datos al nodo maestro mediante ESP-NOW.
5. El nodo maestro comunica la información hacia Node-RED por HTTP.
6. Node-RED actualiza el dashboard y gestiona comandos de control.
7. Node-RED intercambia datos con ThingSpeak mediante MQTT.
8. ThingSpeak almacena y visualiza los datos por estación.
9. MATLAB Analysis calcula indicadores térmicos cada 15 minutos.
10. La lógica difusa clasifica el riesgo térmico.
11. El sistema genera alertas y reportes por correo cuando corresponde.
```

---

## ✅ Resultados Esperados

- Supervisión térmica simultánea de tres estaciones.
- Control independiente del calefactor en cada puesto.
- Visualización local mediante Node-RED.
- Visualización remota mediante ThingSpeak.
- Comunicación distribuida mediante ESP-NOW.
- Registro histórico de variables ambientales.
- Diagnóstico térmico basado en lógica difusa.
- Alertas automáticas por estación.
- Arquitectura modular, replicable y escalable.

---

## 🧪 Alcance del Prototipo

Este sistema corresponde a un prototipo académico y experimental orientado a la supervisión térmica de estaciones de trabajo. Los sensores DHT22 permiten observar tendencias ambientales y validar la arquitectura IoT, pero no sustituyen instrumentos certificados para evaluación ocupacional formal. Para aplicaciones industriales o normativas, se recomienda calibrar sensores, verificar lecturas con instrumentos patrón e incorporar mediciones adicionales como velocidad del aire, temperatura radiante y condiciones de ventilación.

---

### ⭐ Proyecto académico de IoT, automatización y supervisión térmica inteligente

</div>
