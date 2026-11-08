# Propuesta de juego para Roblox: «HUNDIDOS» (nombre provisional)

> Juego cooperativo de rescate de cargamento, de 1 a 4 jugadores. Tu cuadrilla de chatarreros se mete en barcos que **se están hundiendo en tiempo real**. Tenéis que sacar todo el botín que podáis antes de que el agua os alcance.

Documento preparado el 8 de noviembre de 2026. Los datos de mercado están en la sección 9 con sus fuentes; varias son de terceros y no se pueden verificar al 100 %.

---

## 1. Por qué esta idea y no otra

| Lo que premia Roblox ahora | Cómo encaja HUNDIDOS |
|---|---|
| Desde junio de 2026 el algoritmo de recomendaciones mide la **retención a 28 días**, y desde agosto, retención y monetización juntas. | La progresión es larga: barco base, tripulación, colección de artefactos y un museo. Hay razones para volver la semana siguiente, no solo al día siguiente. |
| La sección **Standout Games** (curada a mano) busca juegos *novedosos*: mecánicas poco habituales, estilo visual propio y mezclas de géneros que aprovechen avatares y funciones sociales. Los clones lo tienen difícil. | Mezcla extracción cooperativa con temática naval, que casi nadie toca en Roblox. Se puede postular. |
| Los grandes éxitos recientes de no-tycoon son **cooperativos con tensión**: 99 Nights in the Forest, Doors y Animal Hospital, que salió en mayo de 2026 y ganó 4 premios de innovación. | El núcleo es cooperativo y el reloj es visible (el agua sube), pero el tono es más cómico que de terror puro. Eso amplía la edad del público. |
| En Steam, los cooperativos «friendslop» (Lethal Company, R.E.P.O., Peak) han sido un fenómeno. En mi búsqueda **no encontré** un equivalente dominante en Roblox. | Llegáis antes a un hueco probado en otra plataforma. *Ojo: que mi búsqueda no lo encontrara no prueba que no exista; revisadlo en Roblox (sección 8).* |
| El público de 13 años o más crece más rápido, y el de 18 o más gasta un 50 % más. Hay **+42 % de DevEx** por el gasto de mayores de 18 verificados en EE. UU. (en juegos con R15). | El humor físico y el caos con amigos funcionan para adolescentes y adultos. Usad R15 desde el principio. |
| La sesión media en Roblox dura **9,8 minutos**, y el 44 % juega en PC y en móvil. | Una inmersión dura entre 6 y 10 minutos. Controles simples (coger, soltar, lanzar), pensados para móvil desde el primer día. |

**Lo que descarté y por qué:**
- **Otro «Steal a …» o tycoon:** domina las listas, pero está saturado de clones. Para destacar hace falta marketing que un equipo de 3 no puede igualar.
- **Simulador de pulsar botones:** muy saturado y retención de libro.
- **Terror puro:** es viable, pero ahora mismo compite contra 99 Nights, Doors y Animal Hospital en su terreno.
- **Juego deportivo:** hay demanda, pero las señales son débiles según las propias fuentes, y exige un netcode de físicas muy fino.

---

## 2. El juego en una frase y el bucle principal

**Un barco se hunde. Tú y tus amigos tenéis 8 minutos para sacar la carga más valiosa. Lo que no saquéis, se lo queda el mar.**

```
HUB (muelle / vuestro barco)
  → Elegir pecio (dificultad, tipo de carga, peligros)
  → INMERSIÓN (6–10 min): explorar, coger, cargar entre dos, sacar por grúa/bote
       · El agua sube por compartimentos (reloj visible)
       · Objetos pesados = 2 jugadores · frágiles = no golpear · eléctricos = no mojar
       · Peligros: pulpo/tiburón, explosiones de calderas, puertas atascadas, corrientes
  → LIQUIDACIÓN: el botín se vende → cuota de la empresa (si no se cumple, «despido» = reinicio de racha)
  → Mejoras: barco, equipo (arnés, bomba de achique, grúa), tripulación, cosméticos
  → Artefactos raros → MUSEO personal visitable por otros jugadores
```

**Qué lo hace divertido** (lo que hay que validar con el prototipo):
1. **Comedia física.** Dos jugadores cargando un piano por un pasillo inclinado mientras sube el agua. Eso son clips para TikTok y YouTube Shorts, que es vuestro marketing gratis.
2. **Decisiones bajo presión.** ¿Volvemos a por el cofre o salimos ya? ¿Abrimos la escotilla aunque inunde el pasillo?
3. **Roles que surgen solos.** Uno achica, otro carga, otro vigila al bicho. No hace falta imponer clases.

