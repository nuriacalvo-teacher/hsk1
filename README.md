# 汉语 HSK1 · Repaso

App web para repasar todo el curso **HSK 1** (15 temas). Está pensada para
hispanohablantes: todas las explicaciones, preguntas y traducciones están en
español.

| Sección | Qué hay | Cuántos |
|---|---|---|
| **Dictado · 听写** | Escuchas y escribes en pinyin. Se corrige sílaba a sílaba y tono a tono. | 63 dictados: frases de cada tema, vocabulario de cada tema y dictados especiales (números, edades, precios, fechas, horas y teléfonos) |
| **Listening · 听力** | Diálogos con 2 o 3 voces y 5 preguntas que se responden en pinyin o en español. Después se ve la transcripción y se puede repetir cada línea. | 30 diálogos, 2 por tema |
| **Lectura · 阅读** | Nivel 1 en **pinyin** y nivel 2 en **hanzi**. Al tocar una palabra se ven su hanzi o su pinyin y su traducción. Cada lectura tiene 5 preguntas. | 30 lecturas, 1 por tema y nivel |
| **Traducción · 翻译** | 4 niveles: pinyin → español, español → pinyin, hanzi → español y español → hanzi (con fichas o con el teclado chino). Se puede elegir un tema o mezclar todo el curso. | 270 frases del curso |
| **Vocabulario · 词语** | Todas las palabras por tema, con buscador y audio. | 237 palabras |

Todos los audios tienen **cuatro velocidades**: muy lento, lento, medio y
normal.

## Cómo usarla

- **En internet (recomendado):** activa GitHub Pages una sola vez en
  **Settings → Pages → Source: Deploy from a branch → `main` / `(root)` → Save**.
  Al cabo de un minuto la app queda en
  `https://nuriacalvo-teacher.github.io/hsk1-repaso/`.
- **En tu ordenador:** descarga el repositorio y abre `index.html` con el
  navegador. No hace falta instalar nada.

El progreso (la mejor nota de cada ejercicio) se guarda en el navegador de
cada alumno.

### Cómo se corrige

- **Pinyin:** los tonos se pueden escribir con marcas (`nǐ hǎo`) o con
  números (`ni3 hao3`), que se convierten solos mientras escribes. También
  hay botones ˉ ˊ ˇ ˋ y ü. Se aceptan los cambios de tono de 不 y 一
  (`bù/bú`, `yī/yí/yì`) y el `yāo` de los teléfonos. Si una sílaba tiene el
  tono mal, sale en naranja y la respuesta vale la mitad. Si falta o sobra
  una sílaba, sale en rojo. En **Ajustes** se pueden ignorar los tonos.
- **Español:** no se tienen en cuenta las tildes, las mayúsculas ni los
  artículos. «3» y «tres» valen igual, y también el masculino y el
  femenino. En las traducciones, si la respuesta se parece pero no es
  igual, la app enseña la traducción de referencia. Siempre hay un botón
  **«Mi respuesta también es correcta»**.
- **Hanzi:** no se tienen en cuenta la puntuación ni los espacios, y
  `28块` = `二十八块`.

### Sonido

- **Música de fondo** en los menús: guzheng sobre la escala pentatónica
  china, con un bordón suave y campanillas. Se genera en el navegador y
  nunca se repite igual. **Se para al entrar en un ejercicio** y vuelve al
  salir. Se quita o se pone con el botón ♪ de la cabecera. En **Ajustes**
  también se cambia el volumen.
- **Efectos:** hay un sonido para el acierto (arpegio ascendente), otro para
  el «casi» y otro para el fallo (bloque de madera). Al terminar, suena un
  gong con escala ascendente si has aprobado (≥ 50 %; con ≥ 80 % es más
  largo) y un gong grave con escala descendente si has suspendido. Se pueden
  probar y desactivar en **Ajustes**.

### ¿Hace falta instalar un teclado chino?

**No.** Toda la app se puede hacer con el teclado normal del ordenador o del
móvil:

- **Pinyin:** se escriben las letras y el tono con un número detrás
  (`hao3` → hǎo) o con los botones ˉ ˊ ˇ ˋ. La ü se escribe con `v`.
- **Español:** no importan las tildes ni los signos ¿?.
- **Hanzi** (solo en la traducción de nivel 4) se escriben de una de estas
  tres maneras:
  - con **fichas**;
  - con el **teclado de la app**: se teclea el pinyin sin tonos (`woxiang`)
    y se elige la palabra (我 → 想). Solo propone palabras del curso;
  - con el **teclado chino del dispositivo**, si lo tienes instalado.

Dentro de la app, la página **«Cómo escribir pinyin y hanzi»**
(`#/teclado`) explica paso a paso cómo instalar el teclado chino (pinyin) en
iPhone/iPad, Android, Windows, Mac, Chromebook y Linux.

## Audio con voces nativas

La app usa **audios grabados con voces neuronales chinas** (las mismas voces
de Microsoft Edge: Xiaoxiao, Yunxi, Xiaoyi, Yunjian…) si están en `audio/`.
Si todavía no existen, usa la voz china del navegador. **Hay que grabarlos
una vez**, igual que en el proyecto BRIT:

### Opción A · online, sin instalar nada

1. Pestaña **Actions** del repositorio → **Grabar los audios** → **Run workflow**.
2. Tarda unos 30-45 minutos la primera vez (≈ 600 audios × 3 velocidades) y
   sube él solo los audios al repositorio.

> Si falla al subir: **Settings → Actions → General → Workflow permissions →
> Read and write permissions**. Solo hay que tocarlo una vez.
>
> A veces el servicio de voz rechaza las peticiones que vienen de los
> servidores de GitHub. Si pasa, usa la opción B, que sale desde tu propia red.

### Opción B · en el Mac, con doble clic

1. Clona el repositorio o descárgalo (botón verde **Code → Download ZIP**).
2. En la carpeta `tools`, haz **doble clic en `GRABAR-AUDIOS.command`**.
   Si lo clonaste con git, al terminar sube los audios él solo.

### Elegir las voces

- **`tools/COMPARAR-VOCES.command`** (o *Run workflow* marcando
  **comparativa**) graba un MP3 en el que todas las voces chinas dicen su
  nombre y leen la misma frase.
- Escribe en **`tools/voces.txt`** las que más te gusten. En ese mismo
  fichero se cambian las velocidades.
- **`tools/ESCUCHAR-VOCES.command`** (o **muestra**) graba un minuto con las
  voces elegidas a las tres velocidades.

Al volver a grabar, **solo se regraban los audios cuyo texto o voz haya
cambiado**.

## Cambiar o añadir contenido

Todo el contenido está en `data/` y se puede editar como texto:

| Fichero | Contenido |
|---|---|
| `data/diccionario.tsv` | Vocabulario: hanzi, pinyin, español y tema. |
| `data/frases.txt` | Las frases del curso por tema. Se usan en las traducciones y los dictados de frases. |
| `data/dictados_extra.txt` | Los dictados especiales: números, fechas, horas… |
| `data/listenings_*.json` | Los diálogos y sus preguntas. |
| `data/lecturas_n1.json`, `data/lecturas_n2.json` | Las lecturas y sus preguntas. |

Después de editar, ejecuta:

```bash
python3 tools/build_data.py     # revisa los textos y regenera js/datos.js
```

El revisor (`tools/revisar.py`) avisa de estos problemas:

- palabras que no están en el diccionario;
- pinyin con distinto número de sílabas que de hanzi;
- ejercicios que no tienen exactamente 5 preguntas.

Luego graba los audios nuevos con la opción A o la B.

## Estructura

```
index.html            la app (una sola página)
css/estilos.css       diseño
js/app.js             pantallas y ejercicios
js/corrector.js       corrección de pinyin, español y hanzi
js/sonido.js          música de fondo y efectos (Web Audio, sin ficheros)
js/datos.js           contenidos (generado por tools/build_data.py)
audio/                audios grabados + manifest.js
data/                 contenidos editables
tools/                revisor, generador de datos y grabador de audio
```
