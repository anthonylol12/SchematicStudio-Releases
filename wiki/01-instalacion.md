# 1. Descargar e instalar

[← Índice](README.md) · [Siguiente: Conocer la ventana →](02-la-ventana.md)

## Lo que necesitas

| Requisito | Detalle |
|---|---|
| Sistema | Windows 10 u 11 de **64 bits** |
| Tarjeta gráfica | Cualquiera compatible con Direct3D 11 (casi todas desde 2012) |
| Espacio | Unos 100 MB |
| Minecraft (recomendado) | Instalado con el launcher oficial o con CurseForge. El programa lee de ahí las **texturas** y la **lista de bloques** de cada versión. No copia ni distribuye nada del juego. |

> Sin Minecraft instalado el programa funciona igual, pero muestra los bloques con colores en vez de texturas y solo puede convertir a versiones antiguas (1.8.9 a 1.12.2).

## Paso a paso

1. Ve a la página de **[Releases](../../../releases/latest)**.
2. En **Assets**, haz clic en **`SchematicStudio-0.8.0-win-x64.zip`** para descargarlo.
3. Busca el archivo en tu carpeta de **Descargas**, haz clic derecho → **Extraer todo…** → **Extraer**.
4. Dentro de la carpeta, haz doble clic en **`SchematicStudio.exe`**.
5. La primera vez Windows puede mostrar un aviso azul:

   > **Windows protegió su PC** — Microsoft Defender SmartScreen impidió el inicio de una aplicación no reconocida.

   Pulsa **Más información** y después **Ejecutar de todas formas**. Aparece porque el programa es nuevo y no está firmado con un certificado de pago; solo pasa la primera vez.

6. ¡Listo! Se abre la ventana principal.

## Tenerlo en el menú Inicio (opcional)

En la misma carpeta hay un archivo **`Instalar.ps1`**:

1. Clic derecho sobre **`Instalar.ps1`** → **Ejecutar con PowerShell**.
2. Copia el programa a tu carpeta de programas y crea **Schematic Studio** en el menú Inicio. No pide permisos de administrador.

Para quitarlo más adelante, abre PowerShell en esa carpeta y escribe:

```
powershell -File Instalar.ps1 -Desinstalar
```

Tus ajustes y reglas se guardan en `%APPDATA%\SchematicStudio` y no se borran al desinstalar.

## La primera vez que se abre

- Abajo verás en el **Registro** un mensaje como *«Base de datos de bloques lista: 22 versiones…»*. El programa ha leído las versiones de Minecraft que tienes instaladas. Tarda unos segundos la primera vez; las siguientes es instantáneo.
- Poco después aparece *«Texturas y modelos del juego cargados…»*: a partir de ahí el visor 3D muestra las texturas reales.
