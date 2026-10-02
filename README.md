# ☕ Para Lia — Una invitación especial

Este proyecto es una pequeña invitación interactiva para compartir una tarde tomando café.

Abres la página, tocas la taza y descubres una invitación nocturna de café hecha a mano,
con estrellas, una pregunta muy importante y dos botones... uno de los cuales intenta escaparse.

---

## 🚀 Tecnologías

- **HTML5**
- **CSS3** (personalizado, sin frameworks)
- **JavaScript** (vanilla, sin dependencias)
- **Tailwind CSS CDN** — no se usa en esta versión: todo el CSS está escrito a mano para
  evitar el aviso de consola que Tailwind CDN genera en producción y mantener el sitio
  totalmente autónomo.

Todo funciona **solo en el navegador**: no hay backend, ni base de datos, ni builds.
La fecha y la hora se muestran en pantalla y, si Lia pulsa **"✉️ Enviar mi respuesta"**,
se abren en su propio programa de correo ya rellenado (ver
[Cómo recibes las respuestas](#-cómo-recibes-las-respuestas)). Nada se almacena en un servidor.

---

## ✨ Características

- Pantalla de inicio cinematográfica con taza de café (CSS puro), vapor animado y "Toca para comenzar"
- Arranque con clic, toque, `Enter` o `Space`
- Transición elegante: zoom, destello y fade
- Fondo de estrellas con profundidad, paralaje y curvatura suave hacia el centro
- Partículas de polvo y luces cálidas desenfocadas
- Tazas de café flotando en el canvas, con diferentes tamaños, velocidades y opacidades
- Fotos de café flotando suavemente en el fondo
- Tarjeta glassmorphism con la pregunta principal
- Botón **NO** juguetón pero siempre accesible (se cansa de esquivar)
- Botón **SÍ** con confeti de corazones, tazas y estrellas
- Aviso de confirmación: "¿Estás 100% segura...?"
- Pantalla final con selección **opcional** de día y hora
- Botón **"✉️ Enviar mi respuesta"**: abre el correo de Lia con la respuesta ya escrita
- Reproductor de Spotify con arranque **manual**
- Diseño responsive (320px → 1440px)
- Respeta `prefers-reduced-motion`
- Sin errores en consola

---

## 📬 Cómo recibes las respuestas

No hay servidor: cuando Lia elige el día y la hora aparece un botón
**"✉️ Enviar mi respuesta"** que abre su programa de correo con un mensaje ya escrito a `tcgiussepe@gmail.com`.

```
mailto:tcgiussepe@gmail.com?subject=☕ ¡He aceptado el café!&body=...
```

El enlace se reconstruye cada vez que cambia la fecha o la hora, así que también
puedes copiarlo con el botón derecho si su programa de correo no se abre solo.

El mensaje que llega es:

```
¡He aceptado la invitación del café! ☕❤️

Día:  Jueves, 15 de octubre
Hora: 19:45

Enviado desde la invitación ☕
```

> **Para cambiar el destinatario:** busca `MAIL_DESTINO` en `index.html` y edita
> la dirección de correo.

**Nota:** la fecha y la hora se mantienen solo en el navegador hasta que ella pulse
el botón. Si cierra la página antes, la elección se pierde (no hay almacenamiento).

---

## 📸 Imágenes

Las fotografías se sirven desde el **CDN público de Unsplash** (`images.unsplash.com`),
sin marca de agua y con licencia de uso libre. Ninguna contiene personas.

| Uso | Enlace |
|---|---|
| Foto protagonista | https://images.unsplash.com/photo-1495474472287-4d71bcdd2085 |
| Tarjeta · Una buena conversación | https://images.unsplash.com/photo-1554118811-1e0d58224f24 |
| Tarjeta · Un café | https://images.unsplash.com/photo-1509042239860-f550ce710b93 |
| Tarjeta · Una tarde tranquila | https://images.unsplash.com/photo-1461023058943-07fcbe16d735 |
| Tarjeta · Y buena compañía | https://images.unsplash.com/photo-1447933601403-0c6688de566e |
| Flotante 1 | https://images.unsplash.com/photo-1514432324607-a09d9b4aefdd |
| Flotante 2 | https://images.unsplash.com/photo-1442512595331-e89e73853f31 |
| Flotante 3 | https://images.unsplash.com/photo-1498804103079-a6351b050096 |
| Flotante 4 | https://images.unsplash.com/photo-1610889556528-9a770e32642f |
| Flotante 5 | https://images.unsplash.com/photo-1521017432531-fbd92d768814 |

Todas se cargan con parámetros de optimización (`auto=format&fit=crop&q=70`) y
`loading="lazy"`. Si alguna fallara, la página muestra un degradado en su lugar
en lugar de romperse.

Créditos: fotos de [Unsplash](https://unsplash.com) · iconos propios en SVG.

---

## 🎵 Música

El reproductor usa un embed público de Spotify
(`https://open.spotify.com/embed/track/6IPwKM3fUUzlElbvKw2sKl`) y **no** arranca solo:
hay que pulsar **"♪ Activar música"**. El control se hace con el `postMessage`
del propio reproductor, así que el `iframe` original nunca se modifica.

---

## 📁 Estructura

```
/
├── index.html      # toda la aplicación (HTML + CSS + JS)
├── README.md
└── assets/
    ├── images/     # (vacío: las fotos se sirven por CDN)
    └── icons/
        └── favicon.svg
```

---

## 🚀 Publicación

El sitio es estático, así que GitHub Pages lo sirve tal cual.

1. Sube el proyecto a la rama `main`.
2. Ve a **Settings → Pages**.
3. En **Build and deployment** elige **Deploy from a branch**.
4. Selecciona **main** y la carpeta **/ (root)**.
5. Pulsa **Save**.

GitHub Pages publicará la web en:

```
https://<usuario>.github.io/<repositorio>/
```

Para probarlo en local basta con abrir `index.html` en el navegador
(o servir la carpeta con cualquier servidor estático).

---

## 👨‍💻 Autor

Proyecto creado por:

**Giu**

Contacto:

**tcgiussepe@gmail.com**

---

☕ *Hecho con cariño para Lia.*
