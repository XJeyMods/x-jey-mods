# XJeyMods V18 — GitHub Actions

Este proyecto está preparado para que GitHub compile automáticamente la APK.

## Compilar

- Sube el proyecto a GitHub.
- Ve a **Actions**.
- Ejecuta **XJeyMods V18 - Build APK**.
- Al terminar, abre la ejecución y descarga el artifact **XJeyMods-V18-APK**.

El workflow también se ejecuta automáticamente al hacer `push` a `main` o `master`.

## Resultado

`XJeyMods-V18.apk`

La compilación actual es **Debug**. Para una versión Release firmada se debe configurar un
keystore mediante GitHub Secrets; nunca se debe guardar la clave privada dentro del repositorio.
