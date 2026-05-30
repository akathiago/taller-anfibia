# Análisis de Mejoras: Taller "Cómo entrenar a tu IA"

> Análisis realizado el 30 de mayo de 2026, basado en:
> - Encuesta previa con 55 respuestas
> - Repo de skills del taller
> - Landing page del taller
> - 4 perspectivas de análisis (pedagógico, UX, cobertura skills, marketing)

---

## Resumen Ejecutivo

### Top 5 Acciones Inmediatas

| # | Acción | Impacto | Esfuerzo |
|---|--------|---------|----------|
| 1 | Sesión de instalación asistida 2-3 días antes del taller | Crítico | Medio |
| 2 | Filtro de expectativas en clase 1 ("¿tu proyecto calza?") | Alto | Bajo |
| 3 | Proyecto común obligatorio antes del proyecto propio | Alto | Medio |
| 4 | Ajustar copy del landing (software → sitios web) | Alto | Bajo |
| 5 | Convertir clase 3 en "clínica de rescate" en vez de muestra | Alto | Bajo |

### Métricas Clave

| Métrica | Valor |
|---------|-------|
| Cobertura directa de skills | 48% |
| Cobertura parcial | 24% |
| Sin cobertura clara | 28% |
| Alumnos Windows | ~85% |
| Nunca usó Claude Code | ~70% |
| Riesgo de fricción en instalación | 40-50% |

---

## 1. Análisis Pedagógico

### Problema Central

La estructura asume que "entender conceptos → saber hacer". En realidad es al revés: hacer (con andamios) → fallar → resolver → entender.

### Progresión Cognitiva Actual

```
Clase 1: Teoría LLMs + Instalación + Bases conceptuales
    ↓ (salto abrupto)
Clase 2: Construir proyecto web completo en vivo
    ↓ (prematura)
Clase 3: Muestra de proyectos + técnicas intermedias
    ↓ (poco tiempo para integrar)
Clase 4: Presentaciones finales
```

**Problemas detectados:**

1. **Clase 1 → 2**: Salto abrupto de teoría a producción completa. No hay paso intermedio de práctica guiada con bajo riesgo de fracaso.

2. **Clase 2 → 3**: Lógica inversa. Se pide que muestren proyectos cuando recién construyeron uno en vivo (no ellos solos). La "muestra" de la clase 3 es prematura.

3. **Clase 3 → 4**: Presentación final una semana después de técnicas intermedias. Muy poco tiempo para integrar lo nuevo.

### Carga Cognitiva Clase 1

Tres bloques pesados en una sesión:

| Bloque | Carga |
|--------|-------|
| Cómo funcionan los LLMs | Conceptual alta — abstracción sin anclaje práctico |
| Instalación Claude Code | Técnica — frustración garantizada para algunos |
| Bases conceptuales | Más teoría sobre teoría |

**El riesgo**: Terminan la clase 1 con información pero sin sensación de logro. Para adultos no-técnicos, esto mata la motivación.

### Scaffolding: ¿Las skills alcanzan?

**Lo que hay:**
- `/explorador` y `/clase-2` para descubrir proyecto
- Skills de construcción por tipo de proyecto
- `/claude-md-global` para personalización

**Lo que falta:**
- Skill de diagnóstico cuando algo no funciona
- Skill de checkpoint que valide "hasta acá vas bien"
- Ejemplos de errores comunes (no solo el happy path)

### Recomendaciones Pedagógicas

#### 1. Invertir Clase 1: Primero hacer, después entender

Empezar con una micro-experiencia de éxito en los primeros 30 minutos. Que todos le pidan algo simple a Claude y vean resultado. Después explicar cómo funciona.

**Por qué**: Ancla la teoría en experiencia. "Ah, eso es lo que estaba pasando cuando hice X."

#### 2. Checkpoint de instalación ANTES de clase 1

Mandar instrucciones de instalación una semana antes. Clase 1 arranca con "¿quién no pudo instalar?" y se resuelve en 15 min, no en 45.

**Implementación**: Video de 5 min + documento paso a paso + canal de ayuda async.

#### 3. Convertir Clase 3 en "Clínica de proyectos"

Clase 3 = traé tu proyecto roto/trabado/incompleto. Trabajamos en grupos pequeños resolviendo problemas reales. Las "técnicas intermedias" surgen de necesidades concretas, no de curriculum predefinido.

