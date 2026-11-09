# Visor-222-preview
Pruebas de realidad aumentada

## Actualización: corrección de texturas PNG

Se actualizará automáticamente desde la rama `desarrollo/multicuadros-ar-v2` para utilizar materiales transparentes de Three.js y evitar planos blancos. La página pública principal no cambia.

## Editor visual de capas (v2)

La vista previa incluye `editor.html` con posición, profundidad, escala, rotación, visibilidad, animaciones individuales, guardado local, exportación de JSON y prueba AR. Esta ejecución actualiza el sitio desde la rama de desarrollo; no modifica la aplicación principal.

## Vista previa de capas por QR entre PC y celular

El editor ahora permite **Probar en mi celular · QR**. El enlace incluye los parámetros actuales de las cinco capas originales y el visor los aplica sin cambiar la publicación principal. Esta actualización ejecuta la publicación del sitio de pruebas.

## Administrador de múltiples cuadros

Esta publicación incorpora una lista de obras, creación de cuadros con imagen objetivo y capas PNG independientes, duplicación con nueva referencia, reordenación, eliminación, importación/exportación JSON y prueba de reconocimiento de múltiples objetivos AR con almacenamiento temporal IndexedDB. Los diseños nuevos solo se guardan localmente; no hay publicación automática ni autenticación.

## Acceso privado administrativo — integración preparada

El editor requiere una sesión Supabase autorizada; sin configurar URL y publishable key en la rama de desarrollo permanecerá cerrado. Se incluye login.html, admin-auth.js y SQL RLS. El visor público continúa disponible. Esta actualización despliega el cambio sin modificar Visor-222/main.

## Publicación controlada del catálogo (fase de pruebas)

El convertidor de proyectos JSON ya se validó con el cuadro Creeper. El flujo «Publicar catálogo AR en desarrollo» actualiza únicamente la rama de desarrollo de Visor-222. Este sitio Preview también comprueba periódicamente cambios de esa rama. La autenticación Supabase sigue pendiente; nunca se usa una contraseña en el código público.

## Optimización de reconocimiento v3

El catálogo publicado incluye `targets.mind` generado antes de llegar al celular y el visor lo utiliza directamente. Para múltiples cuadros, únicamente se cargan al inicio las capas PNG de la primera obra; las demás se descargan al reconocer la referencia. Supabase permanece pendiente. Sin cambios en la versión principal.
