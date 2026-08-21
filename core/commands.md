# $-Comandos de GraphQL

| Comando | Acción | Descripción |
|---|---|---|
| `$gql` | Bootstrap | Inicializa la skill y carga contexto del dominio. |
| `$gql:audit` | Auditoría | Escanea el proyecto y genera reporte de hallazgos. |
| `$gql:fix` | Remediación | Aplica mejoras del último `$gql:audit`. |
| `$gql:fix [ruta]` | Puntual | Aplica fix a un archivo o directorio específico. |
| `$gql:n1` | Diagnóstico N+1 | Detecta resolvers con problema N+1 sin DataLoader. |
| `$gql:schema` | Revisión de Schema | Analiza el schema GraphQL y sugiere mejoras de diseño. |