**Por qué**: Normaliza el error. Aprenden viendo cómo otros resuelven problemas similares.

#### 4. Crear skill `/rescate` para problemas comunes

Una skill que cuando algo falla, hace diagnóstico guiado:
- ¿Claude no responde? → Checklist de conexión
- ¿El código no funciona? → Pasos de debugging básico
- ¿No sabés cómo seguir? → Preguntas para reencuadrar

#### 5. Implementar "proyecto semilla" obligatorio

Todos arrancan Clase 2 con el mismo proyecto base mínimo (una landing de una página). Lo personalizan durante la clase. Recién en semana 2-3 hacen proyecto propio.

**Por qué**: Reduce variables. Si todos parten del mismo punto, los problemas son comparables y resolubles en grupo.

### Oportunidades Pedagógicas Perdidas

| Elemento | Estado |
|----------|--------|
| Pair programming | Ausente |
| Feedback async entre clases | No mencionado |
| Checkpoints de progreso | No hay |
| Banco de errores documentados | No existe |
| Proyecto ejemplo completo para explorar | Falta |
| Gradualidad del riesgo | Pasan de 0 a "publicá tu proyecto" |

---

## 2. Análisis UX / Journey del Alumno

### Perfil Real de los Alumnos

**Datos demográficos:**
- Edad: 22-60 años, promedio ~40
- Países: mayoría Argentina, también Colombia, Perú, México
- OS: ~85% Windows, ~15% Mac
- Experiencia Claude Code: mayoría "Nunca lo usé" o "toqué muy poco"

**Profesiones (diversidad enorme):**
- Comunicación/periodismo: ~15
- Docencia/investigación/academia: ~12
- Abogadas: 3
- Diseño/UX: 3
- Arquitectura: 1
- Terapia/coaching: 2
- Administración/gestión: ~8
- Marketing: 4
- Emprendedores: 3

**Motivaciones expresadas:**
- "Curiosidad" aparece ~15 veces
- "FOMO" aparece 4 veces
- "Automatizar", "herramientas", "aprender" frecuentes

### Puntos de Fricción Anticipados

#### 1. Instalación en Windows (CRÍTICO)

85% del grupo usa Windows. La instalación típica involucra:
- Instalar Node.js
- Instalar Git para Windows (con 10+ opciones confusas)
- Configurar PATH
- Configurar credenciales

**Puntos de quiebre:**
- El installer de Git para Windows tiene 8 pantallas con jerga técnica
- El PATH de Windows es concepto alienígena para no-técnicos
- PowerShell vs CMD vs Git Bash: Windows tiene 3 terminales distintas
- Permisos de administrador en laptops corporativas

**Fricción estimada**: 40-50% va a tener algún problema. De esos, 20% va a necesitar asistencia personalizada.

#### 2. Terminal/Línea de comandos

**Problemas específicos:**
- El concepto de "carpeta actual" (cwd) no es intuitivo
- Los comandos de navegación (cd, ls, dir) no se enseñan fuera de cursos técnicos
- Copiar/pegar en terminal de Windows funciona distinto
- Los errores de terminal son crípticos
- El miedo a romper algo es real

**Fricción estimada**: 70% va a sentir incomodidad significativa con la terminal.

#### 3. Git/GitHub para principiantes

**Problemas anticipados:**
- La diferencia entre Git y GitHub es confusa
- Autenticación en GitHub cambió (necesita tokens o SSH keys)
- Los comandos de Git son secuenciales y hay que entender el flujo mental
- Merge conflicts son inevitables si editan desde web y local

**Fricción estimada**: Git va a ser el punto de abandono para 25-30% si no hay scaffolding.

#### 4. Deploy a GitHub Pages

**Problemas:**
- Requiere configuración manual en Settings
- El tiempo de propagación genera ansiedad
- Los errores de build no dan feedback claro

**Fricción estimada**: 15% va a tener problemas con el primer deploy.

### Momentos de Abandono Potencial

| Momento | Trigger | Riesgo |
|---------|---------|--------|
| Instalación (Día 1) | Algo falla en terminal | 15-20% |
| Primera interacción Claude Code | Resultado no es lo esperado | 10-15% |
| Proyecto propio no encaja (Día 2-3) | Skills no cubren la idea | 20-25% |
| Git entra en escena (Día 3-4) | Conflict, credenciales | 15-20% |
| Deploy fallido (Día 4-5) | Sitio no aparece online | 10% |