---

## 3. Sistemas que dan retención (D7 y D30)

- **Progresión del barco base:** el barco es vuestro hub y cambia visualmente al mejorarlo. La identidad del grupo vive ahí.
- **Colección de artefactos:** un libro tipo Pokédex con más de 100 piezas raras por tipo de pecio. El museo se puede visitar, lo que da estatus social.
- **Pecios del día y de la semana**, con modificadores (tormenta, noche, hielo).
- **Evento semanal «Leviatán»:** un jefe cooperativo. Usad *Experience Events* de Roblox, que Standout Games recomienda.
- **Rachas de cuota** con recompensas cosméticas por mantenerlas.
- **Temporadas de unas 6 semanas** con un nuevo tipo de pecio: transatlántico, submarino, nave hundida en un lago helado, galeón…

---

## 4. Monetización (sin pagar para ganar)

| Producto | Tipo |
|---|---|
| Trajes de buzo, cascos, efectos de burbujas, skins del barco | Cosméticos (Game Pass y Developer Products) |
| Pase de temporada (gratuito + premium) | Recurrente |
| Servidores privados | Encaja de forma natural con un juego para jugar con amigos |
| Ampliación del museo, más vitrinas | Comodidad o estatus |
| Revivir a un compañero una vez por inmersión | Developer Product **con límite**, para no romper el juego |

Referencia: solo el **3,8 %** de los jugadores paga (mediana de GameAnalytics 2026). Con un catálogo amplio de cosméticos y un pase de temporada se le saca más a ese 3,8 %, sin enfadar al 96 % restante.

---

## 5. Alcance realista para 3 personas

### Reparto sugerido
| Persona | Responsabilidad |
|---|---|
| **A: Sistemas (Luau)** | Servidor autoritativo: agua, carga de objetos y propiedad de red de las físicas, economía, guardado (DataStore/ProfileStore), antitrampas. |
| **B: Mundo y arte** | Habitaciones modulares de barco (generación procedural por piezas), iluminación, efectos de agua, criaturas, estilo visual propio. |
| **C: Experiencia y crecimiento** | Interfaz, controles para móvil, tutorial (el D1 depende de los primeros 60 segundos), monetización, analítica, Discord, TikTok y anuncios. |

Los tres tenéis Claude Pro: usadlo para generar y revisar Luau, documentar sistemas y escribir textos. **Montad Rojo + Git** para que el código del juego viva en este repositorio y podáis trabajar en paralelo sin pisaros.

### Hitos
| Fase | Duración orientativa | Entregable | Criterio para seguir |
|---|---|---|---|
| **0. Prototipo de diversión** | 2–3 semanas | 1 barco fijo, agua que sube, coger y cargar entre dos, 1 peligro. Sin arte. | Probadlo con 10 a 20 personas ajenas al equipo. Si no hay risas ni «otra más», **cambiad el enfoque antes de invertir más**. |
| **1. MVP** | 2–3 meses | 3 tipos de pecio procedurales, hub, unas 20 mejoras, 1 criatura, móvil completo, tutorial, guardado. | Funciona estable con 4 jugadores en móvil de gama media. |
| **2. Lanzamiento suave** | 2–4 semanas | Publicación con anuncios patrocinados de presupuesto pequeño. | Medir D1, D7, duración de sesión y tasa de rebote en la primera partida. Comparar con la tabla de abajo. |
| **3. Escalar** | continuo | Actualización semanal pequeña, temporada cada ~6 semanas, postulación a Standout Games. | Retención estable o al alza. |

### Métricas de referencia (GameAnalytics 2026, más de 500 juegos)
| | Mediana | Top 1 % |
|---|---|---|
| D1 | 10,3 % | 22,2 % |
| D7 | 1,6 % | 9,1 % |
| D30 | 0,5 % | 4,7 % |

Para un «éxito decente», apuntad a **D1 ≥ 15 % y D7 ≥ 4 %** en el lanzamiento suave. Esa cifra es mi criterio, no una garantía. Si os quedáis muy por debajo, arreglad el tutorial y el primer pecio antes de gastar más en anuncios.

---

## 6. Riesgos técnicos y cómo reducirlos

