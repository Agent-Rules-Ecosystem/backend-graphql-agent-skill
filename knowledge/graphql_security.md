# Seguridad en GraphQL

## Vectores de Ataque Comunes

| Vector | Mitigación |
|---|---|
| Queries profundas (DoS) | Limitar profundidad máxima (7 niveles recomendado) |
| Queries costosas (DoS) | Query cost analysis / complexity limits |
| Introspección en producción | Deshabilitar en `NODE_ENV=production` |
| CSRF en mutations | Tokens CSRF o verificación de `Origin` header |
| Batch attacks | Rate limiting por query / por usuario |

## Autenticación Canónica

La autenticación debe resolverse UNA SOLA VEZ en la función `context`:

```
// Patrón correcto:
// context: async ({ req }) => {
//   const user = await verifyToken(req.headers.authorization)
//   return { user }
// }
//
// Resolver solo accede: resolver(parent, args, { user }) => {
//   if (!user) throw new AuthenticationError()
// }
```
