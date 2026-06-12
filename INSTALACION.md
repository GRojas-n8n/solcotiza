# Guía de instalación — Ecosistema SDD

## 1. Subir plantilla a GitHub

```bash
# Desde tu PC (donde tengas gh autenticado)
cd /ruta/donde/quieres/el/repo

# Descargar la plantilla desde el VPS
scp -r root@5.78.159.252:/opt/segundo-cerebro/proyectos/project-starter/* .
scp -r root@5.78.159.252:/opt/segundo-cerebro/proyectos/project-starter/.* .

# O desde Telegram: pídele a Telesforo el zip

# Crear repo en GitHub
gh repo create project-starter --public --source=. --push
```

## 2. Crear proyecto nuevo desde la plantilla

```bash
gh repo create nuevo-proyecto --template tu-usuario/project-starter --public
git clone https://github.com/tu-usuario/nuevo-proyecto.git
cd nuevo-proyecto
```

## 3. Agregar las 7 skills ECC a Claude Code

No son archivos — son skills que Claude Code ya conoce. Cuando le digas:

```
Implementa specs 01, 02 y 03. No preguntes. Decide orden. Reporta al final.
```

Claude Code activa automáticamente:
- tdd-workflow (tests antes que código)
- verification-loop (verifica contra el spec)
- security-review (revisa seguridad)
- api-design (APIs REST consistentes)
- backend-patterns (arquitectura limpia)
- coding-standards (convenciones)
- strategic-compact (sabe cuándo compactar)

Solo asegúrate de tener un CLAUDE.md en la raíz del proyecto con las reglas SDD.

## 4. Probar el pipeline

```bash
# Abres proyecto
code .
# Terminal integrada
claude
# Pegas:
# > Implementa specs 01, 02 y 03. No preguntes. Decide orden. Reporta al final.
```

## 5. Para desarrollo nocturno (opcional)

Crear `run-specs.bat` en la raíz del proyecto:

```bat
@echo off
cd /d %~dp0
echo Implementa specs 01, 02 y 03. No preguntes. Decide orden. Reporta al final. | claude -p
```

Programar en Task Scheduler o ejecutar manual antes de dormir.