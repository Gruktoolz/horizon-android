# Horizon Android

## Proyecto

Horizon para Android reúne un launcher de Minecraft Java con mejoras de juego para pantallas táctiles. Basado en Horizon. La versión actual es **0.2.1 Alpha**, una prueba pública en desarrollo.

[Canal de difusión de WhatsApp](https://chat.whatsapp.com/ETt0UhVPo0FKySJSzFy05h) · [Grupo de soporte](https://chat.whatsapp.com/JUeYn6NjOiE7HDP0rHM3Le)

## Funcionamiento

**Jugar** permite importar recursos y abrir el juego. **Versiones** muestra la versión disponible y **Ajustes** reúne las opciones del launcher. Incluye controles táctiles revisados, cambio de perspectiva y botones para abrir el teclado y cerrar el chat.

**Modo ligero** aplica renderizado y simulación de 4 chunks, límite de 30 FPS y efectos reducidos. Puedes desactivarlo para recuperar los ajustes anteriores. No garantiza alcanzar 30 FPS.

**Jugar → Reportar error** genera un TXT con datos del dispositivo, errores y actividad reciente para compartirlo desde Android, por ejemplo mediante WhatsApp. Revisa el contenido antes de enviarlo. **Ajustes → Diagnóstico para Excel** guarda un informe más completo.

### Instalar los recursos

1. Guarda en el teléfono un ZIP preparado para Horizon con los recursos de tu copia de Minecraft Java 26.3.
2. Abre **Jugar → Instalar ZIP** y selecciona el archivo en Descargas. **No lo descomprimas**.
3. Espera la confirmación y pulsa **JUGAR**.

El APK no incluye Minecraft ni sus recursos y todavía no prepara el ZIP desde el teléfono. Un ZIP genérico de texturas no sustituye el paquete completo. Los mundos se administran aparte. Las correcciones de interfaz requieren actualizar también el APK.

Requisitos actuales: **Android 10 o posterior y ARM64**. No hay soporte de Android de 32 bits ni compatibilidad certificada con 2 GB de RAM. El inicio de sesión Microsoft no está configurado en este APK. Conserva una firma de desarrollo; sigue siendo una alpha y necesita pruebas en más dispositivos.

## Descargas

- [Descargar Horizon Android 0.2.1 Alpha (APK, 141.67 MiB)](https://github.com/Gruktoolz/horizon-android/releases/download/v0.2.1-alpha.1/Horizon-Android.apk)
- [Todos los cambios y problemas conocidos](https://github.com/Gruktoolz/horizon-android/releases/tag/v0.2.1-alpha.1)

### Capturas del launcher

Las capturas muestran la presentación inicial del launcher; los botones de diagnóstico y modo ligero se añadieron después.

**Jugar**
![Pantalla Jugar](https://raw.githubusercontent.com/Gruktoolz/horizon-android/main/docs/media/android-launcher-play.png)

**Versiones**
![Pantalla Versiones](https://raw.githubusercontent.com/Gruktoolz/horizon-android/main/docs/media/android-launcher-versions.png)

**Ajustes**
![Pantalla Ajustes](https://raw.githubusercontent.com/Gruktoolz/horizon-android/main/docs/media/android-launcher-settings.png)

## Roadmap

- Investigar cierres y bajos FPS con los nuevos reportes.
- Reducir memoria y probar sesiones largas, pausa/reanudación e importaciones interrumpidas en varios dispositivos.
- Ampliar la personalización de controles y las opciones de accesibilidad.
- Completar acceso de cuenta, administración de versiones, perfiles y ajustes.
- Evaluar soporte de 32 bits por separado; todavía no está disponible.
- Evaluar asistencia de combate opcional y configurable: ayuda de apuntado suave, auto-hit acompasado al cooldown y activación press o toggle. Son propuestas futuras y deberán respetar las reglas de cada servidor.
