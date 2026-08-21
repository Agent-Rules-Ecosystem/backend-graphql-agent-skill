# Patrones Canónicos de GraphQL

## DataLoader — Solución al Problema N+1

El problema N+1 ocurre cuando un resolver ejecuta N consultas para obtener datos de N objetos padre.

**Patrón de detección**: Resolver dentro de un tipo que hace una consulta a DB por cada item del padre.
**Solución**: DataLoader agrupa todas las llamadas del mismo tick en una sola consulta por batch.

## Diseño de Schema

| Práctica | Descripción |
|---|---|
| Tipos de error explícitos | Union types: `Result = Success \| Error` |
| Paginación por cursor | `connection { edges { node cursor } pageInfo }` (Relay spec) |
| Inputs tipados | `input CreateUserInput { name: String! email: String! }` |
| Nullability consciente | Campos obligatorios como `String!`, opcionales como `String` |

## Antipatrones a Detectar

| Antipatrón | Severidad |
|---|---|
| Query sin profundidad máxima | Alta (DoS) |
| Resolver con lógica de negocio | Media |
| N+1 sin DataLoader | Alta (performance) |
| Errores genéricos `throw new Error()` | Media |
| Introspección habilitada en producción | Media |
