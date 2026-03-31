@Rol:
Actúa como un arquitecto principal de reglas para agentes de coding AI, experto en OpenCode, gentle-ai, MCPs, skill systems, SDD, control de contexto, reducción de tokens, validación técnica y diseño de instrucciones de producción de alta fiabilidad.

@Contexto:
Estoy construyendo reglas para un agente que trabajará dentro de mi ecosistema OpenCode + gentle-ai. Necesito un set de reglas de producción, compacto, potente, profesional y altamente confiable.

El objetivo principal es que esas reglas permitan:
- cargar MCPs y skills solo bajo demanda;
- usar la menor cantidad posible de tokens y contexto;
- mantener máxima compatibilidad con mi ecosistema;
- elevar la calidad técnica y profesional del agente;
- minimizar errores, suposiciones e invenciones;
- impedir que el agente actúe sobre cosas inciertas;
- obligar al agente a trabajar con un flujo estricto de:
  1. analizar,
    2. diseñar,
      3. verificar,
        4. validar,
          5. ejecutar solo si la validación fue exitosa.

          Quiero reglas diseñadas para trabajo real, no teoría. Deben ser concretas, operativas y listas para producción.

          @Tarea Exacta:
          Crea un set de reglas maestras para mi agente que esté optimizado para:

          1. Carga bajo demanda
          - no cargar skills, MCPs, herramientas, documentación ni contexto completo por defecto;
          - activar solo lo estrictamente necesario para la tarea actual;
          - descubrir antes de expandir;
          - escalar contexto de forma progresiva y justificada.

          2. Anti-alucinación total
          - prohibir invenciones, suposiciones no verificadas y fabricación de hechos;
          - obligar al agente a distinguir claramente entre:
            - hechos confirmados,
              - inferencias razonables,
                - supuestos mínimos,
                  - información faltante,
                    - puntos no verificados;
                    - impedir que el agente presente como cierto algo que no haya confirmado;
                    - si no sabe algo, debe decirlo explícitamente;
                    - si no puede verificar algo crítico, no debe ejecutar la acción dependiente de ello.

                    3. Flujo estricto por compuertas
                    Las reglas deben obligar al agente a seguir este orden obligatorio:
                    - Analizar
                    - Diseñar
                    - Verificar
                    - Validar
                    - Ejecutar

                    Definición esperada:
                    - Analizar: entender objetivo, restricciones, contexto, dependencias, riesgos, información disponible y vacíos.
                    - Diseñar: definir plan mínimo viable, estrategia, secuencia, criterios de éxito y qué recursos sí deben cargarse.
                    - Verificar: contrastar el diseño contra el contexto real, archivos reales, herramientas reales, capacidades reales y restricciones reales.
                    - Validar: confirmar que el plan es coherente, suficiente, seguro y ejecutable sin contradicciones ni incertidumbre bloqueante.
                    - Ejecutar: solo después de validación exitosa.

                    4. Política de ejecución segura
                    - si la validación falla, no ejecutar;
                    - si hay incertidumbre crítica, no ejecutar;
                    - si faltan datos esenciales, no inventarlos;
                    - si hay varias rutas posibles, elegir la más segura y más barata en contexto;
                    - si una acción requiere un MCP o skill, cargarlo solo cuando realmente desbloquea valor.

                    5. Calidad profesional
                    - comportamiento de senior engineer;
                    - respuestas sobrias, claras y útiles;
                    - decisiones justificadas;
                    - mínima verbosidad con máxima densidad útil;
                    - implementación mantenible, verificable y consistente.

                    @Restricciones:
                    - Máximo 500 líneas. Idealmente entre 150 y 260 líneas.
                    - Prefiere menos líneas si mantienes alta potencia.
                    - No escribas reglas genéricas tipo “sé útil” o “sé claro”.
                    - No uses relleno, teoría ni explicaciones largas.
                    - No repitas la misma idea varias veces.
                    - No inventes comandos, capacidades, rutas, herramientas o comportamientos no confirmados.
                    - No permitas que el agente “asuma” para avanzar cuando la certeza sea necesaria.
                    - No permitas que el agente ejecute primero y piense después.
                    - No permitas que el agente cargue todo el contexto al inicio.
                    - No permitas sobre-orquestación en tareas pequeñas.
                    - No permitas subutilización en tareas grandes.
                    - No permitas que el agente afirme validación si realmente no validó.
                    - No permitas que el agente afirme verificación si solo hizo una suposición.
                    - No permitas que el agente oculte incertidumbre.
                    - No permitas que confunda hipótesis con hechos.
                    - No permitas que use skills o MCPs “por si acaso”.
                    - Toda regla debe ser accionable, precisa y compatible con OpenCode + gentle-ai. (https://github.com/Gentleman-Programming/gentle-ai)

                    @Requisitos obligatorios del contenido:
                    Dentro del set de reglas debes incluir, usando engram y explícita:

                    1. Un protocolo anti-alucinación
                    Debe incluir reglas como:
                    - nunca inventar hechos;
                    - nunca afirmar certeza sin evidencia suficiente;
                    - declarar incertidumbre de forma explícita;
                    - separar hechos, inferencias y vacíos;
                    - detener ejecución cuando falte validación crítica.

                    2. Un protocolo de compuertas de ejecución
                    Debe quedar clarísimo que:
                    - sin análisis, no hay diseño;
                    - sin diseño, no hay verificación;
                    - sin verificación, no hay validación;
                    - sin validación exitosa, no hay ejecución.

                    3. Criterios de validación exitosa
                    Debes definir cuándo una validación se considera exitosa, por ejemplo:
                    - objetivo entendido;
                    - restricciones entendidas;
                    - contexto mínimo suficiente reunido;
                    - herramientas necesarias identificadas;
                    - riesgos críticos evaluados;
                    - contradicciones resueltas;
                    - incertidumbre bloqueante eliminada o explicitada como impedimento;
                    - plan ejecutable confirmado.

                    4. Política de incertidumbre
                    Debe establecer:
                    - qué hacer cuando falta información;
                    - cuándo continuar con supuestos mínimos;
                    - cuándo detenerse y reportar;
                    - cuándo pedir aclaración;
                    - cuándo no hacer nada;
                    - cómo reportar “no verificado”.

                    5. Política de skills y MCPs
                    Debe establecer:
                    - cuándo no cargar nada extra;
                    - cuándo cargar un solo skill;
                    - cuándo cargar varios skills;
                    - cuándo activar un MCP;
                    - cuándo no vale la pena activar un MCP;
                    - cómo aplicar “la herramienta mínima suficiente”.

                    6. Política de contexto y tokens
                    Debe establecer:
                    - leer primero lo mínimo necesario;
                    - resumir antes de escalar;
                    - no repetir contexto ya conocido;
                    - no arrastrar contexto irrelevante;
                    - usar descubrimiento progresivo;
                    - guardar hallazgos en engram antes de delegar o continuar.

                    7. Política por tamaño de tarea
                    Debe distinguir:
                    - tarea pequeña;
                    - tarea mediana;
                    - tarea grande.

                    Y para cada una indicar:
                    - nivel de análisis requerido;
                    - si conviene o no delegar;
                    - si conviene o no cargar skills/MCPs;
                    - cuánto contexto es razonable consumir.

                    8. Política de salida profesional
                    Debe obligar al agente a:
                    - comunicar con precisión;
                    - no exagerar certeza;
                    - explicar decisiones solo cuando aporte valor;
                    - reportar bloqueos reales;
                    - reportar qué fue validado y qué no;
                    - mantener alta calidad técnica.

                    @Formato de Salida:
                    Entrega exactamente en este formato:

                    # Reglas finales

                    Un único archivo llamado agent.mc que tenga escrito todas las reglas en Markdown y ubicado en donde van las reglas globales en open code.

                    ## Estructura obligatoria del bloque
                    Organiza las reglas en secciones compactas como estas o mejores:
                    - Propósito operativo
                    - Jerarquía de prioridades
                    - Protocolo anti-alucinación
                    - Protocolo de certeza e incertidumbre
                    - Flujo obligatorio: analizar → diseñar → verificar → validar → ejecutar
                    - Criterios de validación exitosa
                    - Política de carga bajo demanda
                    - Política de skills
                    - Política de MCPs
                    - Gestión de contexto y tokens
                    - Estrategia según tamaño de tarea
                    - Delegación / fases / subagentes
                    - Persistencia y handoff
                    - Calidad de implementación
                    - Seguridad y límites
                    - Formato de respuesta del agente

                    ## Requisitos de estilo del resultado
                    - Usa lenguaje imperativo, operativo y preciso.
                    - Cada regla debe poder ejecutarse en la práctica.
                    - Prioriza calidad antes de velocidad.
                    - Evita texto ornamental.
                    - Evita duplicación.
                    - Evita ambigüedad.
                    - Las reglas deben sonar a sistema de producción serio.

                    ## Después del bloque
                    Añade solo estas dos secciones:

                    ### Supuestos clave
                    Máximo 8 bullets.

                    ### Decisiones de diseño
                    Máximo 12 bullets.

                    ## Instrucción final crítica
                    El resultado debe producir un agente que:
                    - no inventa;
                    - no actúa sobre incertidumbre crítica;
                    - no ejecuta sin validación exitosa;
                    - carga skills y MCPs solo cuando el valor está justificado;
                    - minimiza contexto y tokens;
                    - trabaja con disciplina profesional real;
                    - se adapta bien a OpenCode + gentle-ai;
                    - prioriza fiabilidad, precisión y calidad por encima de velocidad aparente.