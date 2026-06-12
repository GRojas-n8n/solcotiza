# project-starter

Plantilla base para proyectos con **Spec-Driven Development (SDD)** + **Claude Code**.

## Uso

```bash
# Crear repo desde esta plantilla en GitHub
# Clonar
git clone https://github.com/tu-usuario/nuevo-proyecto.git
cd nuevo-proyecto

# Copiar specs (generados por Telesforo)
cp /ruta/a/specs/*.md ./specs/

# Abrir VS Code + Claude Code
code .
claude

# Implementar
# > Implementa specs 01, 02 y 03. No preguntes. Decide orden. Reporta al final.
```

## Estructura

```
├── .github/workflows/   ← CI + review + deploy
├── .claude/             ← Settings optimizados
├── specs/               ← Especificaciones SDD
├── src/                 ← Código fuente
├── tests/               ← Tests
├── docs/                ← Documentación
├── CLAUDE.md            ← Reglas del proyecto
└── README.md
```

## Flujo completo

Ver manual en `[[manual-ecosistema-sdd-claude]]`.