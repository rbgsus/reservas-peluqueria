# Reservas de peluquería

Aplicación web para reservar citas en una peluquería, hecha con microservicios.
La documentación completa y el backlog de tareas están en la carpeta `docs/`.

## Estructura

| Carpeta | Qué es | Puerto |
| --- | --- | --- |
| `config-server` | Configuración central | 8888 |
| `eureka-server` | Registro de servicios | 8761 |
| `gateway` | Entrada única, valida el token | 8080 |
| `ms-clientes` | Perfiles de cliente | 8081 |
| `ms-citas` | Reservas y estados | 8082 |
| `ms-servicios` | Catálogo y precios | 8083 |
| `ms-empleados` | Empleados, horario y cierres | 8084 |
| `ms-historial` | Historial y reseñas (MongoDB) | 8085 |
| `ms-auth` | Login y tokens | 8086 |
| `ms-notificaciones` | Emails | 8087 |
| `frontend` | Angular | 4200 |
| `k8s` | Manifiestos de Kubernetes | |

## Cómo arrancarlo

Pendiente: se completa en la tarea T1.4 (Docker Compose de desarrollo).

## Cómo se trabaja

- `main` es producción y `develop` es pre. No se escribe directamente en ninguna de las dos.
- Cada tarea del backlog tiene su rama: `feature/T1.1-repositorio-y-ramas`.
- La rama se integra en `develop` con una pull request. Antes de integrar hay que marcar la lista de «tarea terminada» de la plantilla.
- Pasar de `develop` a `main` despliega en producción, con aprobación manual.
