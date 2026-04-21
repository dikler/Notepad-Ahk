# Notepad-Ahk
Notepad-Ahk (@UX Edition): Optimización técnica de Notepad++ para el desarrollo en AutoHotkey. Incluye flujo de depuración interna, idioma con localización (ES-MX) y homologacion con Protocolo @UX.


# Notepad-Ahk // Holux Edition (@UX) 🌑⚡

Este repositorio centraliza la configuración avanzada y las herramientas de optimización para convertir **Notepad++** en un entorno de desarrollo (IDE) de alto rendimiento para **AutoHotkey (v1/v2)**, bajo los estándares del **Protocolo @UX**.

## 🚀 Características Brutales

* **Depuración Integrada:** Adiós a las ventanas emergentes. Captura de errores (`ErrorStdOut`) directamente en la consola de NppExec.
* **Salto Inteligente (@UX):** Hipervínculos en consola que te llevan exactamente a la línea del error con un doble clic.
* **Look & Feel Holux:** Interfaz optimizada para el "Lado Oscuro", reduciendo la fatiga visual y maximizando el foco.
* **Localización ES-MX:** Traducción y terminología técnica ajustada para la comunidad de habla hispana.

## 🛠️ Configuración del Compilador (NppExec)

Para replicar el flujo de trabajo mostrado en este repositorio, utiliza el siguiente script en el plugin **NppExec (F6)**:

```cmd
npp_save
npp_console 0
echo ========================================
echo Ejecutando compilación Holux (@UX)...
echo ----------------------------------------
SET AHK_PATH = C:\Cache\Autohotkey\AutoHotkey.exe
"$(AHK_PATH)" /ErrorStdOut "$(FULL_CURRENT_PATH)"
if $(EXITCODE) != 0 goto Error
echo [OK] Proceso finalizado con éxito.
goto End
:Error
echo .
echo [!] ERROR DETECTADO: Revisar línea indicada.
:End
echo ========================================
npp_console 1
