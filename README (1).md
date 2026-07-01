# Proyecto Final Capstone — Consumo y visualización de datos desde una API IoT en contenedor

**Materia:** Arquitectura y Sistemas Operativos — UTN FRBB
**Autores:** Luca Farias, Bruno Verna

## Descripción

Este proyecto consume datos en tiempo real desde un endpoint público de un dispositivo IoT
(`https://callback-iot.up.railway.app/data`), los procesa mediante un flujo en **Node-RED**
ejecutado dentro de un contenedor **Docker**, y los visualiza en un dashboard web con widgets
de tipo Gauge y Chart. El flujo consulta el endpoint cada 10 segundos, ordena los registros
por fecha/hora y muestra los dos más recientes.

## Cómo correr el proyecto

1. Tener Docker y Docker Compose instalados (ver guía en `documentacion/informe-tecnico.pdf`,
   sección "Materiales requeridos").
2. Clonar este repositorio y posicionarse en la raíz:
   ```
   git clone <url-del-repo>
   cd <carpeta-del-repo>
   ```
3. Levantar el contenedor:
   ```
   docker-compose up -d
   ```
4. Abrir el editor de Node-RED en el navegador:
   ```
   http://localhost:1880
   ```
5. Importar el flujo (ver instrucciones en el informe técnico) y abrir el dashboard en:
   ```
   http://localhost:1880/ui
   ```

## Informe técnico

El informe completo se encuentra en [`documentacion/informe-tecnico.pdf`](./documentacion/informe-tecnico.pdf),
e incluye: ejemplo del JSON recibido, descripción del flujo, explicaciones técnicas de Docker,
APIs REST, IoT y Node-RED, diagrama de bloques del sistema y reflexión final.

## Video demostrativo

Link público (Google Drive): ver [`video/enlace-video.txt`](./video/enlace-video.txt)

## Autores

- Luca Farias
- Bruno Verna
