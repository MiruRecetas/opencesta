# MiruRecetas · Sincronización documental previa a la reorganización

**Versión 1.0 · 21/10/2026.** Encargo actual: alinear Markdown de GitHub con las 18 fuentes ya verificadas del proyecto. No ejecutar privatización, migración ni cambios funcionales.

## AS IS

Fork público de ruvelro/opencesta, separado del desarrollo propio. El motor económico consume releases de upstream, no presupone releases de este fork.

Rama base auditada: `main`, SHA `f3e571f639d4897681c8bbbfac3cb5665f941409`. La línea base de los nueve repositorios no había cambiado respecto a la auditoría del 21/10. Los SHA deben comprobarse de nuevo antes de una intervención posterior.

## Fuentes y precedencia

Las decisiones explícitas vigentes de la usuaria delimitan la operación autorizada. El código, contratos y datos reales determinan qué está implementado. Los informes históricos no se reescriben ni invalidan una decisión posterior. La arquitectura futura no se presenta como desplegada.

El [espejo completo de fuentes](https://github.com/MiruRecetas/motor-precios/blob/main/docs/fuentes-proyecto/README.md) permanece en motor-precios, privado; requiere acceso al repositorio. El documento de entrada es Índice, gobierno y manifiesto v2.0. Se consultan además el protocolo de su rol, AS IS, Actions, economía y TO BE según corresponda. El ZIP de marca sigue en el proyecto y los recursos publicados se preservan.

## Triggers y puerta de integración

ci.yml: push a main y pull_request; ejecuta ruff/pytest en core, sin pasos de publicación. snapshot.yml y enrich.yml: únicamente schedule/workflow_dispatch; no se disparan por push/PR. snapshot sí puede publicar releases, Pages y abrir issues si se ejecutase. Su estado administrativo no ha sido certificable con el conector; cero runs observados no demuestra desactivación. No habilitar, despachar ni modificar esos workflows. has_pages=false en el corte.

Solo Markdown en el diff. Antes de fusionar: comprobar main vivo, lista real de cambios, eventos y scripts transitivos; CI aplicable, permisos y ausencia de publicación. Si cambia la base o un workflow, repetir la revisión. No modificar triggers, secretos o protecciones ni desactivar controles para hacer pasar una PR.

## TO BE

Fuentes y desarrollo privados → construcción y validación privadas → publicación controlada de artefactos mínimos → web/PWA públicas. Conservar URL de producto, fotos, marca, datos, raciones, temporizador, nutrición, costes, Bring!, menús, instalación/offline y reversión. Extraer el generador sin adaptar QA, rutas de fuentes y fixtures históricos rompería dependencias.

## PENDIENTE

La migración requiere encargo separado, revisión de permisos/configuración, tratamiento de URL técnicas ya públicas e historial, licencias, publicación con control de concurrencia y reversión. Las pruebas físicas solo son válidas en el alcance expresamente comunicado. No inferir privacidad del HTML/CSS/JS enviado al navegador.

## Historial

21/10/2026: reconciliación de textos, enlaces al espejo privado y revisión de triggers. Los informes y datos históricos se conservan. El estado de fusión/CI de esta sincronización se registra en la PR y en el acta final, no se presupone por este archivo.
