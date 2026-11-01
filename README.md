# conectae-duco-config
Repositorio oficial para la automatización de reglas de red y monitoreo SIP del proyecto **Conecta-EduCo**.

## 🎯 Propósito del Proyecto
El propósito principal de este software es automatizar la sincronización de parámetros de configuración y reglas de enrutamiento con la API de **Wolkvox**, garantizando una integración segura, estable y en tiempo real para la gestión de agentes y flujos de comunicación. Asimismo, centraliza el control de versiones de la infraestructura de configuración bajo estándares de calidad académica (ISO/IEC 25010).

## 🛠️ Tecnologías y Requisitos
* **Python 3.10+**
* **Git** para control de versiones
* Librerías de dependencias especificadas en `requirements.txt` (`requests`, `python-dotenv`)

## 📦 Estructura del Repositorio
* `sync_wolkvox.py`: Script principal de automatización y sincronización con la API.
* `requirements.txt`: Archivo de dependencias del entorno.
* `.env.example`: Plantilla de variables de entorno requeridas para la autenticación.
* `.gitignore`: Archivo para excluir datos sensibles del control de versiones.

## 🚀 Despliegue e Instalación Rápida

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/dgosanchez20-code/conectae-duco-config.git](https://github.com/dgosanchez20-code/conectae-duco-config.git)
   cd conectae-duco-config


Instalar dependencias:
-----------------------------------
Bash
pip install -r requirements.txt
-----------------------------------

Configurar las variables de entorno:
Crea un archivo .env basado en la plantilla y añade tus credenciales de la API de Wolkvox.

Ejecutar prueba de funcionamiento:
----------------------------------
Bash
python sync_wolkvox.py --test-run
----------------------------------
Resultado esperado: Respuesta de conexión exitosa con código HTTP 200 OK.

🔄 Plan de Reversión (Rollback)
En caso de fallos en el despliegue de una actualización:

- Consultar el historial de versiones con git log --oneline.

- Revertir los archivos afectados con git checkout <tag_estable> -- config/.

- Ejecutar la restauración mediante python sync_wolkvox.py --rollback.

👥 Autores
Diego Alejandro Sánchez
Santiago Santa López



