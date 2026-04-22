¡Claro! Configurar el entorno para trabajar con **FlutterFlow** y **Firebase** es un paso clave para profesionalizar tu flujo de trabajo. Aquí tienes la guía completa paso a paso.

---

## 1. Instalación de Node.js y npm (Requisito previo)

Para gestionar herramientas como Firebase CLI, necesitas **Node.js** (que incluye **npm**, su gestor de paquetes).

### Software necesario
* **Instalador oficial:** Descargado de [nodejs.org](https://nodejs.org/).
* **Terminal:** Símbolo del sistema (CMD) o PowerShell en Windows; Terminal en macOS/Linux.

### Cómo verificar si ya están instalados
Abre tu terminal y escribe:
```bash
node -v
npm -v
```
Si aparecen números de versión (ej. `v20.10.0`), ya los tienes. Si ves un error como *"command not found"*, sigue estos pasos:

### Paso a paso para instalar Node.js (npm se instala solo)
1.  **Descarga:** Ve a [nodejs.org](https://nodejs.org/) y elige la versión **LTS** (la más estable).
2.  **Ejecuta el instalador:** Sigue los pasos (Siguiente, Siguiente...).
3.  **IMPORTANTE (Windows):** Asegúrate de marcar la casilla que dice **"Automatically install the necessary tools"** o verifica que la opción **"Add to PATH"** esté seleccionada.
4.  **Reinicia tu terminal:** Una vez terminada la instalación, cierra y abre de nuevo la terminal para que reconozca los cambios.

---

## 2. Instalación de Firebase CLI (firebase-tools)

Una vez que npm funciona, instalamos las herramientas de Firebase de manera **global**. Esto permite usar el comando `firebase` desde cualquier carpeta de tu computadora.

### Procedimiento de instalación global
Ejecuta el siguiente comando en tu terminal:
```bash
npm install -g firebase-tools
```
> **Nota para macOS/Linux:** Si recibes un error de permisos, usa `sudo npm install -g firebase-tools`.

### Cómo acceder a Firebase con tu cuenta de Google
Para vincular tu computadora con tu consola de Firebase:
1.  En la terminal, escribe:
    ```bash
    firebase login
    ```
2.  Se abrirá una ventana en tu navegador. Selecciona tu **cuenta de Google** vinculada a Firebase.
3.  Haz clic en **"Permitir"**.
4.  Vuelve a la terminal; deberías ver un mensaje de éxito: *"Success! Logged in as..."*.

---

## 3. Instalar FlutterFlow CLI

El CLI de FlutterFlow sirve principalmente para descargar el código de tus proyectos localmente sin tener que bajar un archivo `.zip` manualmente.

### Procedimiento de instalación
FlutterFlow CLI se instala a través de **Dart** (que viene incluido al instalar Flutter). Ejecuta:
```bash
dart pub global activate flutterflow_cli
```

### Configuración del PATH (Si es necesario)
Si después de instalarlo el comando `flutterflow` no funciona, debes añadir la ruta de los "binarios" de Dart a las variables de entorno de tu sistema:
* **Windows:** `%USERPROFILE%\AppData\Local\Pub\Cache\bin`
* **macOS/Linux:** `$HOME/.pub-cache/bin`

### Cómo utilizar FlutterFlow CLI
Para exportar el código de un proyecto específico:
```bash
flutterflow export-code --project <PROJECT_ID> --dest <FOLDER_PATH> --token <API_TOKEN>
```
* **PROJECT_ID:** Lo encuentras en la URL de tu proyecto en FlutterFlow.
* **API_TOKEN:** Se genera en la configuración de tu cuenta en FlutterFlow (Settings -> API Token).

---

## Resumen de comandos útiles

| Acción | Comando |
| :--- | :--- |
| **Verificar Node/npm** | `node -v` / `npm -v` |
| **Instalar Firebase CLI** | `npm install -g firebase-tools` |
| **Iniciar sesión Firebase** | `firebase login` |
| **Ver mis proyectos Firebase** | `firebase projects:list` |
| **Instalar FF CLI** | `dart pub global activate flutterflow_cli` |

¿Ya tienes instalado el SDK de Flutter en tu máquina o necesitas ayuda para configurar esa parte también?
