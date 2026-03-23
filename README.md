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
pkg install nodejs git proot-distro python npm config set python python3 make clang build-essential nodejs-lts -y
```
 ### Configurar el entorno para node-gyp
Para saltarte el error del "Android NDK", a veces es necesario engañar al instalador o simplemente darle las herramientas que espera. Un truco muy efectivo en Termux es instalar binutils:
```bash
pkg install binutils
```

   
### 3. Instalar Gemini CLI
```bash
npm install -g @google/gemini-cli
```
### Instalar usando --unsafe-perm (si es necesario)
A veces, los permisos de las carpetas de Node en Termux causan el error ENOTEMPTY que viste al principio. Intenta la instalación así:
```bash
npm install -g @google/gemini-cli --unsafe-perm
```
### 💡 Solución alternativa (La más recomendada)
Si el error persiste debido a tree-sitter, que es muy pesado para compilar en móvil, te sugiero instalarlo de forma local en una carpeta de tu elección en lugar de global, o usar npx para ejecutarlo directamente:

1. Prueba con npx: (esto descarga y ejecuta sin instalar permanentemente si solo quieres probarlo)
```bash
npx @google/gemini-cli
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
