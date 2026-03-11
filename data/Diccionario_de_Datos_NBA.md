# Diccionario de Datos NBA

Este diccionario divide las estadísticas en categorías para que puedas mejor el contexto de los datos.



#### A. Identificación y Contexto

* Player Name: Nombre del jugador.
* Team Abbreviation: Siglas del equipo (ej. LAL, BOS, GSW).
* AGE: Edad del jugador en esa temporada.
* GP (Games Played): Partidos jugados en la temporada.

MIN (Minutes): Promedio de minutos jugados por partido. 

#### B. Ofensiva (Scoring \& Shooting)

* PTS/Pts Pg Puntos/ Promedio de puntos por partido.
* FGM / FGA: Tiros de campo anotados / intentados.
* FG\_PCT (Field Goal %): Porcentaje de acierto general (Eficiencia).
* FG3M / FG3MA: Triples anotados / intentados.
* Fg3p Pct: Porcentaje de acierto en triples.
* FTM/FTA: Tiros libres anotados / intentados.
* Ft Pct: Porcentaje de tiros libres.
* Oreb (Offensive Rebounds): Rebotes ofensivos (segundas oportunidades).
* AST/Ast Pg : Asistencias/ Asistencias por juego.



#### C. Defensiva y Control

* Dreb (Defensive Rebounds): Rebotes defensivos (cerrar la posesión).
* REB/ Reb Pg (Total Rebounds): Suma de OREB + DREB.
* STL/ Stl Pg (Steals): Robos de balón.
* BLK/ Blk Pg (Blocks): Tapones / Bloqueos por juego.
* tov (Turnovers): Balones perdidos (métrica negativa).
* pf (Personal Fouls): Faltas cometidas.



#### D. Métricas Avanzadas (El valor añadido)

* Plus Minus (+/-): Diferencia de puntos del equipo cuando el jugador está en cancha. (Si es +5, el equipo anota 5 puntos más que el rival con él jugando).
* eff (Efficiency): Una fórmula compuesta: (PTS + REB + AST + STL + BLK − (Missed FG + Missed FT + TOV)). Es el resumen numérico global de un jugador.