### Checkpoints que Faltan

1. **"Funciona localmente"**: antes de Git, antes de deploy, ver el sitio en el navegador
2. **"Entiendo qué hizo Claude"**: después de cada generación de código
3. **"Mi proyecto calza"**: validación temprana de viabilidad
4. **"Puedo cambiar algo sin ayuda"**: ejercicio de cambio pequeño sin asistencia

### El Problema de la Diversidad

**Clusters detectados:**

| Cluster | Cantidad | Skills que los cubren |
|---------|----------|----------------------|
| Comunicación/Periodismo | ~15 | Bien cubiertas |
| Docencia/Investigación/Academia | ~12 | Parcialmente cubiertas |
| Abogadas y perfiles legales | 3 | Débilmente cubiertas |
| Marketing/Emprendedores | ~7 | Bien cubiertas |
| Perfiles atípicos | varios | Depende del caso |

**El problema pedagógico**: explicar lo suficiente para la neurocientífica de 59 años aburre a la diseñadora de 22. Ir al ritmo de la diseñadora pierde a la neurocientífica.

**Solución recomendada**: Proyecto común obligatorio primero que nivela al grupo, después proyecto propio.

### Quick Wins de Alto Impacto

| Quick Win | Impacto | Esfuerzo |
|-----------|---------|----------|
| Video de instalación pre-grabado (5 min, específico Windows) | Reduce 50% fricciones instalación | Bajo |
| Checklist "¿Tu proyecto calza?" antes del taller | Filtra expectativas imposibles | Muy bajo |
| Glosario visual de 10 términos clave | Reduce brecha de vocabulario | Bajo |
| Canal "#ayuda-urgente" con promesa de respuesta <30 min | Contención emocional | Bajo |
| Template de "primer proyecto" pre-armado | Reduce terror de pantalla en blanco | Medio |

### Recomendaciones UX (por prioridad)

#### 1. CRÍTICO: Sesión de instalación asistida previa

Una sesión opcional de 1 hora, 2-3 días antes del taller, solo para instalar Node, Git y configurar credenciales. Zoom con pantalla compartida.

**Por qué**: Si el día 1 arranca con instalación fallida, el alumno empieza frustrado y no recupera.

#### 2. ALTO: Filtro de expectativas temprano

En la primera sesión, antes de tocar código, hacer ejercicio grupal: "contá tu proyecto en una frase y decí qué querés que haga". Detectar los que no calzan y ofrecer versión reducida viable.

**Por qué**: Mejor desilusionar el día 1 que el día 4.

#### 3. ALTO: Proyecto común obligatorio

Todos hacen el mismo mini-proyecto primero (portfolio de una sola página con 3 secciones). Después cada uno adapta a su caso.

**Por qué**: Permite nivelar sin aburrir a nadie.

#### 4. MEDIO: Checkpoint de autonomía obligatorio

En algún momento (día 3 sugerido), ejercicio donde Claude NO puede ayudar. El alumno tiene que cambiar algo pequeño editando el código a mano.

**Por qué**: Si nunca tocó el código sin asistencia, no desarrolló autonomía.

#### 5. MEDIO: Documentación de errores comunes

Documento con los 15 errores más comunes de instalación/Git/deploy, con capturas de pantalla y solución paso a paso.

---

## 3. Análisis de Cobertura: Skills vs. Encuesta

### Proyectos de los Alumnos vs. Skills Disponibles

#### Match Directo (48%)

| Proyecto | Skill | Confianza |
|----------|-------|-----------|
| Ana Victoria - Dashboard + web artista | `/dashboard-de-datos` + `/sitio-personal` | Alta |
| Sofía - Web del área de trabajo | `/sitio-personal` o `/landing-de-proyecto` | Alta |
| Nicolás - Crónicas, podcast, recetas | `/pieza-editorial` | Alta |
| Agustina - Prototipo tesis multimedia duelo | `/pieza-experimental` | Alta |
| Catalina - Web paz y drogas | `/pieza-editorial` o `/pieza-experimental` | Media-Alta |
| Sofía S - Agregador encuestas | `/agregador-curado` | Alta |
| Gabriela - Web desarrollo personal | `/sitio-personal` + `/pieza-editorial` | Alta |
| Leonardo - Escritos legales | `/asistente-legal` | Alta |
| Ailín - Fichero tipográfico | `/dashboard-de-datos` | Media |
| Ailín - Juego tipo Catán | `/juego-interactivo` | Alta |
| Aien - Juegos cambio climático | `/juego-interactivo` | Alta |
| Florencia - Reportes datos consumo | `/dashboard-de-datos` | Media |

