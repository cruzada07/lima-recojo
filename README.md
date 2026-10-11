# LimaRecojo

> **¡Que no te deje el camión!** Sistema de rastreo en tiempo real y alertas sonoras personalizadas para la recolección de basura urbana en Lima.

---

## 🇵🇪 Sobre el Proyecto

¿Cuántas veces has escuchado la mítica campanita o melodía del camión de la basura cuando ya estaba a tres cuadras y tuviste que salir corriendo en chancletas? 

**LimaRecojo** nace para solucionar ese clásico dilema limeño. Es una plataforma web ligera y accesible que le permite a los vecinos ver en un mapa interactivo la ubicación exacta y en tiempo real del camión de basura que se aproxima a su zona.

Además, te permite configurar una **alerta preventiva en tu celular** (5, 10 o 15 minutos antes) acompañada de tu sonido preferido: desde la clásica melodía municipal hasta tus temas peruanos favoritos o un audio personalizado grabado por ti.

---

## Características Principales

* 📍 **Rastreo en Vivo:** Visualiza en tiempo real solo los camiones que aún no han pasado por tu tramo de calle.
* ⏰ **Alertas Personalizadas:** Elige con cuánta anticipación deseas recibir el aviso (5, 10 o 15 minutos aproximados).
* 🔊 **Sonido a tu Gusto:**
  * La inolvidable melodía oficial del camión de basura de tu distrito.
  * Una selección de canciones peruanas conocidas.
  * Subida de tu propio archivo de audio personalizado.
* ⚡ **Ultra Ligero:** Diseñado para consumir el mínimo de datos móviles tanto en la app del ciudadano como en el emisor GPS del vehículo.

---

## Arquitectura y Tecnologías

* **Frontend Ciudadano:** HTML5, CSS3, JavaScript (ES6+), Leaflet.js para el mapa interactivo.
* **Backend / Streaming:** Node.js, Express y WebSockets (`socket.io`) para el envío continuo de coordenadas GPS.
* **Geolocalización:** API de Geolocation del navegador + cálculo espacial de distancia y tiempo estimado (ETA).

---

## Estructura del Repositorio

* `src/backend/`: API REST y servidor WebSocket para gestión de rutas y alertas.
* `src/frontend/`: Interfaz web para el vecino, mapa interactivo y selector de audios.
* `src/driver-app/`: Aplicación ultra sencilla para la transmisión GPS desde el vehículo de recojo.
* `docs/`: Guías técnicas, arquitectura y detalles de implementación.

---

## Guía de Instalación y Uso Local

### Requisitos Previos

* Node.js (versión 18 o superior)
* Git

### Pasos de Configuración

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/cruzada07/lima-recojo.git
   cd lima-recojo
   ```

2. **Instalar dependencias del servidor:**
   ```bash
   cd src/backend
   npm install
   ```

3. **Configurar variables de entorno:**
   Copia el archivo `.env.example` a `.env` en la carpeta `src/backend/`:
   ```bash
   cp .env.example .env
   ```

4. **Iniciar el servidor:**
   ```bash
   npm run dev
   ```

5. **Probar la interfaz:**
   Abre el archivo `src/frontend/index.html` en tu navegador favorito.

---

## Contribuir
¡Las contribuciones son más que bienvenidas! Si tienes ideas para mejorar la precisión del tiempo estimado, sumar nuevos audios tradicionales o mejorar la interfaz, no dudes en aportar.

1. Haz un Fork de este repositorio.
2. Crea tu rama de características: `git checkout -b feature/nueva-funcionalidad`
3. Guarda tus cambios: `git commit -m "Agrega nueva funcionalidad"`
4. Haz Push a la rama: `git push origin feature/nueva-funcionalidad`
5. Abre un Pull Request.

---

## Licencia
Este proyecto se distribuye bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

---

*Hecho con cariño para una Lima más limpia y organizada.*
