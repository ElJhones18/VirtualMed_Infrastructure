# Infraestructura (Docker Compose)

Esta carpeta `Infrastructure` debe estar al mismo nivel que `ai-service`, `frontend` y `backend`.

## Estructura esperada

```text
VirtualMed/
├─ Infrastructure/
│  ├─ docker-compose.yml
│  └─ nginx/
├─ ai-service/
├─ frontend/
└─ backend/
```

## Requisito clave

`docker-compose.yml` usa rutas relativas para encontrar los `Dockerfile` de `ai-service`, `frontend` y `backend`.
Si `Infrastructure` no está en ese nivel, Docker Compose no podrá construir las imágenes.

## Uso

Desde la carpeta `Infrastructure`, ejecutar:

```bash
docker compose up --build -d
```

Para detener los servicios:

```bash
docker compose down
```

