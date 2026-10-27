# Mi Cuarto UT

Tu espacio, más cerca de la universidad.

Plataforma de alojamiento universitario para consultar y publicar cuartos, habitaciones y departamentos. Versión independiente con HTML5, CSS, JavaScript, Node.js y SQLite, sin dependencias externas de npm.

## Ejecutar

Requiere Node.js 22.13 o superior.

```bash
npm start
```

Abre http://127.0.0.1:8788/ . En Windows también puedes usar `INICIAR_WINDOWS.cmd`. Consulta `LEEME.md` para la descripción completa de ejecución y límites.

## Código

- `public/`: interfaz, fotografías ilustrativas, tipografía y configuración pública de la API.
- `server.mjs`: servidor HTTP y CORS.
- `runtime.mjs`: SQLite, cuentas, contraseñas protegidas y sesiones.
- `api.mjs`: catálogo, filtros, perfiles, favoritos, anuncios, fotografías, solicitudes y reportes.
- `database/`: esquema SQL y base inicial limpia con seis ejemplos.
- `tests/`: comprobaciones de integración para una base de pruebas separada.

## Estado

Interfaz publicada: https://mi-cuarto-ut-brian-gr.surge.sh/ . La API documentada depende de este equipo y de un túnel temporal; su alojamiento permanente sigue pendiente. Los anuncios iniciales, fotos, precios y mapa son demostrativos. No se consideran ofertas verificadas ni resultados de mercado.

El registro de pruebas existente documenta 54 comprobaciones aprobadas el 20 de octubre de 2026. No se presenta como una nueva ejecución de pruebas en cada commit.

## Avances en GitHub

Repositorio: https://github.com/BrianGarciaR/Mi-Cuarto-UT . La importación inicial conserva el estado actual del código; no reconstruye un historial ficticio de desarrollo. Los siguientes cambios solicitados se registrarán con commits descriptivos en este mismo repositorio.

Las bases activas, sesiones, fotos privadas, archivos `.env` y datos de pruebas están excluidos mediante `.gitignore`. La base inicial incluida contiene únicamente seis anuncios de ejemplo y ninguna cuenta ni solicitud real.
