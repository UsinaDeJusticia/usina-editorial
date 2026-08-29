# Usina Editorial

Skill editorial compartida para **Usina de Justicia**.

Convierte material bruto —textos, PDFs, enlaces, entrevistas, imágenes, datos o combinaciones de esos insumos— en contenido editorial enriquecido, verificado y listo para cargar en WordPress.

La skill **no publica en WordPress**, no modifica el sitio web y no realiza commits sobre `UsinaDeJusticia/usina-de-justicia`. Su trabajo termina al entregar el paquete editorial listo para que una persona lo cargue en `wp.usinadejusticia.org.ar/wp-admin/`.

## Fuente de verdad

Este repositorio es la **fuente de verdad** de `usina-editorial`.

No deben mantenerse versiones editoriales distintas para ChatGPT, Claude Code, Codex, OpenCode o Hermes. Cuando cambie una regla de la skill, se actualiza primero este repositorio y luego se refresca la instalación de cada harness.

## Qué contiene

```text
usina-editorial/
├── README.md
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── content-types.md
    ├── examples.md
    ├── output-contract.md
    ├── research-and-sourcing.md
    └── site-contract.md
```

- `SKILL.md`: flujo principal y reglas editoriales no negociables.
- `references/content-types.md`: patrones adaptativos según el tipo de publicación.
- `references/research-and-sourcing.md`: investigación, verificación, jerarquía de fuentes, privacidad y tratamiento del framing periodístico.
- `references/output-contract.md`: formato de salida listo para WordPress.
- `references/site-contract.md`: límites entre la skill, WordPress y el frontend de Usina.
- `references/examples.md`: ejemplos de comportamiento; no son plantillas rígidas.
- `agents/openai.yaml`: metadatos de presentación para harnesses de OpenAI.

---

# Instalación según el harness

## 1. ChatGPT

ChatGPT no sigue automáticamente los cambios de un repositorio Git. La instalación se hace cargando un paquete de skill.

### Crear `skill.zip`

Clonar el repositorio:

```bash
git clone https://github.com/UsinaDeJusticia/usina-editorial.git
cd usina-editorial
```

En macOS o Linux:

```bash
zip -r ../skill.zip SKILL.md agents references
```

En Windows PowerShell:

```powershell
Compress-Archive -Path SKILL.md,agents,references -DestinationPath ..\skill.zip -Force
```

Se excluye `README.md` deliberadamente: es documentación para humanos y no forma parte del conocimiento operativo que la skill necesita cargar.

### Cargarla en ChatGPT

1. Abrir **Habilidades**.
2. Elegir **Crear**.
3. Elegir **Cargar desde tu computadora**.
4. Seleccionar `skill.zip`.
5. Instalar la skill.

También puede crearse o modificarse desde una conversación usando el editor de Skills de ChatGPT.

**Importante:** cuando este repositorio cambie, la instalación existente en ChatGPT no se actualiza sola. Hay que regenerar `skill.zip` y actualizar/reinstalar la skill.

Documentación oficial: https://help.openai.com/es-419/articles/20001066-skills-en-chatgpt

---

## 2. Codex

Codex descubre skills instaladas bajo `$CODEX_HOME/skills`. Si `CODEX_HOME` no está definido, la ubicación predeterminada es `~/.codex/skills`.

### Instalación global — macOS/Linux

```bash
git clone https://github.com/UsinaDeJusticia/usina-editorial.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/usina-editorial"
```

### Instalación global — Windows PowerShell

```powershell
$CodexHome = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { "$HOME\.codex" }
git clone https://github.com/UsinaDeJusticia/usina-editorial.git "$CodexHome\skills\usina-editorial"
```

Después de una instalación nueva, reiniciar Codex para asegurar que la skill entre en el índice de la sesión.

Codex también incluye `$skill-installer`, que puede instalar skills desde repositorios/rutas de GitHub. La clonación directa anterior es útil cuando se quiere mantener esta copia enlazada a Git y actualizarla mediante `git pull`.

Documentación/referencia oficial: https://github.com/openai/skills

---

## 3. Claude Code

Claude Code reconoce skills personales y skills específicas de un proyecto.

### Instalación personal/global

Disponible en todos los proyectos del usuario:

```bash
git clone https://github.com/UsinaDeJusticia/usina-editorial.git \
  ~/.claude/skills/usina-editorial
```

En Windows PowerShell:

```powershell
git clone https://github.com/UsinaDeJusticia/usina-editorial.git "$HOME\.claude\skills\usina-editorial"
```

### Instalación sólo para un proyecto

Desde la raíz del proyecto:

```bash
git clone https://github.com/UsinaDeJusticia/usina-editorial.git \
  .claude/skills/usina-editorial
```

Claude Code detecta `SKILL.md` y puede invocar la skill automáticamente cuando la tarea coincide con su descripción, o explícitamente como `/usina-editorial` cuando corresponda.

