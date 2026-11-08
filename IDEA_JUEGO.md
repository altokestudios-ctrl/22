# Propuesta v2: «STEAL FROM THE DRAGON» (nombre provisional)

> Juego de robo y defensa con sigilo por ruido. Tú y los demás jugadores del servidor os coláis en la guarida de un **dragón gigante dormido** para robarle huevos y tesoros. Si haces ruido, se despierta. Además, puedes robar a los demás jugadores… y hacer ruido a propósito para que el dragón se despierte justo encima de ellos.

Documento preparado el 8 de noviembre de 2026. Las fuentes están al final. Muchas son guías y webs de estadísticas de terceros, así que las cifras son orientativas.

---

## 1. La estrategia: combinar lo que ya funciona

Las mecánicas no tienen dueño; los nombres, el arte, los personajes y la interfaz sí. Tomamos **bucles probados** de los juegos que dominan ahora y los envolvemos en una identidad propia.

| Juego de referencia | Situación (nov. 2026) | Qué tomamos | Qué NO tomamos |
|---|---|---|---|
| **Steal An Egg** | N.º 1 en jugadores simultáneos: unos 790.000–890.000 el 7–8 nov.; más de 1 millón en octubre. | Robar en zonas vigiladas, incubar huevos, mascotas que generan dinero por segundo, zonas bloqueadas por una estadística, robar bases ajenas. | Su nombre, sus guardianes, su arte, su interfaz y sus mascotas. |
| **Steal a Brainrot** | Récord histórico: más de 25 millones de jugadores simultáneos. | El «captura la bandera» de robar y volver corriendo a la base, la cerradura temporal de la base y el bucle infinito de tycoon. | Los personajes «brainrot» (son memes de terceros). |
| **Grow a Garden** | Mantuvo récords durante 2026 y tiene secuela. | Eventos de clima que dan mutaciones, eventos en directo semanales a hora fija (su «Admin Abuse»), actualizaciones semanales con cuenta atrás. | Plantas, tiendas, estética. |
| **DONT SPLASH** | Juego nuevo que más crece en noviembre (sale el 17 oct.; pico de 116.000). | **El monstruo que caza por el sonido**: cada ruido lo atrae. | El escenario de piscinas, el monstruo, el formato obby. |

**La diferencia frente a los clones** (ya existen derivados como «Fake an Egg»): el guardián no es un NPC más, sino **un jefe gigante compartido por todo el servidor**, y el sigilo se basa en el ruido. Eso añade:
1. **Sabotaje entre jugadores:** tiras una piedra cerca de un rival y el dragón se despierta encima de él. Genera los momentos de traición que se viralizan en TikTok.
2. **Espectáculo:** cuando el dragón se despierta (rugido, barrido de fuego, todos corriendo), el momento se convierte solo en un clip.
3. **Un tema eterno:** dragones y huevos de dragón gustan a todas las edades y no dependen de un meme que caduca.

---

## 2. Bucle principal

```
TU BASE (cueva en el anillo exterior del mapa, servidor de 8 jugadores)
  → Entras en la GUARIDA (centro del mapa). El dragón duerme sobre su tesoro.
     · Medidor de RUIDO del dragón, compartido por todo el servidor
     · Correr = ruido · andar = poco · agacharse = casi nada
     · Monedas/huesos en el suelo = ruido al pisarlos · llevar un huevo = más lento
     · Cuanto más cerca de la cabeza, más raro el botín
  → Coges un huevo / tesoro y vuelves a tu base
     · Otros jugadores pueden golpearte para que lo sueltes y quitártelo
  → Si el dragón DESPIERTA: rugido, barrido de fuego, persecución.
     A quien alcanza, suelta lo que llevaba → botín libre para cualquiera.
  → En tu base: INCUBAS el huevo (de 1 minuto a varias horas, según rareza)
  → La cría de dragón genera ORO/segundo en tu base (visible para todos)
  → Oro → mejoras: botas silenciosas (sigilo), mochila, cerradura de base, incubadora
  → Más sigilo → acceso a guaridas más profundas (dragón de hielo, de tormenta, del vacío…)
  → Robar crías y huevos de las bases ajenas cuando su cerradura está abierta
```

