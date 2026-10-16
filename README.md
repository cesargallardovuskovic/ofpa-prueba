# OFPA · Ambiente de prueba

Sistema de Oficina de Partes (PROEXSI). Versión de demostración con datos ficticios en memoria: 5 Oficinas de Partes y unos 700 partes del año.

- Usuarios: `admin`, `mrojas` (jefe de oficina), `sortiz` (operador), `lfuentes` (encargado), `pgonzalez` (jefatura y firmante), `auditor` (consulta) y otros · Clave: `CambiarEsta2026`
- Los datos se reinician cada vez que el servicio se reinicia.
- Se publica en Render como *Web Service* con Docker (plan gratuito).

## Publicar o actualizar en Render

1. Cree un repositorio (GitHub o GitLab) con estos tres archivos: `Dockerfile`, `ofpa-app.tar.gz` y este `README.md`.
2. En Render: **New › Web Service**, conecte el repositorio, *Runtime* **Docker**, plan **Free**. No necesita variables adicionales.
3. Para actualizar, reemplace `ofpa-app.tar.gz` por el de la nueva entrega y haga *commit*: Render vuelve a desplegar solo.
4. El plan gratuito se suspende tras 15 minutos sin uso; el primer ingreso después tarda cerca de un minuto en despertar.

`ofpa-app.tar.gz` es la publicación de `OFPA.Web` compilada en modo demostración (`dotnet publish src/OFPA.Web -c Release -p:Demo=true`).
