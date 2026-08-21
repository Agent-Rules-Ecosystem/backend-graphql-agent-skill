---
name: backend-graphql-agent-skill
description: Auditoría e implementación de APIs GraphQL: schema design, resolvers, N+1, autenticación y performance.
---

# Backend Graphql Skill Matrix

## Capacidades

```mermaid
graph LR
    A[GQL] --> B[Auditoría de Dominio]
    A --> C[Patrones Canónicos]
    A --> D[Detección de Antipatrones]
    A --> E[Remediación Guiada]
```

## Protocolo de Auditoría (`$gql:audit`)

1. Detectar archivos del dominio en el proyecto
2. Evaluar cumplimiento de patrones canónicos
3. Identificar antipatrones y deuda técnica
4. Reporte por severidad (Alta / Media / Baja)
5. Remediación con `$gql:fix`