### Sistemas de retención (D1, D7, D30)
- **Ingresos sin conexión**, con límite: motivo para volver al día siguiente.
- **Incubación en tiempo real:** el huevo raro tarda 2 horas, así que vuelves a abrirlo.
- **Lunas y clima a nivel de servidor** (luna de sangre, tormenta, eclipse): los huevos robados durante el evento salen con mutación y multiplicador.
- **Índice de dragones:** colección con recompensas por completar cada elemento.
- **Renacer:** reinicias el oro a cambio de un multiplicador permanente y una base con mejor aspecto. Es el estándar del género para la retención a largo plazo.
- **Intercambio de dragones:** **en la fase 2**, no en el lanzamiento. Engancha mucho a la comunidad, pero trae estafas y duplicaciones que hay que blindar.

---

## 3. Motor de crecimiento: cómo pasar de 0 jugadores

Que un juego reciba tráfico depende de dos cosas: que los jugadores lleguen y que se queden (la retención es lo que el algoritmo mide). Esto es lo que va dentro del juego para conseguir ambas:

| Palanca | Implementación |
|---|---|
| **Se entiende en 3 segundos** | Nombre con la palabra «Steal», el término que la gente ya busca. Miniatura: ojo gigante del dragón abriéndose y un avatar con un huevo en brazos. Preparad 3 o 4 miniaturas y quedaos con la que mejor funcione. |
| **Primeros 60 segundos** | Primer robo garantizado en menos de 30 s (huevo pequeño junto a la entrada) y primera eclosión en 60 s. Sin texto de tutorial: flechas y brillos. |
| **Funciona con desconocidos** | Servidores de 8 en los que no hace falta tener amigos. *(Este era el fallo de HUNDIDOS: un cooperativo depende de traer a tus amigos.)* |
| **Bonus por amigos** | +10 % de oro por cada amigo en el servidor, con un tope. Aviso de invitación justo después del primer robo con éxito. |
| **Venganza** | «X te ha robado tu Dragón de Tormenta» → botones [Invitar amigos] y [Perseguir]. Robar crea rivalidad, y la rivalidad trae gente. |
| **Eventos en directo a hora fija** | Cada sábado, «El Dragón Ancestral despierta»: botín masivo, mutaciones garantizadas y regalos para todo el servidor. Concentra jugadores a la vez, y esos picos se notan en las listas. |
| **Actualización semanal con cuenta atrás en el juego** | Mismo día y misma hora cada semana. El jugador sabe cuándo volver. |
| **Códigos para creadores** | Sistema de códigos desde el primer día. Contactad con YouTubers y TikTokers pequeños y medianos: acceso anticipado más código propio. Grow a Garden atribuye su primer pico a creadores de contenido. |
| **Grupo de Roblox** | Cofre diario por unirse al grupo. Es la base para promocionar vuestros siguientes juegos entre sí. |
| **Anuncios patrocinados** | Solo cuando la retención sea buena. Una guía de terceros cita unos 0,007 USD por partida iniciada (nov. 2025), así que 100.000 partidas rondarían los 700 USD. Es orientativo; medidlo vosotros. Los anuncios no suben vuestro puesto en la portada: solo traen gente a probar. |
| **Creator Rewards / Audience Expansion** | Roblox paga una parte de lo que gastan los jugadores nuevos que llegan por vuestro enlace. Compartid siempre el enlace directo del juego. |

---

## 4. Monetización (la probada en el género)

