# Horizon Android

Port experimental de Horizon para Android, basado en Horizon.

## Estado

- Compila como aplicación ARM64 con Vulkan.
- Instalado y probado en un POCO X7 Pro: abrió un mundo guardado y el joystick virtual movió al jugador.
- Las lecturas F3 han variado entre 25 y 120 FPS según la escena. Son capturas puntuales, no una prueba sostenida.
- Los controles, la estabilidad, la configuración inicial y la compatibilidad con otros dispositivos siguen en desarrollo.

## Descargar

Las versiones de prueba aparecerán en [Releases](https://github.com/Gruktoolz/horizon-android/releases). El APK de desarrollo está firmado con una clave de prueba; no es una versión de producción.

## Preparar y abrir los archivos del juego

El APK no incluye ni descarga Minecraft Java Edition, sus recursos, mundos ni texturas. Para iniciar el juego necesitas preparar los archivos de tu propia copia de Java Edition 26.3 en una computadora y copiarlos al almacenamiento privado de Horizon en Android.

1. Instala Java Edition 26.3 con el launcher oficial usando la cuenta que posee el juego y ejecútalo una vez. Esto descarga en esa computadora los archivos de la versión.
2. Desde una copia local del código fuente de Horizon, prepara los recursos. Ten JDK 25 instalado y proporciona la ruta a tu archivo de servidor 26.3:

   ```sh
   cargo run --release -p horizon-prepare -- --prepare --server-jar "$HOME/Downloads/server.jar"
   ```

   La preparación usa los archivos de la instalación local y escribe los recursos generados bajo `.local/horizon-client/26.3`. Esa carpeta es privada y está excluida de Git.
3. Conecta el teléfono por USB, activa la depuración USB y compila/instala la aplicación si todavía no está instalada:

   ```sh
   bash tools/android.sh build
   bash tools/android.sh install
   ```
4. Copia los recursos preparados al espacio privado de la aplicación:

   ```sh
   bash tools/android.sh resources "$PWD/.local/horizon-client/26.3"
   ```

   El script valida `horizon-resources.json` y coloca los archivos en el directorio privado de Horizon. No hace falta dar permiso de almacenamiento compartido.
5. Abre Horizon en el teléfono:

   ```sh
   bash tools/android.sh run
   ```

Si hay más de un teléfono conectado, define `ANDROID_SERIAL` con el identificador que muestra `adb devices -l`. Para ver el registro de la app puedes ejecutar `bash tools/android.sh logs`.

El repositorio y el APK no distribuyen los recursos del juego. Cada persona prepara y transfiere su propia copia; la app abre los archivos desde su almacenamiento privado.

## Construir

Consulta [docs/android.md](docs/android.md) para dependencias, opciones y estado detallado del port.
