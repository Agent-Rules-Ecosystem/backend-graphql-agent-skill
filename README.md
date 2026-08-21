# 📊 Backend GraphQL Agent Skill

> **Skill especializada** — Auditoría e implementación de APIs GraphQL: schema design, resolvers, N+1 y seguridad.
> Requiere `backend-agent-rules` como base.

---

## 📌 Propósito y Alcance

1. 🔍 **Auditar** schemas GraphQL y resolvers en el proyecto.
2. 🛠️ **Detectar** problemas N+1, queries sin límite de profundidad y errores de seguridad.
3. 📐 **Validar** el diseño de schema (types, inputs, paginación Relay).
4. 🔧 **Guiar** la implementación de DataLoader y query cost analysis.
5. 📋 **Reportar** deuda técnica de performance y seguridad en la API GraphQL.

---

## ⚡ $-Comandos

| Comando | Acción |
|---|---|
| `$gql` | Bootstrap |
| `$gql:audit` | Auditoría completa |
| `$gql:n1` | Diagnóstico N+1 |
| `$gql:schema` | Revisión de schema |
| `$gql:fix` | Remediación |

---

## 📦 Instalación

```bash
git submodule add https://github.com/xolotl-hub/backend-graphql-agent-skill.git .skill/backend-graphql-agent-skill
```