#### Match Parcial (24%)

| Proyecto | Skill cercana | Qué falta |
|----------|---------------|-----------|
| Mariana - Formularios con su estilo | `/herramienta-de-trabajo` | Automatización más específica |
| Mónica - Automatizar tareas docentes | `/herramienta-de-trabajo` | Casos de uso docente |
| Valeria - Análisis datos neurociencia | `/asistente-de-investigacion` | Manejo de datasets grandes |
| Florencia GB - Cotejo traducciones | `/asistente-de-investigacion` | Comparación de textos |
| Inés - Panel stock y distribución | `/dashboard-de-datos` | Lógica de inventario |
| Carina - Mapeo 427 municipios | `/dashboard-de-datos` + `/agregador-curado` | Visualización geográfica |

#### Sin Match Claro (28%)

| Proyecto | Por qué no encaja |
|----------|-------------------|
| Carolina - Gemelos digitales | Requiere backend, APIs, modelado complejo |
| Daiana - Tienda online | E-commerce tiene lógica propia |
| Julia - Habilidades mercado laboral | Es formación, no un proyecto construible |
| Ezequiel - Personajes IA análisis político | Agentes conversacionales, fuera de scope |
| Pablo - Sistema seguimiento envíos | Integración con sistemas externos |
| Felipe - Plataforma trading | APIs financieras, tiempo real |
| María Eugenia - Leer AutoCAD | Integración con software cerrado |
| Florencia H - Scan Audit → PowerBI | Pipeline de datos entre herramientas |

### Gaps Evidentes

#### Gap 1: Integración con herramientas externas

**Casos:** María Eugenia (AutoCAD), Florencia H (Scan Audit → PowerBI), Felipe (plataformas trading)

Estos proyectos asumen que Claude Code puede leer formatos propietarios o conectarse a APIs en tiempo real. No puede.

#### Gap 2: E-commerce / Lógica de negocio

**Caso:** Daiana quiere "funcionalidades para tienda online"

No hay skill para carrito de compras, gestión de pedidos, integración con MercadoPago/Stripe.

#### Gap 3: Agentes autónomos / Chatbots

**Casos:** Ezequiel (personajes IA), Carolina (gemelos digitales)

Quieren entidades que "piensen" y respondan. Requiere arquitectura de prompts persistentes, posiblemente APIs externas.

#### Gap 4: Sistemas operativos de gestión

**Casos:** Pablo (seguimiento envíos), Inés (stock y distribución)

Son mini-ERPs. Requieren base de datos, CRUD completo, múltiples usuarios.

### Skills Probablemente Subutilizadas

| Skill | Matches en encuesta | Diagnóstico |
|-------|---------------------|-------------|
| `/pieza-experimental` | 1-2 | Muy de nicho |
| `/explorador` | 0 directos | Útil como onboarding, no como destino |
| `/guia-de-prompts` | 0 directos | Nadie pidió esto como proyecto |
| `/dudas-frecuentes` | 0 | Es soporte, no skill de construcción |

### Skills Faltantes Recomendadas

#### Prioridad Alta

**`/mini-sistema-de-gestion`**
- Para: Inés (stock), Pablo (envíos), Daiana (tienda)
- Qué hace: CRUD básico con localStorage o JSON, tabla editable, estados simples
- Limitación honesta: "Esto no reemplaza un ERP, pero te sirve para prototipar"

**`/agente-conversacional`**
- Para: Ezequiel (personajes), Carolina (gemelos digitales light)
- Qué hace: Crear un "personaje" con system prompt fijo que responde preguntas
- Implementación: HTML con API de Claude o similar

#### Prioridad Media

**`/conector-de-datos`**
- Para: Florencia H, Valeria, Carina
- Qué hace: Scripts para limpiar/transformar CSV, generar outputs para otras herramientas
- NO hace: Conexión directa a PowerBI/Excel

**`/tienda-simple`**
- Para: Daiana
- Qué hace: Catálogo de productos, formulario de contacto/pedido
- NO hace: Pagos integrados, stock en tiempo real

### Skills a Modificar

