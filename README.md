# Pulso Eléctrico

**Lo que mueve la energía.** Web editorial estática, responsive y compatible con GitHub Pages. HTML y CSS completos, sin instalación, JavaScript, fuentes externas ni dependencias.

## Qué incluye

- `index.html`: portada, última edición, archivo, suscripción y feedback.
- `assets/styles.css`: diseño compartido de todas las páginas.
- `assets/logo.png` y `assets/favicon.ico`: símbolo original de pulso eléctrico.
- `ediciones/2026-09-28.html` y `2026-09-29.html`: demostraciones editoriales.
- `ediciones/2026-09-30.html`: borrador de la siguiente edición, sin enlace desde portada.
- `.nojekyll`: publicación directa de los archivos estáticos.

Las muestras NO son noticias contrastadas. Los nueve bloques muestran temas y estructura; los botones de noticias están desactivados hasta añadir fuentes. Los mercados muestran N/D, nunca cotizaciones inventadas. Un archivo subido a un repositorio público es público aunque no esté enlazado: no subas borradores confidenciales.

## 1. Crear el repositorio

Tu repositorio `PulsoELECTRICO/pulso-electrico` ya existe: no necesitas crear otro. Para repetir el proceso desde cero, en GitHub pulsa **+ → New repository**, escribe `pulso-electrico`, elige **Public**, marca añadir README y pulsa **Create repository**. Usa un repositorio público para alojarlo con GitHub Free.

## 2. Subir los archivos sin programar

1. Descomprime el ZIP de la web en tu ordenador.
2. Entra en el repositorio y abre **Code**.
3. Pulsa **Add file → Upload files**.
4. Arrastra el CONTENIDO de la carpeta `pulso-electrico`: `index.html`, `README.md`, `.nojekyll`, `assets` y `ediciones`. No arrastres la carpeta contenedora ni el ZIP: `index.html` debe quedar en la raíz del repositorio.
5. Escribe «Publicar web de Pulso Eléctrico» y pulsa **Commit changes**. Si ya existen index y README, se actualizarán; el historial permite recuperar versiones anteriores.

Para probarla antes, abre `index.html` con doble clic. Conserva las carpetas a su lado para que los estilos y enlaces funcionen.

## 3. Activar GitHub Pages

1. Abre **Settings → Pages**, no Branches.
2. En **Build and deployment → Source**, selecciona **Deploy from a branch**.
3. Elige **main** y **/(root)**. Pulsa **Save**.
4. Espera a que termine el despliegue. Puedes consultar su estado en **Actions**.
5. Abre `https://pulsoelectrico.github.io/pulso-electrico/`.

Si aparece 404, comprueba que `index.html` está en la raíz, que el despliegue terminó y que la dirección incluye `/pulso-electrico/`. GitHub distingue mayúsculas y minúsculas en los nombres de archivos.

