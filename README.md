# Alisio Estudio — Portfolio web

[Castellano](#castellano) · [English](#english)

## Castellano

### Qué es y para qué sirve

Alisio Estudio es una primera versión de un portfolio comercial de diseño web dirigido a negocios de la zona y de la provincia de Santa Cruz de Tenerife. Su objetivo es mostrar distintas direcciones visuales y funciones que podrían adaptarse a empresas sin página web o con una web que necesite mejoras.

El portfolio permite enseñar ejemplos durante una reunión, explicar servicios de diseño y desarrollo, y concretar las necesidades de un posible cliente antes de preparar una propuesta.

**Estado:** prototipo estático e interactivo. Alisio Estudio es un nombre provisional; Brasa & Sal, Nativa y Trazo son marcas ficticias. No representan clientes ni encargos realizados. Las demos se abren en ventanas de diálogo dentro de una misma página; no son tres webs completas e independientes. La interfaz de la web está en castellano; este README es bilingüe.

### Trabajo realizado

- Creación de una identidad visual provisional para el estudio: tonos verdes, fondo claro, acento lima, tipografía de sistema y detalles editoriales.
- Desarrollo de una página principal con presentación, galería de conceptos, funcionalidades, proceso de trabajo y formulario para definir un proyecto.
- Creación de tres composiciones visuales diferentes para restauración, belleza y servicios profesionales.
- Programación de una carta filtrable, una simulación de reserva y un generador de resumen de solicitud de reforma.
- Incorporación de un formulario general que prepara un resumen del negocio, su situación actual y su objetivo, con un botón para copiarlo.
- Diseño con reglas adaptables a móvil y escritorio, navegación por anclas y elementos gráficos dibujados con CSS.
- Inclusión de etiquetas de formulario, indicadores de foco, mensajes de estado, diálogos nativos y soporte para la preferencia de movimiento reducido. Esto no equivale a una auditoría completa de accesibilidad.
- Separación del contenido, los estilos y las interacciones en HTML, CSS y JavaScript, sin frameworks ni dependencias externas.
- Preparación de esta documentación en castellano e inglés y de instrucciones de ejecución y personalización.

### Tipos de web del portfolio

| Concepto | Para qué sirve | Funciones implementadas | Posibles ampliaciones, todavía no implementadas |
| --- | --- | --- | --- |
| **Brasa & Sal — Restauración** | Presentar la oferta de restaurantes, cafeterías o bares y facilitar la consulta de la carta desde el móvil. | Carta de ejemplo con nombres, descripciones y precios; filtros de Todos, Entrantes, Principales y Postres. | Carta accesible por QR, alérgenos validados, idiomas, horarios, ubicación, reservas de mesa y pedidos conectados a un sistema real. |
| **Nativa — Belleza y cuidado personal** | Mostrar servicios de peluquerías, barberías o centros de estética y explicar cómo sería pedir una cita. | Selector de servicio, fecha y hora orientativa; fecha mínima según el día local; resumen de reserva simulada. | Agenda real, disponibilidad por profesional, duración y precio de servicios, confirmaciones, recordatorios, cancelaciones y galería de trabajos autorizados. |
| **Trazo — Reformas y servicios profesionales** | Recoger necesidades iniciales para que una empresa de reformas o un profesional pueda preparar una primera conversación. | Selección del tipo de reforma, superficie aproximada y plazo deseado; generación local de un resumen. | Envío de solicitudes, carga de fotografías, visitas, seguimiento de contactos, proyectos realizados y presupuestos revisados por el profesional. |
| **Alisio Estudio — Web de presentación comercial** | Reunir los conceptos y explicar el servicio del estudio a posibles clientes. | Galería con demos, sección de funcionalidades, proceso de trabajo y resumen copiable de un proyecto. | Contacto real, casos de clientes con autorización, paquetes de servicios, dominio definitivo y contenidos específicos por sector. |

Las ampliaciones son posibilidades de desarrollo, no prestaciones que ya estén disponibles ni resultados comerciales garantizados.

### Cómo funcionan las interacciones

1. **Carta:** abrir Brasa & Sal y seleccionar una categoría. JavaScript muestra los platos correspondientes.
2. **Reserva:** abrir Nativa, elegir servicio, fecha y hora y pulsar «Simular reserva». Se muestra un mensaje; no se reserva ningún hueco.
3. **Solicitud:** abrir Trazo, elegir el trabajo, introducir una superficie de entre 1 y 10.000 m² y seleccionar el plazo. Se genera un resumen; no se calcula un precio ni se envía una consulta.
4. **Resumen general:** indicar tipo de negocio, situación y objetivo al final del portfolio. El texto puede copiarse para utilizarlo después en una conversación comercial.

No hay servidor de aplicación, base de datos, cuentas, pagos, analítica ni integración de correo o agenda. Los formularios no transmiten ni guardan sus datos de forma persistente. Al recargar la página se pierde el resumen generado. El botón de copiar utiliza el portapapeles del navegador; si no está disponible, se indica cómo copiar manualmente.

### Archivos del proyecto

| Archivo | Función |
| --- | --- |
| `dist/index.html` | Estructura y contenido de la página principal, tarjetas, formularios y contenedor de demos. |
| `dist/style.css` | Identidad visual, ilustraciones CSS, distribución, adaptación de pantalla y estados de foco. |
| `dist/app.js` | Datos ficticios, filtros, diálogos, validación nativa de formularios, resúmenes y copia. |
| `README.md` | Documentación bilingüe del proyecto. |
| `LEEME.md` | Acceso breve a la documentación principal. |
| `.gitignore` | Exclusión de configuración local, archivos temporales y posibles secretos. |

La carpeta `dist` contiene directamente el código editable de la web; no es el resultado de una compilación. La configuración local de alojamiento no es necesaria para ejecutar estas demos.

### Abrir el proyecto

**Sin instalar herramientas:** abrir `dist/index.html` en un navegador moderno, manteniendo los tres archivos de `dist` juntos.

**Con un servidor local opcional**, desde la raíz del proyecto y con Python instalado:

```sh
python -m http.server 8000 --directory dist
```

Después abrir `http://localhost:8000`. No se necesita `npm install` ni un proceso de compilación. Para comprobar la sintaxis de JavaScript, con Node.js instalado:

```sh
node --check dist/app.js
```

### Personalización

Editar textos y estructura en `dist/index.html`, colores y composición en `dist/style.css`, y platos, servicios y comportamientos en `dist/app.js`. Sustituir los datos ficticios por información validada con cada negocio. Mantener las advertencias de simulación mientras no existan integraciones reales.

### Verificación y siguientes pasos

La comprobación de sintaxis de JavaScript se ha realizado correctamente. La revisión visual y las pruebas funcionales completas en navegador siguen pendientes: el entorno anterior bloqueó la vista previa local. Tampoco hay un despliegue web confirmado. Guardar el código en GitHub no publica por sí solo una web navegable.

Antes de utilizarlo como servicio operativo: confirmar marca y contacto, revisar en móvil y escritorio, probar teclado y formularios, acordar contenido y alcance con el cliente y conectar los servicios reales necesarios. Para publicar, servir el contenido de `dist` en un alojamiento estático. Si se elige GitHub Pages, hay que configurar la publicación de esa carpeta mediante un flujo de despliegue o adaptar la estructura; no hay ningún flujo incluido.

No se incluye una licencia de software de código abierto. Su elección queda pendiente del titular del proyecto.

---

## English

### What it is and what it is for

Alisio Estudio is an initial commercial web design portfolio aimed at businesses in the area and province of Santa Cruz de Tenerife. It demonstrates visual directions and features that could be adapted for companies without a website or whose existing website needs improvement.

The portfolio can support sales meetings, explain design and development services, and clarify a prospect's needs before preparing a proposal.

**Status:** an interactive static prototype. Alisio Estudio is a provisional name; Brasa & Sal, Nativa and Trazo are fictional brands. They are not clients or completed commissions. The demos open in dialogs within a single page; they are not three complete standalone websites. The website interface is in Spanish; this README is bilingual.

### Work completed

- Created a provisional studio identity using green tones, a light background, a lime accent, system fonts and editorial details.
- Built a main page with an introduction, concept gallery, features, working process and project brief form.
- Designed three distinct visual compositions for hospitality, beauty and professional services.
- Implemented a filterable menu, a booking simulation and a renovation enquiry summary generator.
- Added a general form that produces a copyable summary of the business, its current situation and its goals.
- Added responsive CSS rules for mobile and desktop, anchor navigation and CSS illustrations.
- Included form labels, focus indicators, status messages, native dialogs and reduced-motion support. These measures do not constitute a full accessibility audit.
- Separated content, styles and interactions into HTML, CSS and JavaScript, without frameworks or external dependencies.
- Prepared Spanish and English documentation, including running and customization instructions.

### Website concepts in the portfolio

| Concept | Purpose | Implemented features | Potential additions, not yet implemented |
| --- | --- | --- | --- |
| **Brasa & Sal — Hospitality** | Present a restaurant, café or bar's offering and make its menu easy to browse on a phone. | Sample dishes, descriptions and prices; All, Starters, Mains and Desserts filters. | QR-linked menu, verified allergen information, languages, opening hours, location, table bookings and orders connected to a real system. |
| **Nativa — Beauty and personal care** | Present hair salon, barber shop or beauty services and demonstrate an appointment request journey. | Service, date and illustrative time selection; minimum date based on the local day; simulated booking summary. | Live calendar, staff availability, service duration and pricing, confirmations, reminders, cancellations and an authorized work gallery. |
| **Trazo — Renovation and professional services** | Gather initial requirements so a renovation company or independent professional can prepare a first conversation. | Renovation type, approximate floor area and preferred timeframe; locally generated summary. | Enquiry delivery, photo uploads, site visits, lead tracking, completed projects and professionally reviewed quotations. |
| **Alisio Estudio — Studio presentation website** | Bring the concepts together and explain the studio's offering to prospective customers. | Interactive demo gallery, features, working process and a copyable project brief. | Real contact details, authorized client case studies, service packages, a final domain and sector-specific content. |

These additions are development possibilities, not currently available features or guaranteed business outcomes.

### How the interactions work

1. **Menu:** open Brasa & Sal and select a category. JavaScript displays the matching dishes.
2. **Booking:** open Nativa, choose a service, date and time, then select “Simular reserva”. A message appears; no appointment slot is booked.
3. **Enquiry:** open Trazo, select the work, enter an area from 1 to 10,000 m² and choose a timeframe. A summary is generated; no price is calculated and no enquiry is sent.
4. **General brief:** choose a business type and current situation, then enter a goal at the bottom of the portfolio. Copy the result for a later sales conversation.

There is no application server, database, account system, payment processing, analytics, email integration or calendar integration. Forms do not transmit or persist their data. Reloading the page clears the generated summary. The copy button uses the browser clipboard; manual copying instructions appear if it is unavailable.

### Project files

| File | Purpose |
| --- | --- |
| `dist/index.html` | Main page structure and content, cards, forms and demo container. |
| `dist/style.css` | Visual identity, CSS illustrations, layout, responsive rules and focus states. |
| `dist/app.js` | Fictional data, filters, dialogs, native form validation, summaries and copying. |
| `README.md` | Bilingual project documentation. |
| `LEEME.md` | Short pointer to the main documentation. |
| `.gitignore` | Excludes local configuration, temporary files and potential secrets. |

The `dist` directory contains the editable website source directly; it is not generated by a build. Local hosting configuration is not required to run the demos.

### Run locally

**Without installing tools:** open `dist/index.html` in a modern browser, keeping all three files in `dist` together.

**Optional local server**, from the project root with Python installed:

```sh
python -m http.server 8000 --directory dist
```

Then open `http://localhost:8000`. No `npm install` or build step is required. To check JavaScript syntax with Node.js installed:

```sh
node --check dist/app.js
```

### Customization

Edit text and structure in `dist/index.html`, colors and composition in `dist/style.css`, and dishes, services and behavior in `dist/app.js`. Replace fictional information with details verified by each business. Keep simulation notices until real integrations are available.

### Verification and next steps

The JavaScript syntax check has passed. Visual review and complete browser-based functional testing remain pending because the previous environment blocked the local preview. No website deployment has been confirmed. Uploading source code to GitHub does not automatically publish a browsable website.

Before operational use: confirm the brand and contact details, review desktop and mobile layouts, test keyboard navigation and forms, agree content and scope with the client, and connect the required live services. Publish the contents of `dist` using static hosting. GitHub Pages would require a deployment workflow that publishes that directory or a suitable directory restructure; no deployment workflow is included.

No open-source software license is included. Choosing one remains the project owner's decision.

