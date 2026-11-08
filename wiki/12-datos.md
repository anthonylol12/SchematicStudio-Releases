# 12. Datos técnicos: formatos, versiones y pruebas

[← Glosario](11-glosario.md) · [Índice](README.md)

Para quien quiera los detalles.

## Formatos

| Formato | Lee | Escribe | Versiones | Guarda origen | Notas |
|---|:-:|:-:|---|:-:|---|
| `.schem` Sponge v3 | ✅ | ✅ | 1.13+ | ✅ y posición en el mundo | WorldEdit 7.3+, FAWE |
| `.schem` Sponge v2 | ✅ | ✅ | 1.13+ | ✅ y posición en el mundo | WorldEdit 7.0–7.2 |
| `.schem` Sponge v1 | ✅ | — | 1.13+ | ✅ | Formato antiguo de WorldEdit |
| `.schematic` | ✅ | ✅ | 1.8.9 – 1.12.2 | ✅ y posición en el mundo | IDs numéricos; WorldEdit 6, MCEdit, Schematica |
| `.litematic` | ✅ | ✅ | 1.13+ | ✅ | Varias regiones se combinan en una |
| `.nbt` | ✅ | ✅ | 1.13+ | — | Bloque de estructuras; máx. 48³ desde su menú |

Los archivos se reconocen por su contenido, comprimidos o no.

## Versiones

- **1.8.9 a 1.12.2:** siempre disponibles (tabla interna de IDs).
- **1.13 en adelante:** las que tengas instaladas en el launcher oficial o CurseForge. De cada una se lee la lista exacta de bloques, sus propiedades (catálogo oficial generado por el propio juego) y las texturas.
- Los cambios de nombre entre versiones se tienen en cuenta (por ejemplo `grass` → `short_grass`, `chain` → `iron_chain`).

## Pruebas realizadas

| Prueba | Resultado |
|---|---|
| Pruebas automáticas del programa | **195** (todas correctas) |
| Estructuras `.nbt` colocadas en Minecraft 26.3, 1.21.11 y 1.20.1 y leídas del mundo | 99,0 – 100 % de bloques idénticos (las diferencias son física del juego: hojas que caen, plantas sin soporte…) |
| Todos los estados de bloque exportados validados con `/setblock` | 26.3: 1.724 de 1.724 · 1.21.11: 906 de 906 · 1.20.1: 1.737 de 1.737 |
| Archivos `.schem` cargados y vueltos a guardar con WorldEdit 7.4.2 | 100 % de bloques y entidades de bloque idénticos |
| Giros y reflejos comparados con los de Minecraft (28 colocaciones) | Mismos resultados que la colocación sin girar |
| `.schematic` colocados en Minecraft 1.12.2 | 100 % de bloques correctos, 99,6 % idénticos |
| Construcciones reales abiertas | 98 de 98 sin errores |

## Rendimiento (ordenador portátil con RTX 4070)

| Construcción | Bloques | Abrir | Caras dibujadas |
|---|---|---|---|
| Casa de ejemplo | 1.084 | 43 ms | ~5.000 |
| Construcción grande | 672.422 | 0,2 s | 270.000 (las caras iguales se unen) |
| Mapa enorme | 475 millones de posiciones | por partes | se carga poco a poco |

## Privacidad

- El programa **no se conecta a internet**.
- Solo **lee** los archivos de Minecraft instalados; no los modifica ni los copia.
- Tus ajustes y reglas se guardan solo en tu ordenador (`%APPDATA%\SchematicStudio`).

## Aviso

Schematic Studio es un proyecto independiente: no es un producto oficial de Minecraft ni está aprobado por Mojang o Microsoft. «Minecraft» es una marca de Mojang Synergies AB.