Referencia: [configuración oficial de GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## 4. Publicar una edición diaria

1. Copia una edición en tu ordenador y llámala `AAAA-MM-DD.html`, por ejemplo `2026-10-01.html`. Usa un editor de texto (Bloc de notas sirve), no Word. Guarda en UTF-8 y selecciona todos los tipos para evitar una extensión `.txt`.
2. Cambia el título de la pestaña (`<title>`), los metadatos, el día de la semana, la fecha visible y el titular principal (`<h1>`).
3. Completa los nueve artículos: tres en Lo imprescindible, tres en España, dos europeos y uno del resto del mundo. Incluye fuente, resumen propio y por qué importa. No presentes los textos orientativos de la muestra como noticias del día.
4. Sustituye cada botón desactivado por un enlace a la noticia original, por ejemplo:

```html
<a class="btn" href="URL_COMPLETA_DEL_ARTICULO">Leer noticia ↗</a>
```

5. En mercados, incorpora precio, unidad, fuente enlazada, fecha/hora y zona horaria de corte, contrato y vencimiento. OMIE es la referencia para el precio diario español, no otro indicador que se deba duplicar. Para YR-27 usa el futuro base español con entrega en 2027. Para TTF y Brent identifica el mes exacto del contrato. Mantén N/D si no hay un dato verificado.
6. Compara cotizaciones homogéneas. Con precio anterior positivo: `(actual / anterior - 1) * 100`. Si el precio anterior es cero o negativo, informa de la diferencia absoluta con su unidad. Usa ↑, ↓ o → y texto; nunca solo color.
7. Una vez revisadas las nueve noticias, fuentes y datos, retira el aviso de demostración de esa edición.
8. En `index.html`, cambia LOS DOS enlaces a la última edición: el de «Leer última edición» y el de «Leer newsletter». Actualiza fecha, titular, resumen y los temas del recuadro lateral. Retira el aviso de muestra solo cuando esa edición sea real.
9. Añade una tarjeta al principio del archivo, copiando un bloque `<article class="card">…</article>`. Actualiza fecha, título, URL y etiqueta accesible. Mantén el orden de más reciente a más antigua. No enlaces una edición futura antes de publicarla.
10. Sube la edición y el `index.html` actualizado en el mismo commit. Abre la web publicada y prueba ambos botones, el archivo y una noticia en móvil.

El archivo incluye inicialmente la edición del 29 como acceso adicional, siguiendo el ejemplo solicitado. Puedes reservar «Ediciones anteriores» exclusivamente a días previos retirando esa tarjeta duplicada.

## 5. Suscripciones, feedback y privacidad

«Quiero apuntarme» abre el correo a `juanmcalvo33@gmail.com` con el asunto solicitado. «Ayúdanos a mejorar» hace lo mismo con el asunto de feedback. El visitante necesita una aplicación de correo configurada. No existe envío automático, almacenamiento de suscriptores ni confirmación de alta en GitHub Pages. Gestiona la solicitud y la confirmación por email; no publiques direcciones de suscriptores en el repositorio.

El pie incluye información básica y real sobre el funcionamiento actual, sin enlaces legales ficticios. Antes de operar una lista de distribución, completa la información de privacidad con la identidad del responsable, finalidad, base jurídica, conservación, proveedores, derechos y canal de ejercicio aplicables a tu operativa. Adapta estos textos si incorporas formularios, analítica o un proveedor de email.

## 6. Dominio propio en el futuro

El alojamiento puede seguir siendo gratuito; registrar y renovar `pulsoelectrico.es` tiene un coste aparte y su disponibilidad no se ha comprobado.

1. Registra el dominio con un proveedor de tu elección.
2. Verifica su propiedad en la configuración de Pages de tu cuenta con el registro TXT que indique GitHub.
3. En el repositorio, **Settings → Pages → Custom domain**, introduce `pulsoelectrico.es` y guarda ANTES de apuntar el DNS.
4. En el proveedor del dominio, configura cuatro registros A para `@` con estos destinos: `185.199.108.153`, `185.199.109.153`, `185.199.110.153` y `185.199.111.153`. Para `www`, crea un CNAME a `pulsoelectrico.github.io`, sin `https://` y sin `/pulso-electrico/`.
5. Espera la propagación y activa **Enforce HTTPS** cuando esté disponible. Conserva el archivo CNAME que GitHub genera al publicar desde una rama.

Comprueba los valores vigentes al realizar el cambio en la [guía oficial de dominios de GitHub](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site). Los enlaces relativos de esta web funcionan tanto en la ruta del repositorio como en la raíz de un dominio propio.

## 7. Automatización recomendada

Primero valida el formato editorial con el proceso manual. Después separa contenido y diseño: guarda cada edición en Markdown o JSON y genera las páginas con un generador estático. Un único listado de ediciones puede producir la portada, el archivo y la última edición, evitando editar dos enlaces a mano.

Como siguiente fase, utiliza GitHub Actions para generar y desplegar el sitio tras aprobar un pull request. Más adelante, una tarea programada puede preparar un borrador diario con fuentes autorizadas, fecha de corte y comprobación de enlaces. Mantén revisión editorial antes de publicar; si faltan fuentes o cotizaciones, conserva N/D y no fabrique datos. GitHub Pages no envía newsletters: esa parte requiere un servicio de distribución separado.

Para un despliegue automatizado usa **Source: GitHub Actions** y la plantilla oficial de sitio estático (checkout, generación/validación, upload-pages-artifact y deploy-pages). No dependas de que un commit creado con GITHUB_TOKEN dispare la publicación desde rama: GitHub indica que esos commits no activan ese proceso. Los horarios de Actions se expresan en UTC y pueden retrasarse; para España hay que contemplar el cambio horario. Guarda claves en Secrets, nunca en HTML ni en archivos públicos. Esta entrega no activa ninguna tarea ni conecta servicios externos.

## Diseño y mantenimiento

Colores: azul `#087ede`, verde `#21b573`, azul oscuro `#073f3a`, texto `#08263d`. Tipografía del sistema para carga rápida. El CSS compartido está en `assets/styles.css`; modifica ese archivo para cambiar todo el sitio. Incluye salto al contenido, foco de teclado, jerarquía semántica, diseño móvil, tablas desplazables y estilos de impresión.
