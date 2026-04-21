# Notepad-Ahk
Notepad-Ahk (@UX Edition): Optimización técnica de Notepad++ para el desarrollo en AutoHotkey. Incluye flujo de depuración interna, idioma con localización (ES-MX) y homologacion con Protocolo @UX.

<img width="1280" height="1024" alt="imagen" src="https://github.com/user-attachments/assets/ed1e33b8-e0a1-4087-8401-a08cf7d716a4" />

# Notepad-Ahk // Holux Edition (@UX) 🌑⚡

Este repositorio centraliza la configuración avanzada y las herramientas de optimización para convertir **Notepad++** en un entorno de desarrollo (IDE) de alto rendimiento para **AutoHotkey (v1/v2)**, bajo los estándares del **Protocolo @UX**.

## 🚀 Características Brutales

* **Depuración Integrada:** Adiós a las ventanas emergentes. Captura de errores (`ErrorStdOut`) directamente en la consola de NppExec.
* **Salto Inteligente (@UX):** Hipervínculos en consola que te llevan exactamente a la línea del error con un doble clic.
* **Look & Feel Holux:** Interfaz optimizada para el "Lado Oscuro", reduciendo la fatiga visual y maximizando el foco.
* **Localización ES-MX:** Traducción y terminología técnica ajustada para la comunidad de habla hispana.
<img width="1200" height="955" alt="Ahk_Notepad_Holux(Ux)_Compilar_01" src="https://github.com/user-attachments/assets/2c614990-eb51-4e3d-a020-3697059867be" />


## 🛠️ Configuración del Compilador (NppExec)

Para replicar el flujo de trabajo mostrado en este repositorio, utiliza el siguiente codigo con el complemento **NppExec (F6)**:
<img width="400" height="482" alt="Ahk_Notepad_Holux(Ux)_01" src="https://github.com/user-attachments/assets/c029af5d-3019-4ac7-b6b5-03398fa3c1e9" />
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
