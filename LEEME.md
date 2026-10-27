# Mi Cuarto UT - Brian Garcia Rueda

HTML5, CSS y JavaScript con servidor Node.js y base SQLite. Implementación visual basada en el maquetado v02. Instagram: https://www.instagram.com/micuartout/ .

## Ejecutar en Visual Studio Code

1. Descomprime el ZIP y abre `Mi-Cuarto-UT.code-workspace`.
2. Necesitas Node.js 22.13 o superior: https://nodejs.org/ .
3. En la terminal de esta carpeta ejecuta `npm start` o `node server.mjs`.
4. Abre http://127.0.0.1:8788/ . También puedes ejecutar `INICIAR_WINDOWS.cmd`.

No necesitas instalar paquetes ni copiar contraseñas del propietario. No abras solo el HTML con Live Server: ese modo no ejecuta la API ni conecta SQLite. Si el puerto 8788 ya está ocupado por esta misma aplicación, utiliza la sesión que ya está ejecutándose.

## Publicación actual

Página gratuita: https://mi-cuarto-ut-brian-gr.surge.sh/ . Surge aloja permanentemente los archivos de la interfaz mientras se conserve la cuenta y el servicio.

**Límite importante:** la API usa actualmente un túnel HTTPS temporal a este equipo. El catálogo dinámico, las cuentas y los formularios necesitan que Node.js, el túnel y el equipo permanezcan activos. Esto no es un backend administrado permanente. Si se apagan, permanece disponible el catálogo estático de ejemplos con un aviso de desconexión; no se simula el registro de datos. El dominio del túnel cambia al reiniciarlo. El servidor puede instalarse posteriormente en un alojamiento Node.js con disco persistente; no debe desplegarse SQLite en un disco efímero.

La dirección del servidor público está en `public/config.js`. En ejecución local se utiliza el mismo servidor de la página, sin conexión con el alojamiento anterior. No se requieren Vercel, extensiones, una cuenta de ChatGPT ni claves de servicios externos.

## Datos y archivos

- `public/index.html`, `styles.css` y `app.js`: interfaz separada, navegación, filtros, mapa esquemático y formularios.
- `server.mjs`: servidor HTTP, archivos estáticos, límites de tamaño y CORS.
- `api.mjs`: catálogo, favoritos, perfiles, anuncios, fotografías, contacto y reportes.
- `runtime.mjs`: SQLite, registro, acceso con contraseña, sesiones y archivos.
- `database/mi_cuarto_ut.sqlite`: referencia inicial limpia con seis anuncios ilustrativos.
- `data/`: se crea al ejecutar. Conserva la base activa y las fotos. No la borres ni la publiques como archivos estáticos. Respalda esta carpeta con el servidor detenido.
- `tests/api.mjs`: 54 comprobaciones de integración. Solo contra el servidor técnico del puerto 8790 y una base de pruebas separada. Resultado en `tests/pruebas-api.json`.
- `api-source.ts` y `catalog-source.ts`: referencias de procedencia de la adaptación; el programa ejecuta las versiones JavaScript `.mjs`.

Las cuentas, solicitudes y fotos privadas de producción no se incluyen en el ZIP. El primer inicio crea una base independiente desde los seis ejemplos; no es una migración de las cuentas del proveedor anterior.

## Funciones y límites

Registro e inicio de sesión propios; contraseñas con scrypt y sal aleatoria; sesiones de 24 horas; permisos por cuenta; catálogo SQL; filtros; favoritos; perfiles de estudiante, maestro y rentador; carga de JPG/PNG/WebP de hasta 5 MB; edición, borrador, pausa y retiro; contactos del rentador entregados solo con sesión; solicitudes con folio y reportes persistentes.

El correo de registro no está verificado. No se implementaron recuperación automática de contraseña, notificaciones por correo, pagos, contratos ni verificación de inmuebles. El formulario de contacto guarda datos y devuelve un folio: no envía mensajes de correo automáticamente. No hay panel administrativo de solicitudes.

El mapa, fotografías y precios iniciales son ejemplos, no inventario real. La geografía definitiva continúa pendiente ante las discrepancias de los documentos. Se conserva la paleta #0D3B66, #00B894, #E5E7EB y #1F2937, Montserrat y la licencia de la fuente en `public/assets/`.
