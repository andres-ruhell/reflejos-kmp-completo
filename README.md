# Reflejos KMP

App terminada de la mini práctica de Kotlin Multiplatform (Aplicaciones Móviles, Ibero CDMX, noviembre 2026). Es un juego de reflejos que corre en escritorio, Android e iOS con el mismo código.

Es la plantilla oficial de [kmp.jetbrains.com](https://kmp.jetbrains.com), con Android, iOS, escritorio, Share UI y pruebas, más estos tres archivos:

| Archivo | Qué hace |
|---|---|
| `shared/src/commonMain/kotlin/mx/ibero/reflejos/Juego.kt` | Lógica: estados, espera al azar, tiempo y récord |
| `shared/src/commonTest/kotlin/mx/ibero/reflejos/JuegoTest.kt` | Cuatro pruebas de la lógica |
| `shared/src/commonMain/kotlin/mx/ibero/reflejos/App.kt` | Interfaz con Compose Multiplatform |

## Correrlo

Necesitas Android Studio instalado. Desde la carpeta del proyecto:

**Mac (Terminal)**

```bash
export JAVA_HOME="/Applications/Android Studio.app/Contents/jbr/Contents/Home"
export ANDROID_HOME="$HOME/Library/Android/sdk"
./gradlew :shared:jvmTest
./gradlew :desktopApp:run
```

**Windows (PowerShell)**

```powershell
$env:JAVA_HOME = "C:\Program Files\Android\Android Studio\jbr"
$env:ANDROID_HOME = "$env:LOCALAPPDATA\Android\Sdk"
.\gradlew.bat :shared:jvmTest
.\gradlew.bat :desktopApp:run
```

- **Android:** enciende el emulador y corre `./gradlew :androidApp:installDebug` (Windows: `.\gradlew.bat :androidApp:installDebug`). También puedes elegir `androidApp` en Android Studio y presionar Run.
- **iOS (solo Mac con Xcode):** en Android Studio elige `iosApp` y presiona Run, o abre `iosApp/iosApp.xcodeproj` en Xcode.

La primera vez Gradle descarga Gradle, un Java 21 y las librerías; tarda varios minutos.

Versiones: Kotlin 2.4.21, Compose Multiplatform 1.12.2, Android Gradle Plugin 9.1.1, Gradle 9.5.1.
