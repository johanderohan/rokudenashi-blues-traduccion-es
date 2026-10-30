# Rokudenashi Blues: Taiketsu! Tokyo Shitennou (Super Nintendo) — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Traducción al **español de España** de *Rokudenashi Blues: Taiketsu! Tokyo Shitennou*
(Super Famicom, Bandai, 1994), el juego de lucha y aventura basado en el manga de Masanori Morita:
Taison Maeda, alumno del Instituto Teiken que quiere ser campeón de boxeo, se va metiendo en una
pelea tras otra hasta enfrentarse a los «Cuatro Reyes» de Tokio. Se ha traducido **directamente del
japonés**, a partir de la ROM japonesa original.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu propia copia para
aplicarlo.

## Estado

Última versión: **[v1.0 — Primera versión completa](../../releases/tag/v1.0)** (en revisión).

| Parte | Estado |
|---|---|
| Modo historia: narración y diálogos de los siete capítulos, con el final | **1200 mensajes** traducidos y revisados |
| Intro, verbos de exploración, papeleta de la suerte y créditos | Traducidos (los nombres del equipo, romanizados) |
| Rótulos gráficos necesarios para jugar | Menú principal, pantalla de opciones, selección de luchador y escenario, ¡YA!, PAUSA, EMPATE, IRA, ¿CONTINUAR? / PULSA START / FIN DEL JUEGO y CONTINUAR / SALIR |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « » …** |
| Logotipos | Se conservan (ver abajo) |
| Revisión en el juego | Todo el texto visto en pantalla; capítulo 1 jugado hasta el capítulo 2 (ver abajo) |

Se mantienen a propósito, como imagen de marca, el logotipo ろくでなしBLUES y el rótulo 対決!東京四天王
del título, y el aviso de copyright. También se dejan POWER, 1P/COM y VS, que están en inglés en el
original.

### Cambios técnicos

- El juego dibuja el texto en casillas fijas de 16 píxeles pensadas para kanji: en castellano solo
  cabían 12-14 letras por renglón. Se ha añadido una **fuente de ancho variable** con las letras de
  la propia fuente del juego (mismo trazo y color) y ajuste entre parejas de letras, de modo que
  caben unas 30-35 letras por renglón. Se conservan la escritura progresiva, la paginación de tres
  renglones y los cambios de expresión de los retratos.
- La ROM pasa de 12 a **16 Mbit** (2 MB) para alojar el texto castellano; el japonés que no se
  traduce (ninguno jugable) sigue saliendo igual que en el original.
- Los rótulos gráficos se han redibujado con las paletas y el estilo originales y se han
  recomprimido con el mismo método del juego.

### Comprobaciones y trabajo pendiente

- Una auditoría automática relee la ROM construida y comprueba cada mensaje (que el juego lo
  encuentra donde debe y que no se sale del cuadro), los gráficos y el *checksum* interno.
- **Todo el texto** (los 1200 mensajes, la intro, los verbos y los créditos) se ha hecho dibujar al
  propio motor del juego en el emulador y se ha comprobado página a página, también el de los
  capítulos 2-7 y el final.
- Jugado en emulador (snes9x) **desde partida nueva**: intro, menú, capítulo 1 completo con su
  exploración, el combate del ring (pausa, derrota, ¿CONTINUAR? y victoria) y la llegada al
  capítulo 2; modo de un jugador y de dos (selección, combates, pausa, continuar) y opciones.
  Arranque y modo historia comprobados también en bsnes (precisión).
- **Pendiente:** jugar de principio a fin los capítulos 2-7 y el final (su texto se ha visto en
  pantalla, pero forzado), la prueba en consola física o *flashcart* y una revisión humana
  independiente. La traducción y su revisión se han hecho con asistencia de IA. Por eso la versión
  figura «en revisión»; si encuentras algo, abre una incidencia.

### Incidencias conocidas

- Las mayúsculas de la fuente del juego son algo más altas y con remates que las minúsculas (es el
  diseño original de esa fuente).
- En la pantalla de opciones, la lista de botones del mando va muy junta, como en el original.
- Algunos puestos de los créditos van partidos en dos renglones porque la pantalla solo enseña una
  parte del lienzo.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en versión **japonesa**, sin cabecera de copiadora:

   | | |
   |---|---|
   | Archivo | `Rokudenashi Blues - Taiketsu! Tokyo Shitennou (Japan).sfc` |
   | Tamaño | 1.572.864 bytes (1,5 MB) |
   | MD5 | `d4a376574ba6e7384132111f8cf55feb` |
   | CRC32 | `2C85EC10` |

   ```bash
   md5sum "Rokudenashi Blues - Taiketsu! Tokyo Shitennou (Japan).sfc"     # Linux
   md5 "Rokudenashi Blues - Taiketsu! Tokyo Shitennou (Japan).sfc"        # macOS
   CertUtil -hashfile "Rokudenashi Blues - Taiketsu! Tokyo Shitennou (Japan).sfc" MD5   # Windows
   ```

   Si tu archivo mide 1.573.376 bytes tiene una cabecera de 512 bytes: quítala antes de parchear.
3. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "Rokudenashi Blues - Taiketsu! Tokyo Shitennou (Japan).sfc" rokudenashi-blues-snes-es-v1.0.xdelta "Rokudenashi Blues (ES).sfc"`
4. Comprueba que la ROM resultante mide **2.097.152 bytes** (2 MB) y tiene MD5
   **`e371470becf4014fbd36edd04c7cca70`**.
5. Juega en tu emulador o *flashcart*. El juego no guarda partida (como el original).

## Cambios por versión

### v1.0 — 30 de octubre de 2026

- Primera versión completa: el modo historia entero (siete capítulos y final), la intro, los
  créditos y los menús en castellano de España, traducidos del japonés.
- Fuente española de ancho variable con el estilo original y rótulos gráficos del menú, las
  opciones, la selección y el combate traducidos.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación alguna con
Bandai, Shūeisha ni con los titulares de *Rokudenashi Blues*. Aquí no se distribuye el juego ni
ninguna parte de él: solo un parche que modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo hago.
