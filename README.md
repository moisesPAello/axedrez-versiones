# Roguelike de ajedrez · versiones

Versiones de prueba de un roguelike de ajedrez en desarrollo: armas un ejército, lo
mejoras en una tienda entre partidas y juegas torneos contra rivales con estilos
distintos. Además de las piezas clásicas, hay piezas de otros juegos de tablero
(xiangqi, shogi, janggi, Tamerlán, damas) que se combinan en la misma partida.

**Página de descargas y notas de cada versión: https://moisespaello.github.io/chess-roguelike-versiones/**

## Qué hay aquí y qué no

Este repo **no contiene el código fuente del juego**. Solo tiene lo que se publica para
quienes lo prueban:

- las releases, con los ejecutables de Windows, Linux y Android;
- la página de versiones (GitHub Pages), con las notas de cada versión.

El código vive en un repo privado. Es el mismo esquema que usan apps de código cerrado
como Obsidian, que publica sus releases en un repo público aparte.

## Cómo se genera

Nada de esto se edita a mano. Al etiquetar una versión en el repo privado, la
integración continua:

1. corre las pruebas del motor y compila el juego para las cinco plataformas;
2. crea aquí la release con los ejecutables;
3. genera la página a partir de notas escritas para jugadores, con los sprites de las
   piezas nuevas recortados de la hoja de arte;
4. avisa en el canal de Discord de quienes lo prueban.

El paso 3 es la frontera entre lo privado y lo público: solo publica lo que genera, quita
los metadatos de las imágenes y se detiene si una nota trae algo interno, como un
correo, una ruta o un enlace al repo privado.

## El motor

Escrito en C# sin dependencias, con las reglas de la FIDE validadas con perft y una capa
de efectos que cambia cómo se mueven y capturan las piezas. Los movimientos de las piezas
de otros juegos se comparan contra Fairy-Stockfish durante el desarrollo. El rival es una
búsqueda alfa-beta propia.

## Estado

En desarrollo y en pruebas cerradas con amigos. Los ejecutables no están firmados: la
página explica cómo abrirlos en Windows. Este repo no recibe issues; el feedback
va por el canal de Discord.
