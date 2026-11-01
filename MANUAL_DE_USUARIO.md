# Manual de Usuario - Conecta-EduCo Config

## 1. Introducción y Propósito
El presente manual tiene como objetivo guiar al operador o administrador del sistema en el uso correcto, ejecución y supervisión del software de sincronización **Conecta-EduCo Config**. Este sistema permite automatizar las reglas de enrutamiento y la conectividad con la API de Wolkvox de forma segura.

## 2. Requisitos Previos de Operación
Antes de ejecutar el sistema, el usuario debe asegurarse de contar con:
* Acceso a una terminal de comandos (PowerShell, CMD o Git Bash).
* Python instalado en el equipo.
* Credenciales de acceso y permisos vigentes proporcionados por el administrador de la API de Wolkvox.

## 3. Guía de Puesta en Marcha (Paso a Paso)

### Paso 1: Configuración de Credenciales
1. Ubique el archivo de plantilla de variables de entorno `.env.example` en el directorio del proyecto.
2. Cree una copia de este archivo y renómbrelo simplemente como **`.env`**.
3. Abra el archivo `.env` con un editor de texto (como Visual Studio Code) e introduzca los datos de acceso a la API correspondientes:
   ```env
   WOLKVOX_API_KEY=tu_clave_de_api_aqui
   WOLKVOX_ENDPOINT=[https://api.wolkvox.com/v2/](https://api.wolkvox.com/v2/)

Paso 2: Ejecución del Modo de Prueba
Para verificar que la conexión con el servidor y la autenticación son correctas sin alterar los registros en producción, ejecute el script en modo de prueba:
----------------------------------
PowerShell
python sync_wolkvox.py --test-run
----------------------------------
Resultado esperado en pantalla: El sistema mostrará un mensaje de inicialización seguido de la respuesta del servidor indicando HTTP 200 OK - Modo de prueba finalizado con éxito.

Paso 3: Ejecución de Sincronización en Producción
Una vez validada la conexión de prueba, ejecute el script principal para realizar la sincronización regular de las configuraciones de red y reglas de enrutamiento:
-----------------------------------
PowerShell
python sync_wolkvox.py
-----------------------------------

4. Resolución de Problemas Comunes (Troubleshooting)

## 4. Resolución de Problemas Comunes (Troubleshooting)

| Síntoma o Error | Causa Probable | Solución Recomendada |
| :--- | :--- | :--- |
| `HTTP 401 Unauthorized` | Credenciales incorrectas o caducadas en el archivo `.env`. | Verifique que su `WOLKVOX_API_KEY` esté escrita correctamente y sin espacios adicionales. |
| `No se encontró el archivo .env` | El archivo de configuración de entorno no fue creado o renombrado. | Asegúrese de crear el archivo `.env` en la raíz del proyecto basándose en el ejemplo. |
| `Error: Python no se reconoce...` | Python no está agregado al PATH del sistema operativo. | Reinstale Python seleccionando la opción de añadir al PATH o utilice el comando `py` alternativo. |

5. Soporte y Contacto
Para dudas adicionales sobre la operación de la herramienta, contacte al equipo de desarrollo del proyecto Conecta-EduCo a través del repositorio oficial en GitHub.
