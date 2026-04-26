# Especificación Técnica: Defensores de Gamonal - Arcade Edition

## 1. Concepto General
Un videojuego de disparos espacial (shoot 'em up) de desplazamiento vertical desarrollado íntegramente en HTML5. El motor utiliza un bucle de animación basado en `requestAnimationFrame` y renderizado directo en un elemento `Canvas 2D`.

## 2. Arquitectura de Estados
El flujo del juego se gestiona mediante tres estados principales:
- **START_SCREEN:** Pantalla de título con estética glitch y botón de inicio de misión.
- **PLAYING:** Estado activo donde se procesan físicas, colisiones y renderizado de entidades.
- **GAME_OVER:** Superposición de fin de partida con resumen de puntos y opciones de navegación.

## 3. Entidades y Mecánicas de Juego

### Nave del Jugador
- **Físicas:** Sistema de movimiento basado en vectores con aceleración y fricción constante (0.9).
- **Armamento:** Disparo láser simple por defecto.
- **Power-ups:** Modo "Double Shot" que permite disparar dos láseres paralelos durante un tiempo limitado (visualizado mediante una barra de energía).
- **Resurgimiento:** Sistema de 3 vidas con un contador de cuenta atrás de 3 segundos tras cada colisión.

### Enemigos y Obstáculos
1. **Naves Normales:** Descienden verticalmente a velocidad constante.
2. **Naves Élite:** Aparecen en formaciones de 5. Tienen capacidad de rebote en pantalla y disparan proyectiles dirigidos al jugador.
3. **Asteroides (Meteoritos):** - **Salud:** Poseen 5 puntos de vida (HP).
   - **Feedback Visual:** Implementan un medidor de vida (verde/rojo) que se hace visible solo después de recibir el primer impacto.

### Jefe Final (Omega Boss)
- Activación automática tras 80 segundos de juego ininterrumpido.
- **Patrón:** Movimiento lateral oscilatorio y ráfagas de disparos en círculo (360°).
- **HUD:** Barra de salud específica en la parte superior de la interfaz.

## 4. Interfaz de Usuario (UI)
- **HUD de Juego:** Marcador de puntos, contador de vidas y barra de power-up.
- **Menú de Muerte:**
  - Botón **Reintentar:** Reinicia la acción directamente.
  - Botón **Menú Principal:** Regresa a la carátula inicial del juego.
- **Estética:** Estilo "Neo-Arcade" con colores neón (#00ffcc, #ff3366) y fondos espaciales dinámicos.

## 5. Requisitos de Implementación
- **Lenguaje:** JavaScript (Vanilla), HTML5, CSS3.
- **Renderizado:** Canvas API (600x800px).
- **Entrada:** Manejo de eventos de teclado (Flechas y Espacio).