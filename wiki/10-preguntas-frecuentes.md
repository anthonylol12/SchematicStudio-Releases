# 10. Preguntas frecuentes y problemas

[← Proyectos](09-proyectos.md) · [Índice](README.md) · [Siguiente: Glosario →](11-glosario.md)

### Windows no me deja abrirlo («Windows protegió su PC»)
Pulsa **Más información → Ejecutar de todas formas**. Pasa porque el programa no está firmado con un certificado de pago. Solo ocurre la primera vez.

### Los bloques salen de colores lisos, sin texturas
- Comprueba que el botón **Texturas** está activado (azul).
- Las texturas se leen de tu Minecraft instalado. Si no tienes ninguna versión instalada con el launcher oficial o CurseForge, el programa usa colores. Instala una versión (basta con abrirla una vez desde el launcher) y vuelve a abrir Schematic Studio.

### En «Destino» no aparece la versión que quiero
Las versiones de **1.8.9 a 1.12.2** están siempre. Las de **1.13 en adelante** aparecen si están instaladas en tu launcher. Instálala (ábrela una vez) y reinicia el programa.

### Al convertir salen muchos bloques en rojo («Sin equivalencia»)
Son bloques que no existen en la versión de destino y para los que no hay nada lo bastante parecido. Opciones:
1. Usa **Cambiar…** en cada fila y elige tú el sustituto ([ver cómo](05-convertir-version.md#elegir-tú-el-sustituto)).
2. Baja la **Similitud** (por ejemplo a 40 %) y vuelve a convertir.
3. Al exportar, deja marcada «usar la opción más parecida».

### ¿Por qué un bloque sale como «aire» al exportar?
Porque no existe en esa versión y no le has dado sustituto. El informe de exportación te dice cuáles son.

### He pegado la construcción y aparece desplazada
Revisa el **origen** (bloque magenta). Al pegar con WorldEdit, el origen queda en tu posición. Cámbialo en [Transformaciones](08-transformaciones.md) con **Centrar origen**, **Ajustar al suelo** u **Origen en selección**.

### El archivo `.nbt` no carga en el bloque de estructuras
El bloque de estructuras solo admite hasta **48 × 48 × 48** desde su menú. Usa `/place template minecraft:nombre` o exporta a `.schem`.

### ¿Puede estropear mi archivo original?
No. El programa abre los archivos solo para leer. Todo lo que guardas va a archivos nuevos, y si sobrescribes uno existente se hace antes una copia `.bak`.

### El programa va lento con construcciones enormes
- Desactiva **Texturas** (modo colores).
- Oculta materiales que no necesites ver (pestaña Materiales, casillas).
- Construcciones de millones de bloques se cargan poco a poco: puedes ir mirando mientras termina.

### ¿Dónde guarda el programa sus ajustes?
En `%APPDATA%\SchematicStudio` (pega esa ruta en la barra del Explorador de archivos): ajustes, reglas de sustitución (`rules.json`) y copias de recuperación.

### ¿Qué hago si encuentro un error?
Mira las pestañas **Registro**, **Advertencias** y **Errores** del panel inferior: ahí aparece lo que ha pasado. Anota el mensaje y los pasos para repetirlo.

### En Minecraft 1.12.2 la construcción sale aplastada (una sola capa plana)
Pasaba con los `.schematic` exportados con la versión 0.8.1 o anterior cuando la construcción venía de un mundo moderno a poca altura (por ejemplo, Y = −60): WorldEdit 6 la recortaba a la altura del mundo de 1.12.2. **Actualiza a la 0.8.2 o posterior y vuelve a exportarla.**

### Al pegar con WorldEdit se borra el terreno alrededor
`//paste` pega también el aire de la caja de la construcción. Usa **`//paste -a`** para pegar solo los bloques.
