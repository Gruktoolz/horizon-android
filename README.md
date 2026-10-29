# Horizon Android

Port experimental de Horizon para Android, basado en Horizon.

## Descargas

- [Descargar APK para Android ARM64](https://github.com/Gruktoolz/horizon-android/releases/download/v0.1.0-android-preview.1/horizon-android.apk)
- [Descargar el código fuente completo](https://github.com/Gruktoolz/horizon-android/releases/download/v0.1.0-android-preview.1/horizon-android-source-v2.zip)

La compilación es experimental, está firmada con una clave de desarrollo y no es una versión de producción. La importación de recursos desde ZIP está en pruebas.

## Instalar tus recursos en Android

Horizon no incluye Minecraft ni sus recursos. Necesitas un ZIP preparado con los archivos de tu propia copia de Java Edition 26.3. Debe contener `horizon-resources.json`, `assets/` y `data/` directamente en la raíz.

1. Descarga o copia el ZIP de recursos en **Descargas** del teléfono o tablet.
2. Cierra Horizon si está abierto.
3. En **Archivos** o **Descargas**, toca el ZIP y elige **Horizon**.
4. Espera a que Horizon lo valide y lo importe en su almacenamiento privado.
5. Abre Horizon normalmente. No hace falta descomprimir el ZIP, conectar USB, buscar `Android/data` ni conceder acceso general al almacenamiento.

Los mundos y las partidas guardadas son archivos aparte; este ZIP solo contiene recursos.

## Si aún no tienes el ZIP

La preparación de tus recursos se hace una sola vez en una computadora. Instala y ejecuta Java Edition 26.3 con el launcher oficial, descarga el [código fuente](https://github.com/Gruktoolz/horizon-android/releases/download/v0.1.0-android-preview.1/horizon-android-source-v2.zip), extrae la carpeta, instala JDK 25 y ejecuta desde la raíz del código:

```sh
cargo run --release -p horizon-prepare -- --prepare --server-jar "$HOME/Downloads/server.jar"
mkdir -p .local/android
cd .local/horizon-client/26.3
zip -r ../../android/horizon-android-resources-26.3.zip .
```

Cambia la ruta de `server.jar` si lo guardaste en otro lugar. Copia el ZIP creado al teléfono y sigue los cinco pasos anteriores.

Cada persona prepara sus propios recursos. El APK y el repositorio no distribuyen recursos, texturas ni mundos de Minecraft.

## Estado

Probado en un POCO X7 Pro: abrió un mundo guardado y el joystick virtual movió al jugador. Las lecturas F3 anteriores variaron entre 25 y 120 FPS según la escena; son capturas puntuales, no una prueba sostenida. Los controles, la estabilidad, la importación en dispositivo real y la compatibilidad con otros equipos siguen en desarrollo.
