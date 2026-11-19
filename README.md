# ¿Por qué un control de versiones con GitHub no sustituye un respaldo Docker?

Un **control de versiones con GitHub no sustituye un respaldo Docker** porque ambos cumplen funciones diferentes: **GitHub permite gestionar y recuperar versiones del código fuente, mientras que un respaldo Docker permite recuperar una imagen del entorno de ejecución de una aplicación.**

## 1. Diferencias entre GitHub y un respaldo Docker

| Característica | GitHub (Git) | Respaldo Docker |
|---|---|---|
| Código fuente | Sí | Puede incluirlo |
| Historial de cambios | Sí | No de forma equivalente a Git |
| Dependencias instaladas | Generalmente solo declaradas | Sí, si están incluidas en la imagen |
| Sistema operativo base | No | Incluye las capas del sistema base |
| Configuración del servidor | Solo si está registrada en el repositorio | Incluye configuración incorporada en la imagen |
| Servidor web Nginx | Puede guardar su configuración | Puede incluir Nginx instalado y configurado |
| Restauración del entorno | Requiere reconstruirlo | Permite cargar la imagen directamente |
| Datos persistentes | No automáticamente | No se incluyen en `docker save`; requieren respaldo independiente |
