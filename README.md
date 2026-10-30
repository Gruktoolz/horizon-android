# Horizon Android

## Proyecto

Horizon Android combina un launcher de Minecraft Java con controles para pantallas táctiles y herramientas de diagnóstico. Basado en Horizon. La versión actual es **0.3.0 Alpha 2**, todavía en desarrollo.

[Canal de difusión](https://chat.whatsapp.com/ETt0UhVPo0FKySJSzFy05h) · [Grupo de soporte](https://chat.whatsapp.com/JUeYn6NjOiE7HDP0rHM3Le)

## Funcionamiento

### Instalar y jugar desde el teléfono

1. [Descarga el APK](https://github.com/Gruktoolz/horizon-android/releases/download/v0.3.0-alpha.2/Horizon-Android.apk) e instálalo.
2. Abre **Horizon.debug → Jugar → Descargar recursos**. La app descarga el paquete actualizado desde Dropbox, lo verifica y lo instala.
3. Espera el mensaje **Recursos instalados** y pulsa **JUGAR**.

Si ya tienes recursos, pulsa **Reparar recursos** para instalar el paquete actualizado. Puedes pausar la descarga y continuar después.

**Alternativa manual:** [descarga el ZIP completo de recursos y controles](https://www.dropbox.com/scl/fi/xw9qbitivxzbb1ptarvyr/horizon-recursos-26.3-bedrock-v0.3.1.zip?rlkey=ioikjtnzmfw3ufrghs7xbiiy7&dl=1), guárdalo en Descargas y selecciónalo desde **Jugar → Importar ZIP**. **No lo descomprimas ni lo muevas a carpetas ocultas.** No necesitas una PC ni comandos para instalar este paquete preparado.

El APK y los recursos se descargan por separado. El paquete completo corresponde a Minecraft Java 26.3 y contiene los controles actualizados; un ZIP genérico de texturas no lo sustituye. Los mundos se administran aparte.

### Controles

Entra en una partida y abre **Pausa → Opciones → Controles → Personalizar controles táctiles**. Puedes mover botones, cambiar tamaño y opacidad, restablecer, guardar o cancelar. El selector ofrece joystick o cruceta, con mira o interacción mediante toque.

Durante el juego se mantienen los botones superiores de **perspectiva (F5), chat y pausa**. El teclado dispone de acceso contextual para volver a abrirlo y de controles para enviar o cerrar el chat.

### Rendimiento y reportes

**Modo ligero** aplica distancias de 4 chunks, límite de 30 FPS, resolución de mundo reducida y efectos mínimos. Puedes desactivarlo para recuperar los ajustes anteriores. No garantiza alcanzar 30 FPS.

**Jugar → Reportar error** genera un TXT con información del dispositivo, errores y actividad reciente, que puedes compartir desde Android. **Ajustes → Diagnóstico para Excel** exporta un informe más completo. El registro detallado de rendimiento es opcional.

### Requisitos y actualización

- **Android 10 o posterior, ARM64 y Minecraft Java 26.3**.
- Esta build aparece como **Horizon.debug** y actualiza la prueba instalada con ese nombre. Puede coexistir con las previews antiguas y no migra automáticamente sus mundos o cuentas. No desinstales la app anterior para intentar actualizar.
- Puedes jugar sin conexión sin iniciar sesión. El acceso Microsoft y la renovación de sesión están integrados; requieren la cuenta correspondiente.
- Sigue siendo una **alpha con firma de desarrollo**. No añade soporte para Android de 32 bits ni certifica equipos de 2 GB. Los cierres, bajos FPS y problemas de movimiento en servidores siguen en investigación.

## Descargas

- [Horizon Android 0.3.0 Alpha 2 — APK](https://github.com/Gruktoolz/horizon-android/releases/download/v0.3.0-alpha.2/Horizon-Android.apk)
- [Recursos completos y controles actualizados — ZIP en Dropbox, 395 MiB](https://www.dropbox.com/scl/fi/xw9qbitivxzbb1ptarvyr/horizon-recursos-26.3-bedrock-v0.3.1.zip?rlkey=ioikjtnzmfw3ufrghs7xbiiy7&dl=1)
- [Cambios y problemas conocidos de esta versión](https://github.com/Gruktoolz/horizon-android/releases/tag/v0.3.0-alpha.2)

### Capturas del launcher

Estas capturas muestran la presentación inicial; la versión actual añade descarga, reparación, diagnóstico y modo ligero.

**Jugar**
![Pantalla Jugar](https://raw.githubusercontent.com/Gruktoolz/horizon-android/main/docs/media/android-launcher-play.png)

**Versiones**
![Pantalla Versiones](https://raw.githubusercontent.com/Gruktoolz/horizon-android/main/docs/media/android-launcher-versions.png)

**Ajustes**
![Pantalla Ajustes](https://raw.githubusercontent.com/Gruktoolz/horizon-android/main/docs/media/android-launcher-settings.png)

## Roadmap

- Investigar cierres, consumo de memoria, bajos FPS y correcciones de movimiento en servidores.
- Probar sesiones largas, pausa/reanudación e instalaciones interrumpidas en más dispositivos Mali y Adreno.
- Pulir gestos táctiles, editor, accesibilidad e integración del teclado.
- Ampliar la administración real de versiones y perfiles.
- Mejorar renovación y recuperación de errores de cuenta.
- Evaluar soporte de 32 bits por separado.
- Evaluar asistencia de combate opcional y configurable: ayuda de apuntado suave, auto-hit acompasado al cooldown y activación press o toggle, según las reglas de cada servidor.
