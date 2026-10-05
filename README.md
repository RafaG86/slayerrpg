# Slayer RPG

## Moobs Slayer

Juego de plataformas 2D estilo Idle Slayer. El héroe corre solo por el escenario y el jugador salta para recoger monedas. Los moobs se desbloquean como mejora.

Abre `moobs-slayer/index.html` en el navegador para jugar. No necesita instalación.

### Controles

- **Espacio / W / ↑**: saltar
- **J**: atacar
- **K**: ataque en altura (solo desarrollo)
- Botones DEV **Autoataque** y **Autorecogida**: el héroe ataca a los moobs y salta solo en el momento que alcanza más objetos del grupo.
- **P**: correr / detener
- **B**: boost · **T**: tienda · **Y**: ascensión

### Estado actual

- Personaje pixel art con animaciones de correr, quieto, saltar y atacar, y colores personalizables.
- Monedas en grupos de 1 a 3, siempre por encima del piso.
- Mejora "Llegan los moobs" (10 monedas): desbloquea los moobs, que pueden aparecer a cualquier altura.
- Tienda (botón abajo a la derecha, tecla T) con cinco secciones:
  - **Equipamiento** (modelo Idle Slayer): espada, escudo, armadura, casco, botas veloces y anillo de riqueza. Cada pieza produce monedas por segundo; cada nivel cuesta un 15% más. Desde el casco, cada pieza pide completar una misión.
  - **Mejoras**: "Llegan los moobs" y mejoras de hito (niveles 10, 50, 100, 150 y 200 de cada pieza) que dan +100% de producción, sumadas sobre la base.
  - **Misiones**: objetivos con recompensa en monedas o que desbloquean equipo.
  - **Configuración**: guías, partículas, barra superior, pausa con la tienda abierta y reinicio de progreso.
  - **Estadísticas**: monedas, moobs, acierto, rachas, saltos, distancia y tiempo de juego.
- Los moobs son los enemigos: se derrotan tocándolos o con el ataque y funcionan como las almas del Idle Slayer.
- Ascensión (botón abajo a la izquierda):
  - Los moobs de la partida se convierten en Puntos Slayer (PS); cada PS cuesta 4 moobs más que el anterior (el primero cuesta 5). Cada PS ganado da +1% de monedas por segundo para siempre.
  - Al ascender se reinician monedas, moobs, equipo y mejoras; se conservan PS, árbol, misiones, estadísticas y configuración.
  - Árbol de 8 nodos pagados con PS (más producción, moobs desde el inicio, reinversión, hordas de 4, herencia, puerta ultra…).
  - Ultra ascensión (se desbloquea en el árbol): borra PS y árbol y da Puntos Ultra Slayer = raíz cuadrada de los PS. Se gastan en las Piedras del Tiempo: Actividad (valor de monedas y moobs) e Inactividad (ganancia sin conexión), con rendimiento decreciente.
  - Ganancia sin conexión: 10% de la producción (más con la Piedra de Inactividad), hasta 8 horas.
- Boost (botón o B): 75 monedas, velocidad ×3.5 durante 10 s y 30 s de espera.
- Cajas aleatorias (desde 100 monedas gastadas): aparecen cada 30–120 s en altura y se abren saltando. Eventos: producción ×20, monedas ×10, lluvia de monedas, almas ×5, horda de moobs y boost gratis. Los efectos se acumulan; 1 de cada 10 cajas es plateada y se guarda para abrirla después.
- Moobs gigantes: 12% de los grupos; 4 de vida, se dañan con el toque y el ataque, frenan al héroe mientras pelea y dan 25 moobs.
- Etapa bonus: se entra tocando un portal (aparece cada 2–5 min tras gastar 500 monedas o ascender) o por una caja aleatoria. Nivel de 4 secciones con plataformas y huecos; arcos de monedas sobre cada hueco (cada moneda vale 1 + 2 s de producción) y moobs en las plataformas. Caerse termina la etapa (se conserva lo recogido); completarla da +50% de las monedas recogidas y una caja plateada.
- Portales y dimensiones (nodo "Portales" del árbol, 3 PS): botón arriba a la derecha; recarga de 10 minutos. Cada dimensión cambia paisaje, color de los moobs y bonos:
  - Colinas (inicio) · Bosque (almas ×1.5, 5 PS) · Fábrica (producción ×1.5, 15 PS) · Jungla (30% gigantes y almas ×1.25, 30 PS) · Desierto ardiente (monedas ×2, 60 PS) · Espacio funky (gravedad baja y todo ×1.25, tras una ultra ascensión). El requisito de PS usa el récord de PS alcanzado.
- 20 logros (pestaña Estadísticas): cada uno da +1% de monedas por segundo.
- Guardado automático en el navegador (localStorage, clave `moobs-slayer-save-v1`): monedas, moobs, equipo, mejoras, misiones, estadísticas y configuración. Se guarda cada 5 s, al comprar o reclamar y al cerrar la página; se carga sola al abrir el juego.
- Panel de patrones de aparición para estudiar y mejorar el respawn.
