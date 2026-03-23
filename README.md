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
pkg install nodejs git proot-distro python npm config set python make clang build-essential nodejs-lts -y
```
 ### Configurar el entorno para node-gyp
Para saltarte el error del "Android NDK", a veces es necesario engañar al instalador o simplemente darle las herramientas que espera. Un truco muy efectivo en Termux es instalar binutils:
```bash
pkg install binutils
```

 ### Utiliza este comando para evitar errores:
```bash
mkdir -p "$HOME/.gyp" && printf "{'variables':{'android_ndk_path':''}}" > "$HOME/.gyp/include.gypi"
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