| Riesgo | Mitigación |
|---|---|
| Físicas de objetos cargados entre varios jugadores (lag, temblores) | Asignar la propiedad de red al portador principal. Cargar «entre dos» = restricción simple + reducir velocidad, no física realista. Prototipar esto **lo primero**. |
| Agua que sube | Nada de agua de terreno dinámica: usad un plano o volumen por compartimento que sube con tween, y daño o ralentización por zona. Barato y legible en móvil. |
| Rendimiento en móvil | Presupuesto de piezas por habitación, *streaming* activado, pocas luces dinámicas. |
| Trampas (teletransportar botín, duplicar dinero) | El servidor valida todas las ventas y posiciones. Nunca confiar en el cliente. |
| Que se perciba como copia de R.E.P.O. o Lethal Company | La identidad diferencial es **el barco que se hunde y el agua como reloj**. Nada de robots, monstruos o estética prestada de esos juegos. |

---

## 7. Variantes si la idea principal no convence en el prototipo

1. **Mudanzas imposibles:** el mismo motor de «cargar entre varios», pero en casas que se derrumban, se queman o se inundan. Más urbano, menos original.
2. **Rescate en montaña / avalancha:** extracción de personas y equipo con frío y tormenta como reloj.
3. **Brigada de bomberos cooperativa:** apagar y rescatar a la vez. Hay que revisar la competencia en Roblox.

Las tres reutilizan el 70–80 % del código del prototipo, así que cambiar de rumbo sale barato.

---

## 8. Antes de comprometeros (tareas para esta semana)

- [ ] Buscar en Roblox: «sinking ship», «salvage», «shipwreck», «diver», «extraction co-op». Apuntad la competencia directa y su número de jugadores simultáneos (CCU). No pude consultar las listas oficiales desde esta sesión.
- [ ] Mirar Rolimons o RoMonitor para comprobar cuántos cooperativos de extracción hay ahora en el top 200.
- [ ] Decidir el nombre definitivo y comprobar que está libre en Roblox.
- [ ] Montar Rojo + Git en este repositorio.
- [ ] Empezar la Fase 0.

---

## 9. Fuentes

Las consulté mediante buscador. Las páginas oficiales de Roblox no se podían abrir directamente desde esta sesión, así que algunos datos vienen de resúmenes de terceros.

- Cambio de algoritmo de junio de 2026: [Roblox Newsroom – Optimizing Discovery](https://about.roblox.com/newsroom/2026/06/optimizing-discovery-great-games-reach-millions-players-roblox) · [lensblox](https://lensblox.com/blog/roblox-algorithm-change-2026-explained/)
- Standout Games: [Documentación de Roblox](https://create.roblox.com/docs/creator-programs/standout-games)
- DevEx +42 % para mayores de 18: [Roblox Newsroom](https://about.roblox.com/newsroom/2026/04/roblox-fuels-high-fidelity-games-over-18-players-increases-qualifying-devex-rate-42)
- Benchmarks de retención y monetización: [GameAnalytics 2026 Roblox Report](https://www.gameanalytics.com/reports/2026-roblox-report) · [Resumen en gamedevreports](https://gamedevreports.substack.com/p/gameanalytics-key-roblox-and-roblox)
- Audiencia por edad: [Newzoo/GEEIQ en gamedevreports](https://gamedevreports.substack.com/p/newzoo-and-geeiq-the-roblox-audience) · [eMarketer](https://www.emarketer.com/content/roblox-com-s-adult-audience-bigger-than-you-think) · [Konvoy (visión escéptica)](https://www.konvoy.vc/content/can-roblox-age-up)
- Tendencias y éxitos de 2026: [Lista de juegos de Roblox (Wikipedia)](https://en.wikipedia.org/wiki/List_of_Roblox_games) · [Grow a Garden (Wikipedia)](https://en.wikipedia.org/wiki/Grow_a_Garden) · [Animal Hospital – GosuGamers](https://www.gosugamers.net/entertainment/news/78741-animal-hospital-becomes-roblox-s-latest-horror-sensation-here-s-everything-you-need-to-know)
- Saturación de géneros (blogs y proveedores, poco fiables): [RoLearn](https://rolearn.dev/insights/unsaturated-roblox-game-genres-2026/) · [RoWatcher – tycoons](https://rowatcher.com/news/tycoon-games-the-genre-that-built-roblox-and-still-hasn-t-peaked) · [RoWatcher – mapa de oportunidades](https://rowatcher.com/news/roblox-genre-opportunity-map-2026-where-smart-developers-are-building-next)
- Friendslop: [Wikipedia](https://en.wikipedia.org/wiki/Friendslop) · [Insider Gaming](https://insider-gaming.com/best-friendslop-games-you-need-to-play/)