| Producto | Tipo | Nota |
|---|---|---|
| Botas silenciosas premium, mochila doble, cerradura larga | Game Pass | El núcleo del género. |
| VIP (más oro, zona VIP, etiqueta en el chat) | Game Pass | |
| Incubación instantánea | Developer Product | Monetiza la impaciencia sin romper el juego. |
| **«Luna de sangre para todo el servidor»** | Developer Product | Un jugador paga y **todos** se benefician, con aviso en pantalla. Es social y genera agradecimiento y presión de grupo. |
| Huevos de pago | Developer Product | **Obligatorio según la política de Roblox:** mostrar las probabilidades numéricas reales antes de comprar, actualizarlas si hay potenciadores activos y respetar `ArePaidRandomItemsRestricted` en las regiones donde aplica. |
| Pieles de base, estelas, efectos de fuego | Cosmético | |

Solo paga en torno al **3,8 %** de los jugadores (mediana de GameAnalytics 2026), así que todo el diseño gira en torno a dar razones para ese 3,8 % sin echar al resto.

---

## 5. Plan de producción (3 personas)

Este género se construye rápido, y **la velocidad importa**: las modas en Roblox duran meses, no años. Si el lanzamiento se retrasa mucho, el «Steal» puede enfriarse. Por eso el núcleo (robar a un guardián dormido, base, incubación) se diseña para poder **cambiar el tema** sin reescribir el código.

| Persona | Responsabilidad |
|---|---|
| **A: Sistemas (Luau)** | Servidor autoritativo: ruido e IA del dragón, cargar y soltar objetos, bases y cerraduras, guardado de datos, **antitrampas** (velocidad, teletransporte, distancia al coger objetos). Los juegos de robo son imán de exploits. |
| **B: Mundo, modelos y animación** | Guarida, bases, dragones y crías. Con presupuesto: **encargad los modelos y animaciones de dragón** a artistas (Talent Hub de Roblox) y centraos en el montaje y los efectos. |
| **C: Interfaz, economía y crecimiento** | Interfaz para móvil primero, hoja de cálculo de la economía (costes exponenciales, que no haya inflación), monetización, analítica, Discord, TikTok, creadores y anuncios. |

| Semana | Entregable |
|---|---|
| 1–2 | Medidor de ruido + dragón que despierta y persigue + coger/llevar/soltar + bases con cerradura. **Probadlo con 8 personas: ¿hay gritos y traiciones?** Si no, ajustad el ruido antes de seguir. |
| 3–4 | Incubación, oro por segundo, mejoras, 2 guaridas, guardado, monetización básica, códigos. |
| 5–6 | Pulido para móvil, antitrampas, eventos de luna, miniaturas, 2–3 creadores con acceso anticipado. |
| 6–7 | **Lanzamiento.** Anuncios con presupuesto pequeño durante 3–7 días para medir retención. |
| Después | Actualización semanal fija, evento del sábado y una guarida o dragón nuevo cada 2–3 semanas. |

### Métricas de control (GameAnalytics 2026, más de 500 juegos)
| | Mediana | Top 1 % | Objetivo antes de gastar fuerte en anuncios (mi criterio) |
|---|---|---|---|
| D1 | 10,3 % | 22,2 % | ≥ 15 % |
| D7 | 1,6 % | 9,1 % | ≥ 4 % |
| Sesión | 9,8 min | — | ≥ 15 min |

---

## 6. Riesgos (sin adornar)

| Riesgo | Qué hacer |
|---|---|
| El género «Steal» está lleno de clones y la mayoría fracasa. | La diferencia tiene que **notarse en 10 segundos**: dragón gigante, ruido y sabotaje. Si en las pruebas parece «otro Steal An Egg», hay que exagerar más esa diferencia. |
| La moda se enfría antes de lanzar. | Lanzar en 6–7 semanas, no en 6 meses. El tema es intercambiable. |
| Trampas (duplicar oro, teletransportarse a la guarida) | Validación en el servidor de todo; nunca confiar en el cliente. Es imprescindible antes del lanzamiento. |
| Inflación de la economía | Hoja de cálculo de costes y ganancias; simular 30 días de juego antes de lanzar. |
| Que se perciba como copia | Nada de nombres, arte, interfaz ni personajes de otros juegos. Mecánicas sí, identidad no. |
| Calificación de edad | Mantener el miedo ligero (sin sangre ni sustos fuertes) para poder optar a la calificación más baja y llegar al público más amplio. Revisad el cuestionario de madurez. |

