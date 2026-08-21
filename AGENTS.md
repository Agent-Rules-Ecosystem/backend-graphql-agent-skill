---
name: backend-graphql-agent-skill
description: Auditoría e implementación de APIs GraphQL: schema design, resolvers, N+1, autenticación y performance.
---

# Backend Graphql Skill Directive

## Bootstrap de la Habilidad

Al detectar triggers de GraphQL (`$gql`, `graphql audit`, `schema review`, `resolver patterns`):

1. `.skill/backend-graphql-agent-skill/SKILL.md` ← Directiva principal
2. `.skill/backend-graphql-agent-skill/core/commands.md` ← $-Comandos
3. `.skill/backend-graphql-agent-skill/core/brain.md` ← Motor de decisiones

## Reglas Canónicas de GraphQL

- **DataLoader obligatorio**: Todo resolver que acceda a base de datos en una lista debe usar DataLoader para prevenir el problema N+1.
- **Profundidad máxima de queries**: Limitar la profundidad máxima de queries (recomendado: 7 niveles) para prevenir DoS.
- **Autenticación en context**: La verificación de tokens debe ocurrir en la función `context`, nunca dentro de resolvers individuales.
- **Sin lógica de negocio en resolvers**: Los resolvers solo orquestan; la lógica de negocio vive en servicios/repositorios.
- **Errores tipados**: Usar tipos de error explícitos en el schema (union types) en lugar de lanzar errores genéricos.