| Skill actual | Modificación |
|--------------|--------------|
| `/dashboard-de-datos` | Agregar ejemplos de inventario/stock, no solo métricas |
| `/herramienta-de-trabajo` | Incluir casos docentes explícitos |
| `/asistente-de-investigacion` | Agregar comparación de textos |

### Comunicación de Limitaciones

En el `/explorador` o al inicio:

```
QUÉ PODEMOS CONSTRUIR:
- Sitios web completos
- Dashboards con tus datos
- Herramientas de automatización
- Juegos y piezas interactivas

QUÉ REQUIERE TRABAJO ADICIONAL:
- Conexión con software cerrado (AutoCAD, PowerBI nativo)
- Sistemas de pago integrados
- Apps móviles nativas

EN ESOS CASOS: Te ayudamos a construir la parte que SÍ se puede,
y te orientamos para el resto.
```

### Framework para Comunicar Limitaciones a Alumnos

```
1. Validar el proyecto: "Esto tiene mucho sentido para tu trabajo"
2. Ser específico sobre el límite: "X herramienta es cerrada / requiere Y"
3. Ofrecer el pivot: "Lo que SÍ podemos hacer es..."
4. Mostrar el valor: "Esto te resuelve el 70% del problema manual"
```

### Casos Problemáticos Específicos y Pivots

**María Eugenia (AutoCAD → cómputo métrico)**
- Expectativa: "Que lea un .dwg y saque cantidades"
- Realidad: Claude Code no puede abrir archivos .dwg
- Pivot: Si exporta a CSV o tiene tablas, puede procesar eso
- Comunicación: "AutoCAD es cerrado, pero si exportás la tabla de materiales a Excel, ahí sí podemos automatizar el cómputo"

**Florencia H (Scan Audit → PowerBI)**
- Expectativa: Pipeline automático
- Realidad: Son dos sistemas cerrados
- Pivot: Script que transforma el output de Scan Audit a formato que PowerBI entiende
- Comunicación: "No podemos meternos adentro de PowerBI, pero sí preparar los datos para que los importes en dos clicks"

**Felipe (Plataforma trading)**
- Expectativa: Retomar algo complejo con APIs financieras
- Realidad: Requiere APIs pagas, tiempo real, seguridad
- Pivot: Dashboard de visualización con datos que él traiga manualmente
- Comunicación: "El trading en vivo tiene complejidades de seguridad que exceden el taller. Pero podemos armar el análisis visual de tus datos"

---

## 4. Análisis de Marketing: Landing vs. Realidad

### Promesas del Landing vs. Entrega Real

| Promesa del landing | Realidad | Veredicto |
|---------------------|----------|-----------|
| "Construir software describiendo ideas en lenguaje natural" | Sitios estáticos HTML/CSS/JS vanilla | **Oversell** |
| "Herramientas para el trabajo intelectual" | Herramientas personales sin backend | Parcialmente cierto |
| "Autonomía técnica" | Autonomía *con* Claude, no *sin* Claude | Hay que redefinir |
| "Desmitificar el código para no-programadores" | Sí cumple | OK |

### Gaps de Expectativa Peligrosos

| Expectativa probable | Realidad |
|---------------------|----------|
| "Voy a poder hacer apps" | Solo sitios estáticos |
| "Voy a poder hacer un sistema para mi empresa" | Herramientas individuales sin usuarios/login |
| "Voy a aprender a programar" | Vas a aprender a iterar con Claude |
| "Voy a poder conectar APIs" | No está en el scope |
| "Voy a poder hacer algo que funcione en mi celular" | PWA básica como mucho |

### El Elefante en la Sala: Costo Total

**Inversión inicial:**
- Taller: USD 100
- Claude Pro: USD 20/mes (mínimo 2 meses)
- **Total mínimo: USD 140**

**Inversión sostenida:**
- Para seguir usando lo aprendido: USD 20/mes indefinidamente

**Lo que el landing no dice:**
1. Que Claude Pro es requerido PERMANENTEMENTE para usar lo aprendido
2. Que las herramientas no funcionan sin Claude Code corriendo
3. Que el modelo de suscripción es recurrente, no one-time

### Audiencia Prometida vs. Audiencia Real

**Landing dice:** "Periodistas, editores, escritores, investigadores, docentes, artistas, diseñadores"

**La encuesta muestra:** Abogadas, arquitectas, administrativas, comerciantes