---

## 7. Otras dos combinaciones con la misma estrategia (por si el prototipo no convence)

1. **Pesca + robo:** pescas peces raros y los expones en tu acuario, que genera dinero por segundo; los demás pueden robártelos. Mezcla Fisch, el gran éxito de pesca de 2024–25, con el bucle de robo.
2. **Granja de día + asedio de noche:** de día cultivas y mutas cosechas; de noche el servidor entero defiende contra hordas. Mezcla Grow a Garden, 99 Nights in the Forest y tower defense.

Las dos reutilizan la base, el guardado, la economía, la monetización y el antitrampas del proyecto principal.

---

## 8. Esta semana

- [ ] Buscad en Roblox: «steal a dragon», «dragon egg», «don't wake». Anotad la competencia directa y sus jugadores simultáneos. No pude consultar Roblox directamente desde esta sesión.
- [ ] Elegid el nombre definitivo (opciones: *Steal from the Dragon*, *Don't Wake the Dragon*, *Steal a Dragon Egg*) y comprobad que no está cogido.
- [ ] Montad Rojo + Git en este repositorio.
- [ ] Empezad las semanas 1–2.

---

## 9. Fuentes

- Steal An Egg, mecánicas: [Página en Roblox](https://www.roblox.com/games/107778070777162/Steal-An-Egg) · [games.gg](https://games.gg/roblox/guides/steal-an-egg-beginner-guide/) · [Sportskeeda](https://www.sportskeeda.com/roblox-news/steal-an-egg-a-beginner-s-guide)
- Jugadores simultáneos ahora: [LiveCounts](https://livecounts.nl/roblox-charts/) · [RoWatcher](https://rowatcher.com/roblox-player-count) · [clip.dor.gg (octubre)](https://clip.dor.gg/en/blog/roblox-popular-games-ranking)
- Juegos que más crecen en noviembre: [GGRecon](https://www.ggrecon.com/articles/fastest-growing-new-roblox-games-november-2026/) · [Bloxrant](https://bloxrant.com/roblox-trending-games)
- DONT SPLASH: [Bloxodes](https://bloxodes.com/wiki/dont-splash) · [RoWatcher](https://rowatcher.com/games/10771421858/dont-splash)
- Steal a Brainrot y Grow a Garden: [Wikipedia – Steal a Brainrot](https://en.wikipedia.org/wiki/Steal_a_Brainrot) · [Wikipedia – Grow a Garden](https://en.wikipedia.org/wiki/Grow_a_Garden) · [Screen Rant](https://screenrant.com/roblox-steal-brainrot-fad-explanation/) · [RoLearn – análisis del récord de Grow a Garden](https://rolearn.dev/insights/grow-a-garden-ccu-record-analysis/)
- Admin Abuse y eventos semanales: [Wiki de Grow a Garden](https://growagarden.fandom.com/wiki/Admin_Abuse) · [GameSpot](https://www.gamespot.com/articles/next-grow-a-garden-update-and-events/1100-6534922/)
- Anuncios y captación: [Roblox – plataforma de anuncios](https://about.roblox.com/newsroom/2026/01/roblox-expands-advertising-platform) · [clipclip – coste de anuncios](https://clipclip.io/guides/roblox-ads-cost) · [clipclip – cómo conseguir jugadores](https://clipclip.io/guides/get-more-players) · [PPC Land](https://ppc.land/roblox-developers-buy-ads-for-traffic-as-80-of-top-games-use-ai/)
- Benchmarks: [GameAnalytics 2026 Roblox Report](https://www.gameanalytics.com/reports/2026-roblox-report) · [gamedevreports](https://gamedevreports.substack.com/p/gameanalytics-key-roblox-and-roblox)
- Política de artículos aleatorios de pago: [Documentación de Roblox](https://create.roblox.com/docs/production/monetization/paid-random-items)
