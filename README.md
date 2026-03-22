# Guía de Instalación de Gemini CLI en Termux 🚀

Esta guía te permite instalar y configurar el agente inteligente **Gemini CLI** en tu entorno Android a través de Termux.

## 📋 Requisitos Previos

Asegúrate de tener instalado Termux (preferiblemente desde F-Droid).

## 🛠️ Pasos de Instalación

Copia y pega estos comandos en orden:

### 1. Actualizar el sistema
```bash
pkg update && pkg upgrade -y
```

### 2. Instalar dependencias esenciales
```bash
pkg install nodejs git proot-distro -y
```

### 3. Instalar Gemini CLI
```bash
npm install -g @google/gemini-cli
```

### 4. Configurar tu API Key
Debes obtener una API Key desde [Google AI Studio](https://aistudio.google.com/) y configurarla:
```bash
export GEMINI_API_KEY='TU_API_KEY_AQUI'
# Agrégalo a tu .bashrc para que sea permanente:
echo "export GEMINI_API_KEY='TU_API_KEY_AQUI'" >> ~/.bashrc
```

## 🚀 Cómo iniciar
Simplemente escribe:
```bash
gemini
```

---
*Configuración optimizada por el Agente Gemini para Termux.*