**El problema:** Las skills están diseñadas para trabajo intelectual humanístico. No para trabajo comercial, legal complejo, o técnico.

### Lo que Falta Comunicar

**En el landing:**
1. "Esto es para herramientas personales, no sistemas empresariales"
2. "Los proyectos son sitios estáticos que corren en el navegador"
3. "Necesitás mantener la suscripción de Claude Pro para seguir construyendo"
4. "Vas a aprender a colaborar con IA, no a programar en el sentido tradicional"
5. "El stack es HTML/CSS/JS vanilla — no vas a poder hacer apps móviles ni sistemas con usuarios"

### Recomendaciones de Copy

**Cambiar:**
> "Aprender a construir software describiendo ideas en lenguaje natural"

**Por:**
> "Aprender a construir sitios web y herramientas propias colaborando con IA"

**Cambiar:**
> "Diseñar herramientas para el trabajo intelectual"

**Por:**
> "Diseñar herramientas personales para tu trabajo — sitios, dashboards, piezas editoriales, mini-juegos"

**Agregar:**
> "Este taller no te enseña a programar en el sentido tradicional. Te enseña a usar Claude Code como colaborador técnico para hacer cosas que antes requerían un developer."

**Agregar (en requisitos):**
> "Claude Pro es necesario no solo durante el taller, sino para seguir usando lo aprendido después."

### Qué Decir en la Clase 1

**Minuto 1-5:**
> "Antes de arrancar, vamos a alinear expectativas. Este taller tiene un alcance específico."

**Mostrar en pantalla:**

```
LO QUE SÍ VAMOS A HACER:
- Sitios personales
- Portfolios
- Herramientas que corren en el navegador
- Dashboards con datos propios
- Piezas editoriales y experimentales
- Mini-juegos web

LO QUE NO VAMOS A HACER:
- Apps móviles
- Sistemas con usuarios y login
- Conexiones a bases de datos
- Integraciones con APIs externas
- Automatizaciones complejas
```

**Después preguntar:**
> "¿Alguno tenía en mente hacer algo que cae en la lista de 'no vamos a hacer'? Hablémoslo ahora."

---

## 5. Plan de Implementación Sugerido

### Antes del Taller (esta semana)

- [ ] Grabar video de instalación específico Windows (5 min)
- [ ] Crear documento "¿Tu proyecto calza?" con checklist
- [ ] Preparar glosario visual de 10 términos
- [ ] Crear canal #ayuda-urgente en Discord/Slack
- [ ] Agendar sesión de instalación asistida (1 hora, 2-3 días antes)

### Para Clase 1

- [ ] Preparar slide de "LO QUE SÍ / LO QUE NO"
- [ ] Diseñar micro-experiencia de éxito (primeros 30 min)
- [ ] Preparar ejercicio de filtro de proyectos

### Para Clase 2

- [ ] Crear template de "proyecto semilla" común
- [ ] Documentar los 15 errores más comunes con soluciones

### Para Clase 3

- [ ] Rediseñar como "clínica de rescate" en vez de muestra
- [ ] Preparar ejercicio de autonomía (cambio sin Claude)

### Skills a Crear

- [ ] `/rescate` - diagnóstico de problemas comunes
- [ ] `/mini-sistema-de-gestion` - CRUD básico
- [ ] `/agente-conversacional` - personajes con prompt fijo

### Skills a Modificar

- [ ] `/dashboard-de-datos` - agregar ejemplos de inventario
- [ ] `/herramienta-de-trabajo` - incluir casos docentes
- [ ] `/asistente-de-investigacion` - agregar comparación de textos

---

## Apéndice: Datos de la Encuesta

### Distribución por Sistema Operativo
- Windows: ~85%
- Mac: ~15%

### Distribución por Experiencia con Claude Code
- Nunca lo usé: ~60%
- Toqué muy poco: ~35%
- Ya construí cosas: ~5%

### Palabras más frecuentes en motivación
- Curiosidad: 15 menciones
- Herramientas: 10 menciones
- Automatizar: 8 menciones
- Aprender: 8 menciones
- FOMO: 4 menciones

### Proyectos más comunes por categoría
1. Sitios personales / portfolios
2. Dashboards de datos / métricas
3. Herramientas de automatización de trabajo
4. Piezas editoriales / contenido
5. Sistemas de gestión (sin skill adecuada)

---

*Documento generado el 30 de mayo de 2026*
