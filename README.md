
# 🚗 Cyberpandino Cluster - PandaOS

[![Licencia: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)  
[![Versión](https://img.shields.io/badge/version-0.9.0-green.svg)](https://github.com/cyberpandino/cluster/releases)  
[![Node](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen.svg)](https://nodejs.org/)  
[![Plataforma](https://img.shields.io/badge/platform-Raspberry%20Pi%204B%2F5-red.svg)](https://www.raspberrypi.com/)  
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/cyberpandino/cluster/blob/main/.github/CONTRIBUTING.md)

Cuadro de instrumentos digital para Fiat Panda 141 basado en Raspberry Pi 4B.

---

## 📋 Descripción

Sistema completo de cuadro de instrumentos digital que sustituye la instrumentación analógica original del Fiat Panda 141.  
El sistema se conecta con la centralita mediante protocolo OBD-II (ELM327) y lee las luces testigo a través de optoacopladores conectados a los pines GPIO de la Raspberry Pi.

### Características Principales (v0.9.0)

- ✅ **Lectura de datos OBD-II**: Velocidad, revoluciones, temperatura, presión de aceite, etc.  
- ✅ **Detección de luces testigo del vehículo**: Largas, cortas, intermitentes, nivel de aceite, etc.  
- ✅ **Sensores externos**:  
  - Temperatura exterior (DS18B20)  
  - Nivel de combustible (ADS1115)  
- ✅ **Gestión del encendido**: Sistema de ahorro de energía automático  
- ✅ **Interfaz moderna**: Dashboard 3D con modelo Panda interactivo  
- ✅ **Modo demo**: Para desarrollo sin hardware  

---

## 📸 Vista previa
 <div align="center">
  <img src="docs/images/dashboard-main.png" alt="Dashboard principale" width="800"/>
  <p><em>Dashboard principale con modello 3D interattivo</em></p>
</div>

### Dashboard Principal

El cuadro digital sustituye completamente el tablero analógico original con una interfaz moderna y personalizable.

---

## 🗺️ Funciones Futuras

Consulta lo que estamos planeando: [Roadmap & Wishlist](ROADMAP.md)

Algunas ideas en lista:  
- 📹 Cámara trasera y sensores de aparcamiento  
- 🚪 Animaciones 3D avanzadas (puertas, luces)  
- 🎨 Dashboards y temas personalizables  
- 🌍 Internacionalización  
- 📱 App móvil compañera  
- ¡Y mucho más!  

---

## 📚 Índice de la Documentación

### 🚀 Empieza Aquí
- **[Inicio Rápido](QUICK_START.md)**  
- **[Hardware](HARDWARE.md)**  

### 📖 Documentación Técnica
- **[Arquitectura](ARCHITETTURA.md)**  
- **[Documentación General](DOCUMENTAZIONE.md)**  
- **[Configuración Cliente](client/CONFIGURAZIONE.md)**  
- **[Configuración Servidor](server/CONFIGURAZIONE_SERVER.md)**  
- **[Configuración Entorno](client/src/config/README.md)**  

### 🤝 Contribución
- **[Cómo Contribuir](.github/CONTRIBUTING.md)**  

### 📋 Otros
- **[Roadmap](ROADMAP.md)**  
- **[Autores](AUTHORS.md)**  
- **[Licencia](LICENSE)**  

---

## ⚠️ Aviso

PandaOS es un proyecto hobbístico y experimental.  
No es un producto certificado ni cumple estándares industriales o automotrices.  
Todo se ofrece “tal cual”, sin garantías de funcionamiento o compatibilidad.  
El uso en vehículos en circulación es **fuertemente desaconsejado**.  

---

## 🏗️ Arquitectura

El proyecto consta de tres módulos principales:


cluster/ ├── client/          → Interfaz gráfica (React + Vite + Electron) ├── server/          → Backend comunicación OBD-II y GPIO (Node.js) └── main.js          → Wrapper Electron para app de escritorio

### Tecnologías Usadas

- **Frontend**: React 18, TypeScript, Three.js, Socket.IO Client  
- **Backend**: Node.js, Socket.IO Server, SerialPort, GPIO (onoff)  
- **Desktop**: Electron 36  
- **Hardware**: Raspberry Pi 4B, ELM327, DS18B20, ADS1115  

---

## ⚙️ Requisitos del Sistema

### Software
- Node.js ≥ 18.0.0 (20.x LTS recomendado)  
- npm ≥ 9.0.0 (10.x recomendado)  
- Git ≥ 2.0  

### Hardware (Producción)
- Raspberry Pi 4B (4GB+) o Raspberry Pi 5  
- Adaptador ELM327 USB  
- Optoacopladores (PC817 o similares)  
- Pantalla LCD ultra-wide (1920×480 recomendado)  
- Sensores opcionales: DS18B20, ADS1115  

---

## 🚀 Configuración del Proyecto

1. Clonar repositorio  
2. Instalar dependencias: `npm run install:all`  
3. Configurar cliente y servidor  

---

## 🎯 Ejecución

- **Producción (Raspberry Pi)**: `npm start`  
- **Desarrollo (Mock)**: `npm run client`  

---

## 📦 Build Producción

- Cliente: `npm run build`  
- Electron: `npm run build:electron`  

---

## 📄 Licencia

GPL v3.0 o posterior.  

---

## 👥 Autores

- **ChatGPT**

---


