# Taller Anfibia · Cómo entrenar a tu IA

> Skills personalizadas de Claude Code para el taller dictado por Thiago Donato en Anfibia Escuela.

Once skills que te ayudan a construir cosas con Claude Code: un sitio personal, un dashboard, una pieza editorial, un mini-juego, una herramienta de trabajo, lo que necesites. Cada skill te guía paso a paso, te hace las preguntas correctas y te empuja a tomar decisiones autorales.

---

## Cómo instalar

### Paso 1 · Cloná este repo

Abrí una terminal y ejecutá:

```bash
git clone https://github.com/[TU-USUARIO]/taller-anfibia.git
cd taller-anfibia
```

### Paso 2 · Copiá las skills a tu carpeta de Claude Code

En Mac o Linux:

```bash
mkdir -p ~/.claude/skills
cp -r skills/* ~/.claude/skills/
```

En Windows (PowerShell):

```powershell
mkdir $HOME\.claude\skills -Force
Copy-Item -Path .\skills\* -Destination $HOME\.claude\skills -Recurse
```

### Paso 3 · Verificá que funcionen

Abrí Claude Code en cualquier carpeta y escribí `/`. Deberías ver las skills listadas. Si están, todo bien.

---

## El catálogo

### Antes de empezar

**`/claude-md-global`**
Asistente para escribir tu CLAUDE.md global. Define quién sos y cómo querés que Claude trabaje con vos en cualquier proyecto.
*Se hace una sola vez (con refinamientos posteriores).*

### Para encontrar tu idea (si no la tenés)

**`/explorador`**
Conversá con esta skill si no tenés claro qué construir. Te hace preguntas hasta encontrar tu proyecto.

### Para construir tu proyecto

**`/herramienta-de-trabajo`**
Una herramienta web a medida de tu trabajo. Automatización de tareas repetitivas, plantillas, asistentes.

**`/sitio-personal`**
Un sitio web propio. Personal, institucional, profesional.

**`/dashboard-de-datos`**
Un dashboard interactivo con tus datos. Carga CSV, visualiza, filtra.

**`/asistente-de-investigacion`**
Una herramienta para tu trabajo académico. Análisis de corpus, gestión bibliográfica, codificación cualitativa.

**`/landing-de-proyecto`**
Una landing page para presentar un proyecto, producto o servicio.

**`/pieza-editorial`**
Una pieza editorial digital. Crónica, ensayo, dossier, especial periodístico.

**`/pieza-experimental`**
Una pieza web autoral sin reglas comerciales. Manifesto, bestiario, fanzine, tributo.

**`/juego-interactivo`**
Un mini-juego web. Trivia, memotest, generador, plataformero simple.

**`/agregador-curado`**
Un sitio que reúne contenido externo con tu mirada autoral.

---

## El flujo recomendado del taller

```
1. Instalar Claude Code
        ↓
2. Invocar /claude-md-global (una sola vez)
        ↓
3. ¿Tenés idea clara del proyecto?
   ├── SÍ → seguí al paso 4
   └── NO → invocá /explorador primero
        ↓
4. Crear la carpeta del proyecto
        ↓
5. Invocar la skill de construcción específica
   (esta skill pregunta sobre el proyecto y va
   guardando las decisiones a medida que avanzás)
        ↓
6. Iterar con # mientras construís
   (cada # guarda una regla nueva en el CLAUDE.md
   del proyecto)
        ↓
7. (Opcional) Correr /init si querés ordenar
   el CLAUDE.md del proyecto en algún momento
        ↓
8. Deploy a GitHub Pages
```

---

## Estructura del repo

```
taller-anfibia/
├── README.md
├── LICENSE
├── .gitignore
└── skills/
    ├── claude-md-global/SKILL.md
    ├── explorador/SKILL.md
    ├── herramienta-de-trabajo/SKILL.md
    ├── sitio-personal/SKILL.md
    ├── dashboard-de-datos/SKILL.md
    ├── asistente-de-investigacion/SKILL.md
    ├── landing-de-proyecto/SKILL.md
    ├── pieza-editorial/SKILL.md
    ├── pieza-experimental/SKILL.md
    ├── juego-interactivo/SKILL.md
    └── agregador-curado/SKILL.md
```

Cada skill vive en su propia carpeta con un archivo `SKILL.md` adentro. Es el formato estándar que requiere Claude Code.

---

## Cómo modificar una skill

Las skills son archivos `.md` editables. Si querés ajustar alguna a tu medida:

1. Abrís el archivo `SKILL.md` correspondiente con cualquier editor de texto.
2. Editás libremente.
3. Guardás.

Los cambios se aplican la próxima vez que invoques la skill.

**Importante**: si modificás una skill, modificá la copia en `~/.claude/skills/`, no la del repo clonado. Si querés que tus cambios queden en el repo, copialos también allí y hacé commit.

---

## Filosofía

Estas skills no programan por vos. Te guían en el proceso. La idea no es que vos no sepas qué está pasando, sino que tengas un acompañante que te haga las preguntas correctas y te empuje a tomar decisiones autorales.

El objetivo final del taller es que **después puedas armar tus propias skills**, sin necesitar las que yo te di. Esto es solo el andamio.

---

## Stack común

Todas las skills usan el mismo stack base:

- HTML / CSS / JavaScript vainilla.
- Cero frameworks pesados.
- Markdown para contenido.
- Git + GitHub para versionado y deploy.
- GitHub Pages para publicar.

Es lo que enseñamos en el taller. Es lo que rinde para piezas chicas a medianas.

---

## Origen

Estas skills fueron diseñadas mirando el formulario de inscripción real del taller, con 47 respuestas. Los patrones encontrados se agruparon en 11 caminos posibles, intentando cubrir a todo el grupo sin caer en hacer una skill por persona.

No son skills genéricas: son específicas para este grupo, este contexto y este momento. Pero pueden servirle a cualquier persona que esté arrancando con Claude Code.

---

## Licencia

[MIT](LICENSE). Uso libre. Si las modificás y querés compartirlas, mencioná de dónde vienen. Si te sirven para tu trabajo, escribime contando cómo. Eso me alegra.

---

*Thiago Donato · Anfibia Escuela · Mayo-Junio 2026*
