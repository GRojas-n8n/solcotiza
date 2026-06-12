# CLAUDE.md — [Nombre del Proyecto]

## Stack
- Backend: Node.js + Express
- Frontend: React + Vite
- Base de datos: PostgreSQL con Prisma
- Tests: Jest
- CI: GitHub Actions

## Estructura del proyecto
- src/ → código fuente
- tests/ → tests unitarios
- specs/ → especificaciones SDD
- docs/ → documentación

## Reglas SDD
- No escribir código sin spec aprobado en /specs/
- Test-first: escribir tests ANTES que el código
- No refactorizar código existente sin preguntar
- Commits con conventional commits

## Convenciones
- Nombres de funciones: camelCase
- Nombres de tablas: snake_case
- Errores en español para el usuario
- Código en inglés

## Ramas
- Cada lote de specs va en su propia rama: feat/specs-XX-YY
- Nunca escribir directo a main
- Al terminar, abrir PR contra main con resumen de cambios
