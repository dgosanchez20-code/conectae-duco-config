# Bitácora de Cambios (CHANGELOG) - Conecta-EduCo Config

Todas las modificaciones notables de este proyecto serán registradas en este archivo.  
El formato está basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.0.0/) y este proyecto adhiere al versionado semántico [SemVer](https://semver.org/lang/es/).

---

## [1.0.0] - 2026-05-31 (Versión Inicial / Release Final)

### Añadido
* **Script de Sincronización:** Creación del archivo principal `sync_wolkvox.py` para la automatización de reglas de enrutamiento y control con la API de Wolkvox.
* **Control de Entorno:** Integración de la librería `python-dotenv` para la gestión segura de credenciales mediante el archivo `.env`.
* **Automatización y Pruebas:** Implementación del parámetro `--test-run` para verificar la conectividad con el servidor y validar respuestas con código `HTTP 200 OK`.
* **Documentación del Repositorio:** 
  * Redacción del archivo `README.md` con propósitos, tecnologías, instrucciones de instalación y plan de reversión (*rollback*).
  * Creación del archivo de dependencias `requirements.txt`.
  * Configuración de exclusiones seguras mediante `.gitignore` para proteger datos sensibles.

### Seguridad
* Eliminación de credenciales en texto plano del código fuente, migrándolas completamente a variables de entorno protegidas.
