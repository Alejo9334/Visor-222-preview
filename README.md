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

## Optimización automática de imágenes PNG

Se activa la optimización de capas PNG en el flujo de publicación de la rama de desarrollo. Los originales se conservan y se utilizan WebP transparentes cuando reducen el peso. Primera prueba Minecraft: 4,08 MB → 1,15 MB (71,7 % menos). Informe visual: `optimizar.html`; la autenticación administrativa continúa pendiente y el visor público original no se modifica.

## Ajuste de texto del visor público

Bienvenida: «Tu imagen cobra vida». Instrucción: «Activa la cámara y apunta a una de las imágenes registradas». Actualización exclusiva de Preview.

## Texto de bienvenida · Opción 3

Título: «La magia está frente a ti». Descripción: «Activa tu cámara y observa cómo las imágenes cobran vida ante tus ojos». Se actualiza el Preview desde la rama de desarrollo, sin modificar la versión principal.

## Experiencia inmersiva con reconocimiento cinematográfico

La nueva vista previa incorpora una confirmación luminosa al reconocer imágenes, entrada progresiva por capas sin modificar las animaciones propias y un botón de vista inmersiva para celulares. Respeta la preferencia del sistema de reducir movimiento; la aplicación principal continúa intacta.

## Nuevo panel para registrar imágenes AR

Se añade `preparar-imagen.html`: imagen física JPG/PNG, hasta 15 capas PNG, ajustes de profundidad y animación, vista previa y generación de un único archivo JSON. Después de subirlo mediante la sesión autenticada de GitHub a `proyectos/pendientes/`, la acción de desarrollo añadirá el diseño al catálogo, organizará archivos, optimizará texturas y compilará el reconocimiento. Sin tokens en el navegador ni cambios a main.

## Editor visual local sin Supabase (Preview)

Se habilita `editor.html` sin inicio de sesión y se retiran las acciones de nube privada. El antiguo `login.html` redirige al editor. `preparar-imagen.html` permite crear paquetes JSON y la publicación requiere autenticación con permisos de escritura en GitHub. Los clientes utilizan únicamente el visor público. El código principal permanece sin modificar.

## Panel unificado de Visor-222

El editor visual (`editor.html`) ahora reúne creación y carga de referencia, selección múltiple de PNG, propiedades y animaciones, guardado local, importación/exportación JSON, y generación del paquete publicable del cuadro activo con comprobación de IDs ya publicados. La ruta anterior `preparar-imagen.html` redirige al editor. La publicación sigue requiriendo cuenta autorizada de GitHub; el cliente solo accede a `index.html`. No se modifica la aplicación principal.

## Emergencia cinematográfica 2.5D por imagen

Se incorporó en la rama de desarrollo el efecto de salida frontal progresiva de las capas PNG, con duración predeterminada de 1.4 segundos, escala inicial de 70 %, profundidad cinematográfica y destello opcional. El editor permite ajustar por cuadro duración, escala, intensidad, activación y brillo. El publicador preserva estos parámetros en el JSON del catálogo. MindAR, las imágenes de referencia y la aplicación principal no cambian. Respetar reducir movimiento del dispositivo.


### Actualización de vista previa

La vista previa se construye desde `public/prototipo-ar` de la rama `desarrollo/multicuadros-ar-v2` del repositorio `Visor-222`. Cada publicación de Preview copia el catálogo AR, el archivo de reconocimiento y los recursos de imagen desde esa rama.


### Reconocimiento AR y caché

Cada compilación de `targets.mind` incorpora una huella de contenido (`cacheKey`). El visor añade esa huella a la URL del archivo de reconocimiento para evitar que los dispositivos reutilicen una versión anterior desde la caché.


## Actualización 2.5D — profundidad y movimiento por capa

La Preview incorpora una entrada frontal cinematográfica con escalonado por profundidad, un pequeño rebote de llegada y movimiento ambiental independiente por capa PNG. El editor incluye el preset opcional «Aplicar profundidad + movimiento 2.5D», que distribuye Z y asigna flotación, pulso o giro a cada capa; el usuario puede seguir ajustándolas individualmente. Se mantienen MindAR, el catálogo multimarcador y los recursos existentes. Cambios desarrollados y validados únicamente en `desarrollo/multicuadros-ar-v2`.


Catálogo de demostración actualizado: Minecraft y Carnet utilizan ahora emergencia cinematográfica de 1,6 s, escala inicial del 62 %, profundidad Z escalonada y perfiles alternados de flotación, pulso y giro por capa. El archivo `targets.mind` fue recompilado en la rama de desarrollo con sus dos objetivos.


## Editor 3D de capas PNG

Preview incorpora un lienzo de capas en perspectiva 3D con vistas Perspectiva, Frontal, Lateral y Superior. Se añadió separación global entre PNG y ajuste individual de separación Z por capa. Los valores se conservan en el proyecto JSON, el publicador y el visor AR. La vista 3D es una representación de planos PNG (2.5D), no geometría 3D real. Los cambios están aislados en la rama `desarrollo/multicuadros-ar-v2`; la aplicación principal no se modifica.


## Editor ampliado: escala independiente y nuevas animaciones

La Preview sincroniza desde `Alejo9334/Visor-222`, rama `desarrollo/multicuadros-ar-v2`. El editor amplía la separación global entre PNG a 0–8% y la separación individual a ±8%; amplía posición X/Y a ±100%, profundidad a 100% y escala general a 300%. Añade escala horizontal X y vertical Y independientes (25–300%). Las animaciones independientes incluyen ahora Desplazamiento lateral y Balanceo 3D, además de Flotación, Pulso y Rotación. Los ajustes de separación y animación se conservan al preparar publicaciones y al compartir la vista previa mediante QR v2. La rama pública principal de Visor-222 no se modifica.
