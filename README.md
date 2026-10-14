# ZVELOZ Status Monitor

Monitor externo de uptime para los servicios públicos de ZVELOZ.
Corre cada 5 minutos vía GitHub Actions.

## Endpoints monitoreados

| Servicio | URL |
|----------|-----|
| Website | https://zveloz.com/ |
| Backend/API | https://api.zveloz.com/api/app/settings |

## Qué hace al detectar caída

1. Abre un issue en este repo con label `outage` (mención a @Edgar881220)
2. Envía email de alerta a `infra.zveloz@gmail.com` vía SMTP propio
3. Al recuperarse, comenta y cierra el issue automáticamente

## Configuración

Secrets requeridos en este repo: `MAIL_HOST`, `MAIL_PORT`,
`MAIL_USERNAME`, `MAIL_PASSWORD`, `MAIL_FROM`, `ALERT_EMAIL`.

Mejora futura pendiente: alerta por WhatsApp (CallMeBot API, gratis)
cuando se defina el número destino.
