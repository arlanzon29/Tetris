# SpeedG3 - Juego de Mesa con Cartas

## Descripción

Juego de mesa tipo "oca" con un circuito/tablero circular donde los jugadores avanzan tirando cartas en lugar de dados.

## Mecánicas Principales

- **Tablero con forma de circuito**: Casillas numeradas en un recorrido con curvas y rectas
  - Las posiciones de las casillas están predefinidas (no calculadas dinámicamente)
  - Distribución: 10 casillas horizontal inferior + 5 vertical derecha + 10 horizontal superior + 5 vertical izquierda
  - Total: 30 casillas
- **Movimiento con cartas**: En lugar de dados, los jugadores revelan cartas para avanzar
- **Cartas especiales**: Cartas con efectos (avanzar más, retroceder, ir a prisión, etc.)
- **Objetivo**: Ser el primero en completar una cantidad de vueltas o llegar a una meta
- **Ficha de coche**: El jugador está representado por un coche
- **Multijugador**: Soporte para varios jugadores en el mismo circuito
  - Inicio: 2 jugadores
  - Cada jugador tiene su propio mazo de cartas
  - Cada jugador tiene su propio coche en el tablero
  - Turnos alternados entre jugadores

## Sistema de Cartas

### Mazo
- Cartas numeradas del 1 al 5
- 2 cartas de cada valor (10 cartas en total)
- Se barajan al inicio de cada partida

### Mano del Jugador
- Cada jugador tiene 3 cartas en mano
- Debe usar una carta para moverse
- Tras usar una carta, robamos una nueva del mazo

## Versión HTML

Prototipo funcional en HTML para validar mecánicas antes de implementar en Unity.

## Estado

En desarrollo - protype HTML en progreso.