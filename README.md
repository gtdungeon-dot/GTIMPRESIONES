# GT Impresiones Cotizador v2.0
## Guía Completa de Instalación y Uso

---

## 📁 ESTRUCTURA DEL PROYECTO

```
gt-impresiones-cotizador/
├── package.json          ← Configuración del proyecto
├── src/
│   ├── main.js           ← Proceso principal de Electron
│   ├── index.html        ← Interfaz principal
│   ├── styles.css        ← Estilos visuales
│   ├── app.js            ← Lógica de la aplicación
│   └── assets/
│       └── logo.png      ← Logo de GT Impresiones
```

---

## 🚀 PASOS PARA INSTALAR Y EJECUTAR

### Paso 1: Instalar Node.js
Si no lo tenés instalado:
1. Ir a https://nodejs.org
2. Descargar la versión **LTS** (la recomendada)
3. Instalarlo con las opciones por defecto

### Paso 2: Abrir la carpeta en VS Code
1. Abrir **Visual Studio Code**
2. `File` → `Open Folder...`
3. Seleccionar la carpeta `gt-impresiones-cotizador`

### Paso 3: Abrir la Terminal en VS Code
- Presionar **Ctrl + `** (la tecla del acento grave, abajo del Escape)
- O ir a `Terminal` → `New Terminal`

### Paso 4: Instalar dependencias
En la terminal, escribir y presionar Enter:
```bash
npm install
```
Esperar a que termine (puede tardar 1-2 minutos).

### Paso 5: Ejecutar la aplicación
```bash
npm start
```

¡La aplicación debería abrirse! 🎉

---

## 📦 COMPILAR EL INSTALADOR (.exe)

Para crear un instalador para Windows:
```bash
npm run build
```

El instalador se generará en la carpeta `dist/`.

---

## 🔐 CREDENCIALES DE ACCESO
- **Usuario:** GT
- **Contraseña:** 147

---

## ✨ NOVEDADES DE LA VERSIÓN 2.0

### 🎨 Diseño rediseñado
- Inspirado en la estética limpia y profesional de BambuStudio
- Fuente **Poppins** en toda la aplicación
- Paleta rojo, blanco y negro/gris oscuro
- Barra de título con botones nativos (minimizar, maximizar, cerrar)

### 🌗 Modo Día / Modo Noche
- Botón en la barra lateral para cambiar entre temas
- El modo día usa fondos claros, el modo noche fondos oscuros

### 💾 Datos guardados automáticamente
Los siguientes valores se guardan y no hay que reingresar cada vez:
- Precio del kg de filamento
- Precio de venta del filamento
- Precio por hora de kW
- Precio por hora de uso del equipo
- Margen porcentual por fallas

Para modificarlos, ir a la pestaña **Configuración**.

### 📊 Calculadora simplificada
En la pantalla principal solo se ingresa:
1. **Peso de la pieza** (en gramos)
2. **Horas de impresión**

El resto se calcula automáticamente con los parámetros guardados.

### 📂 Historial mejorado
Al guardar un cálculo:
- Se pide un **nombre** para identificar la pieza
- Se puede agregar una **foto** de la pieza (opcional)
- El historial muestra las piezas con imagen y datos clave
- Se puede ver el detalle completo de cada cotización
- Se pueden eliminar entradas individualmente

### 🖼️ Logo sin fondo
El logo de GT Impresiones se muestra correctamente sin el fondo negro.

---

## ❓ SOLUCIÓN DE PROBLEMAS COMUNES

**"npm no se reconoce como comando"**
→ Reiniciar VS Code después de instalar Node.js

**"Cannot find module 'electron'"**
→ Correr `npm install` nuevamente

**La app no abre o da error**
→ Verificar que estés en la carpeta correcta con `ls` (Mac/Linux) o `dir` (Windows)
→ Asegurarse de que el archivo `src/assets/logo.png` exista

---

## 📍 DÓNDE SE GUARDAN LOS DATOS

Los datos se guardan automáticamente en:
- **Windows:** `C:\Users\TuUsuario\AppData\Roaming\gt-impresiones-cotizador\`
- Archivo `config.json` → parámetros de configuración
- Archivo `history.json` → historial de cotizaciones
- Carpeta `images/` → imágenes de las piezas
