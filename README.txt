XJeyMods V18 - integración de KEY

IMPORTANTE
- Package de esta reconstrucción: com.holovip
- Firebase project: xjeymods
- Realtime Database: https://xjeymods-default-rtdb.firebaseio.com
- La APK NO escribe directamente en Realtime Database.
- El backend validateKey es quien activa, vincula y expira la KEY.

1) Backend
Abre firebase-backend en Firebase Cloud Shell.
Instala/deploya con Firebase CLI:
  firebase login
  firebase use xjeymods
  firebase deploy --only functions

2) Base de datos
La estructura debe ser:
  keys
    xjey-mods-XXXX
      deviceId: ""
      activatedAt: 0
      expiresAt: 0
      active: false

No abras las reglas al cliente. Mantén .read=false y .write=false.

3) AndroidIDE
Abre la carpeta XJeyMods_V18_Project como proyecto Gradle.
Sincroniza y compila.

4) KEY
La pantalla de login llama a validateKey antes de mostrar el panel.
Una KEY nueva queda vinculada al Android ID del dispositivo y dura 12 horas.

NOTA
Esta reconstrucción conserva el HTML y recursos extraídos de la APK recibida. La APK original era compilada; por eso esta carpeta es un proyecto Android nuevo que reproduce su panel y añade la autenticación por KEY.
