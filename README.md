# Notepad-Ahk
Notepad-Ahk (@Holux Version):     

Editor con interfaz de panel dual (ventana dividida) y optimización para compilacion de codigo (AutoHotkey/AHK). 
Incluye flujo de depuración interna, idioma con localización (ES-MX) y homologacion con Protocolo @UX.

<img width="1280" height="1024" alt="imagen" src="https://github.com/user-attachments/assets/ed1e33b8-e0a1-4087-8401-a08cf7d716a4" />

# Notepad-Ahk // Holux Version (@UX) 🌑⚡

Este repositorio centraliza la configuración avanzada y las herramientas de optimización para convertir el editor (**Notepad++**) en una "mini" interfaz de desarrollo con entorno integrado (IDE).     
El enfoque de escalabilidad bajo el **Protocolo @UX**, en una aplicacion "amigable" y conocida, permite mejorar el rendimiento general de proyectos. 

El beneficio directo, es un gran ahorro en tiempo de depuracion y una mejor experiencia al compilar codigo (**AutoHotkey/AHK (v1/v2)**) o rutinas especificas. 

## 🚀 Características Brutales

* **Depuración integrada(AHK):** La depuracion muestra los errores (`ErrorStdOut`) directamente en el panel de consola (NppExec), justo al lado de la ventana de resultados, sin ventanas emergentes.
* **Deteccion relacional (@UX):** La deteccion de los errores es estilo relacional con "ligas" (hipervínculos) de texto seleccionables (doble clic/toque) en la consola, para ir al error especifico. 
* **Interaccion (HOLUX):** La interaccion en la interfaz es optimizada con el "tema oscuro" nativo, reduciendo la fatiga visual y en favor de una experiencia mas fluida.
* **Localización (ES-MX):** La localizacion tiene soporte de traducción y compatibilidad técnica en Español internacional (ES-MX/UTF8/UX).
<img width="1200" height="955" alt="Ahk_Notepad_Holux(Ux)_Compilar_01" src="https://github.com/user-attachments/assets/2c614990-eb51-4e3d-a020-3697059867be" />


## 🛠️ Configuración del Compilador (NppExec)

La configuracion usa el siguiente codigo en el complemento (**NppExec (F6)**) para replicar el flujo de trabajo mostrado en este repositorio:
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
