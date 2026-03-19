GDD: La Última Batería
1. Información General

    Título: La Última Batería.

    Género: Survival / Arcade Top-Down.

    Plataforma: PC / Web (Godot Engine).

    Concepto: Un robot en una fábrica cerrada que debe gestionar su energía para no apagarse.

2. Objetivo y Victoria

    Condición de Victoria: Sobrevivir 60 segundos sin que la energía llegue a 0.

    Condición de Derrota: La energía llega a 0%.

    Puntuación: Tiempo sobrevivido y número de baterías recolectadas.

3. Mecánicas de Juego (Gameplay)

    3.1. Movimiento: El jugador controla al robot usando las teclas WASD.

    3.2. Sistema de Energía:

        Comienza al 100%.

        Consumo pasivo: -2% por segundo.

        Al llegar a 0%: Game Over.

    3.3. Recolección (Baterías):

        Aparecen en posiciones aleatorias cada X segundos.

        Efecto: Recupera +20% de energía al tocarla.

    3.4. Obstáculos (Cubos):

        Se mueven en línea recta y rebotan en las paredes.

        Penalización: Al chocar con el jugador, resta -30% de energía de golpe.

4. Progresión y Dificultad

    Inicio: 2 o 3 cubos en pantalla.

    Escalado: Cada 10-15 segundos aparece un nuevo cubo, aumentando el caos en la sala.

5. Interfaz de Usuario (UI)

    HUD (En juego):

        Barra de energía (ProgressBar).
        Cronómetro de supervivencia.
    Menús:

        Pantalla de Game Over (con botón "Reintentar").

        Pantalla de Victoria (si llega a los 60s).

6. Apartado Técnico y Recursos

    Motor: Godot Engine 4.x.

    Nodos principales: CharacterBody2D (Jugador), Area2D (Baterías/Enemigos), Timer (Control de tiempo/spawn).

    Gráficos:

        Jugador: Sprite de robot .

        Escenario: TileMap industrial/Fabrica .

        Enemigos: Cubos simples o drones.
   7. Dificultad Dinámica y Features Extra

    7.1. Desgaste de Energía Progresivo:

        0s - 20s: Consumo base de -2% por segundo.

        20s - 40s: El robot se vuelve "viejo" y consume -3% por segundo.

        40s - 60s: Modo crítico. Consumo de -4% por segundo. ¡Obliga al jugador a no fallar ni una batería!

    7.2. Cubos Frenéticos:

        Cada vez que aparece un cubo nuevo (cada 10-15s), la velocidad de todos los cubos en pantalla aumenta un 10%. El mapa se vuelve un caos de rebotes.

    7.3. "Sobrecarga" (Mecánica de Riesgo/Recompensa):

        Si el jugador recoge una batería teniendo más del 90% de energía, entra en modo "Sobrecarga" durante 3 segundos: el robot se mueve el doble de rápido, pero el consumo de energía se triplica.

    7.4. Luces de Emergencia:

        Cuando la energía baje del 25%, la pantalla (o el robot) empieza a parpadear en rojo y suena una alarma suave. Esto añade presión psicológica al jugador.