Claude Code observa cambios en los directorios de skills existentes. Si el directorio superior de skills no existía cuando comenzó la sesión, puede ser necesario reiniciar Claude Code una vez.

Documentación oficial: https://code.claude.com/docs/es/skills

---

## 4. OpenCode

OpenCode soporta nativamente Agent Skills y además es compatible con las rutas de Claude Code y `.agents/skills`.

### Opción recomendada si también se usa Claude Code

Instalar una sola copia en:

```bash
~/.claude/skills/usina-editorial
```

Es decir:

```bash
git clone https://github.com/UsinaDeJusticia/usina-editorial.git \
  ~/.claude/skills/usina-editorial
```

Tanto Claude Code como OpenCode pueden descubrir esa instalación.

### Instalación exclusiva para OpenCode — global

```bash
git clone https://github.com/UsinaDeJusticia/usina-editorial.git \
  ~/.config/opencode/skills/usina-editorial
```

### Instalación exclusiva para un proyecto OpenCode

Desde la raíz del proyecto:

```bash
git clone https://github.com/UsinaDeJusticia/usina-editorial.git \
  .opencode/skills/usina-editorial
```

OpenCode también descubre skills en:

```text
~/.claude/skills/
~/.agents/skills/
.claude/skills/
.agents/skills/
```

Por eso no hace falta mantener una copia diferente de la skill sólo para OpenCode.

Documentación oficial: https://opencode.ai/docs/skills

---

## 5. Hermes

Hermes puede usar la skill de dos formas.

### Opción A — instalación nativa de Hermes

```bash
git clone https://github.com/UsinaDeJusticia/usina-editorial.git \
  ~/.hermes/skills/usina-editorial
```

La skill quedará disponible en el índice de skills de Hermes y podrá invocarse como `/usina-editorial`.

### Opción B — repositorio compartido mediante `external_dirs`

Esta opción es preferible cuando se quiere que Hermes consuma skills mantenidas fuera de `~/.hermes/skills`.

Por ejemplo:

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/UsinaDeJusticia/usina-editorial.git \
  ~/.agents/skills/usina-editorial
```

Luego editar `~/.hermes/config.yaml`:

```yaml
skills:
  external_dirs:
    - ~/.agents/skills
```

Hermes escaneará ese directorio además de su directorio local de skills.

Esta variante combina especialmente bien con OpenCode, que también reconoce `~/.agents/skills`.

Si se desea que GitHub sea estrictamente la única fuente editable, mantener el checkout compartido bajo control de Git y evitar modificaciones manuales divergentes.

Documentación oficial: https://github.com/hermes-agent-org/hermes/blob/main/website/docs/guides/work-with-skills.md

---

# Actualizar una instalación existente

Si la skill fue instalada mediante `git clone`, actualizarla es simplemente hacer `git pull` en el directorio correspondiente.

Ejemplo para Claude Code:

```bash
git -C ~/.claude/skills/usina-editorial pull --ff-only
```

Ejemplo para Codex:

```bash
git -C "${CODEX_HOME:-$HOME/.codex}/skills/usina-editorial" pull --ff-only
```

Ejemplo para Hermes:

```bash
git -C ~/.hermes/skills/usina-editorial pull --ff-only
```

Para **ChatGPT**, volver a generar `skill.zip` y actualizar/reinstalar la skill desde Habilidades.

---

# Instalación compartida avanzada

Si varios harnesses se ejecutan en la misma máquina y se quiere mantener **un único checkout físico**, una estrategia posible es clonar el repositorio en una ubicación neutral y enlazarlo desde los directorios que cada harness descubre.

Ejemplo conceptual:

```text
~/agent-skills/usina-editorial        ← único repositorio Git

~/.claude/skills/usina-editorial      → enlace al repositorio
~/.codex/skills/usina-editorial       → enlace al repositorio
```

OpenCode puede además apuntar directamente a rutas adicionales o utilizar sus ubicaciones compatibles; Hermes puede registrar el directorio padre mediante `skills.external_dirs`.

Los enlaces simbólicos dependen del sistema operativo y de sus permisos. Si se busca la configuración más simple y robusta, usar una clonación por harness y mantenerlas sincronizadas con `git pull`.

---

# Regla de mantenimiento

1. Modificar primero `UsinaDeJusticia/usina-editorial`.
2. Revisar y versionar el cambio en Git.
3. Actualizar las instalaciones locales con `git pull`.
4. Regenerar `skill.zip` únicamente para ChatGPT.

No copiar las reglas editoriales a archivos paralelos como `CLAUDE.md`, `AGENTS.md`, memorias o prompts permanentes. Esos mecanismos pueden recordar **que la skill existe**, pero la lógica editorial debe seguir viviendo aquí.