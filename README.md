# Slayer RPG

## Moobs Slayer

Estilo visual cartoon suave: todo se dibuja en vectorial a la resolución real de la pantalla (canvas escalado con devicePixelRatio), con degradados, contornos redondeados, halos y nubes. Fuente de la interfaz: Fredoka.

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
  - **Equipamiento** (modelo Idle Slayer): las 18 piezas del original con sus costos base y producción — espada, escudo, armadura, casco, botas veloces, anillo de riqueza, daga, hacha, bastón mágico, arco largo, libro de hechizos, espíritu, collar, guantes, capa, garra, lanza y shuriken. Cada nivel cuesta un 15% más; compra ×1, ×10, ×100 o Máx. Desde el casco cada pieza pide una misión (desde la daga: subir la pieza anterior a nivel 25). Se muestran las piezas disponibles y la siguiente bloqueada.
  - **Mejoras**: catálogo de 33 compras únicas con filtros (disponibles, próximas, compradas y por tipo), "Llegan los moobs" y mejoras de hito (niveles 10, 50 y cada 50 hasta 500 de cada pieza, de bronce a divina) que dan +100% de producción, sumadas sobre la base.
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
- Arco (nodo "Libro de proyectiles", 4 PS): mientras el héroe está en el aire dispara flechas solas cada 0,35 s; los moobs derrotados con flecha dan +50% de almas y las flechas también dañan a los gigantes. "Flecha doble" (6 PS) agrega una segunda flecha hacia abajo.
- Catálogo de mejoras (se pierden al ascender), por tipo:
  - Producción: Pan del camino, Carne (1.280, como el original), Guiso de moob, Banquete, Néctar, Ambrosía, Energía estelar (3e60), Cota de codicia (500 M, +0,1% por nivel de equipo) y Espada de furia (+3000% a la espada).
  - Valor de moneda: Recompensa al esfuerzo (200), Monedero grande, Cofre sin fondo y Hongos extravagantes (2e33): cada moneda recogida vale un % de tu producción.
  - Logros: Cinturón del conocimiento (2.500), de la sabiduría y del poder (2,5e68): % extra por logro.
  - Almas, arco (Estabilidad, Disparo triple, Carcaj rápido), cajas (imán vertical, más frecuentes, efectos más largos), enemigos (más moobs, más gigantes, evolución gigante), imán de monedas I/II/guantes, boost económico, Mega boost y Colgante hechicero (+30% sin conexión).
- 21 logros (pestaña Estadísticas): cada uno da +1% de monedas por segundo.
- Guardado automático en el navegador (localStorage, clave `moobs-slayer-save-v1`): monedas, moobs, equipo, mejoras, misiones, estadísticas y configuración. Se guarda cada 5 s, al comprar o reclamar y al cerrar la página; se carga sola al abrir el juego.
- Panel de patrones de aparición para estudiar y mejorar el respawn.
