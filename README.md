# d-Paspuel.github.io

# VitalReminder

Aplicación móvil para recordatorios de medicamentos y citas médicas, diseñada específicamente para adultos mayores.

## Características

- ✅ Interfaz accesible con alto contraste
- ✅ Botones grandes y fáciles de tocar
- ✅ Recordatorios de medicamentos
- ✅ Gestión de citas médicas
- ✅ Notificaciones al cuidador
- ✅ Funciona sin conexión
- ✅ Instalable como PWA

## Requisitos Previos

- *Node.js* 14.0 o superior ([Descargar](https://nodejs.org/))
- *npm* (incluido con Node.js)
- Para builds móviles:
  - *Android Studio* (para Android)
  - *Xcode* (para iOS - solo macOS)

## Instalación Rápida

### Windows

1. Haz doble clic en install.bat
2. Espera a que se complete la instalación
3. Ejecuta npm run dev en la carpeta ProyectoAnalisisIbero

### macOS / Linux

bash
cd ProyectoAnalisisIbero
npm install
npm run dev


## Estructura del Proyecto


VitalReminder/
├── install.bat                 # Script de instalación (Windows)
├── build-mobile.sh            # Script para builds móviles
├── capacitor.config.json      # Configuración de Capacitor
├── README.md                  # Este archivo
└── ProyectoAnalisisIbero/
    ├── package.json           # Dependencias del proyecto
    ├── vite.config.js         # Configuración de Vite
    ├── src/
    │   ├── main.js           # Punto de entrada
    │   ├── App.js            # Componente principal
    │   └── styles/
    │       └── global.css    # Estilos globales
    └── public/               # Archivos estáticos



## Comandos Disponibles

### Desarrollo

bash
# Navegar al directorio del proyecto
cd ProyectoAnalisisIbero

# Instalar dependencias (solo la primera vez)
npm install

# Ejecutar servidor de desarrollo
npm run dev


Accede a la aplicación en http://localhost:3000

### Producción

bash
# Compilar para producción
npm run build

# Vista previa de la build
npm run preview


Los archivos compilados estarán en la carpeta dist/

### Construcción Móvil (Opcional)

bash
# Desde el directorio raíz (VitalReminder/)
bash build-mobile.sh


Este script:
1. Compila la aplicación web
2. Instala las dependencias de Capacitor
3. Agrega soporte para Android e iOS
4. Sincroniza los archivos

*Después de ejecutar build-mobile.sh:*

bash
# Para abrir Android Studio
npx cap open android

# Para abrir Xcode (macOS solo)
npx cap open ios


## Desarrollo

### Estructura de Componentes


src/
├── components/
│   ├── screens/       # Pantallas principales
│   └── ui/            # Componentes UI reutilizables
├── services/          # Servicios (API, almacenamiento)
├── utils/             # Funciones auxiliares
├── hooks/             # Custom React hooks
├── context/           # React Context
└── styles/            # Estilos globales


### Stack Tecnológico

- *React* 18.2.0 - Interfaz de usuario
- *Vite* 4.4.0 - Herramienta de build
- *Capacitor* - Framework para aplicaciones multiplataforma
- *PWA* - Funcionalidad offline e instalable

## Solución de Problemas

### "npm command not found" / "npm no se encuentra"

*Solución:* Instala Node.js desde [nodejs.org](https://nodejs.org/)

### Puerto 3000 en uso

*Solución:* Edita vite.config.js y cambia el puerto:

javascript
server: {
  port: 3001,  // Cambia a otro puerto disponible
  open: true
}


### Errores en npm install

*Solución:* Limpia el cache de npm:

bash
npm cache clean --force
npm install


### Error en build-mobile.sh (Windows)

*Solución:* Asegúrate de tener Git Bash instalado, o ejecuta:

bash
# En PowerShell
bash ./build-mobile.sh


## Contribución

Las contribuciones son bienvenidas. Por favor:

1. Crea una rama para tu feature (git checkout -b feature/AmazingFeature)
2. Haz commit de tus cambios (git commit -m 'Add some AmazingFeature')
3. Push a la rama (git push origin feature/AmazingFeature)
4. Abre un Pull Request

## Licencia

Este proyecto está bajo la licencia MIT. Ver el archivo LICENSE para más detalles.

## Soporte

Para reportar bugs o sugerir mejoras, abre un issue en el repositorio.

---

*Última actualización:* Diciembre 2025
