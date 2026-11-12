# Axedrez · versiones

Versiones de prueba de Axedrez, un roguelike de ajedrez en desarrollo: armas un ejército, lo
mejoras en una tienda entre partidas y juegas torneos contra rivales con estilos
distintos. Además de las piezas clásicas, hay piezas de otros juegos de tablero
(xiangqi, shogi, janggi, Tamerlán, damas) que se combinan en la misma partida.

## Última versión: 0.3.0-beta.18 · Trofeos y la tienda renovada

Ganarle a un boss ahora deja un trofeo, una ventaja que llevas hasta el siguiente. La tienda también cambia: el taller trae a veces cambios raros y legendarios, una pieza ya no pierde sus mejoras al cambiarla, el Escudo viene según la clase de la pieza y los comodines pasan a llamarse estandartes. Además cambia dónde entran las piezas nuevas de tu ejército. Las runs empezadas antes siguen sin trofeos y con su tienda de siempre: para verlo todo, empieza una nueva.

**[Descargar](https://github.com/moisesPAello/axedrez-versiones/releases/tag/v0.3.0-beta.18)** · [notas completas](v0.3.0-beta.18/)

En la release, descarga el `.apk` en Android o el `.zip` de Windows o Linux. Los
«Source code» que agrega GitHub son las notas de este repo, no el juego.

## Versiones

- [0.3.0-beta.18 · Trofeos y la tienda renovada](v0.3.0-beta.18/) (2026-11-12)
- [0.3.0-beta.17 · Axedrez: el Versus](v0.3.0-beta.17/) (2026-11-11)
- [0.3.0-beta.16 · Axedrez: busca una versión nueva cuando quieras](v0.3.0-beta.16/) (2026-11-10)
- [0.3.0-beta.15 · Axedrez: el Duelo](v0.3.0-beta.15/) (2026-11-10)
- [0.3.0-beta.14 · Axedrez: se actualiza solo](v0.3.0-beta.14/) (2026-11-10)
- [0.3.0-beta.13 · Axedrez: aprende a jugar](v0.3.0-beta.13/) (2026-11-05)
- [0.3.0-beta.12 · Axedrez: vender piezas y tus runs con tu nombre](v0.3.0-beta.12/) (2026-11-05)
- [0.3.0-beta.11 · Clases de pieza](v0.3.0-beta.11/) (2026-11-04)
- [0.3.0-beta.10 · Piezas de otros juegos y el Almanaque](v0.3.0-beta.10/) (2026-11-04)

## Qué hay aquí y qué no

Este repo **no contiene el código fuente del juego**. Solo tiene lo que se publica para
quienes lo prueban:

- las releases, con los ejecutables de Windows, Linux y Android;
- una carpeta por versión con sus notas y las imágenes de las piezas nuevas.

El código vive en un repo privado. Es el mismo esquema que usan apps de código cerrado
como Obsidian, que publica sus releases en un repo público aparte.

## Cómo se genera

Nada de esto se edita a mano. Al etiquetar una versión en el repo privado, la
integración continua:

1. corre las pruebas del motor y compila el juego para cada plataforma;
2. genera las notas a partir de las que se escriben para jugadores, con los sprites de
   las piezas nuevas recortados de la hoja de arte;
3. publica aquí las notas y la release con los ejecutables;
4. avisa en el canal de Discord de quienes lo prueban.

El paso 2 es la frontera entre lo privado y lo público: solo publica lo que genera, quita
los metadatos de las imágenes y se detiene si una nota trae algo interno, como un
correo, una ruta o un enlace al repo privado.

## El motor

Escrito en C# sin dependencias, con las reglas de la FIDE validadas con perft y una capa
de efectos que cambia cómo se mueven y capturan las piezas. Los movimientos de las piezas
de otros juegos se comparan contra Fairy-Stockfish durante el desarrollo. El rival es una
búsqueda alfa-beta propia.

## Estado

En desarrollo y en pruebas cerradas con amigos. Los ejecutables no están firmados:
Windows avisa la primera vez («Más información» y después «Ejecutar de todos modos»).
Este repo no recibe issues; el feedback va por el canal de Discord.
