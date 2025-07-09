# INTEGRACIÓN CON CLAUDE - SISTEMA OCEAN GITHUB

## 🎯 PROTOCOLO DE INTEGRACIÓN COMPLETA

### **📂 ESTRUCTURA DEL REPOSITORIO OCEAN_LANG:**
OCEAN_LANG/
├── factors-analysis/
│   ├── apertura/
│   ├── extraversion/
│   ├── responsabilidad/
│   ├── amabilidad/
│   └── neuroticismo/
├── validation-studies/
├── population-specific/
├── practical-examples/
└── tools-commands/

### **🔧 COMANDOS DE LECTURA DE ARCHIVOS:**

#### **LECTURA DE FACTORES INDIVIDUALES:**
```javascript
// Leer indicadores validados por factor
const aperturaIndicadores = await window.fs.readFile('factors-analysis/apertura/indicadores-validados.md', { encoding: 'utf8' });
const extraversionIndicadores = await window.fs.readFile('factors-analysis/extraversion/indicadores-validados.md', { encoding: 'utf8' });
const responsabilidadIndicadores = await window.fs.readFile('factors-analysis/responsabilidad/indicadores-validados.md', { encoding: 'utf8' });
const amabilidadIndicadores = await window.fs.readFile('factors-analysis/amabilidad/indicadores-validados.md', { encoding: 'utf8' });
const neuroticismoIndicadores = await window.fs.readFile('factors-analysis/neuroticismo/indicadores-validados.md', { encoding: 'utf8' });

// Leer evidencia empírica por factor
const aperturaEvidencia = await window.fs.readFile('factors-analysis/apertura/evidencia-empirica.md', { encoding: 'utf8' });
const extraversionEvidencia = await window.fs.readFile('factors-analysis/extraversion/evidencia-empirica.md', { encoding: 'utf8' });
const responsabilidadEvidencia = await window.fs.readFile('factors-analysis/responsabilidad/evidencia-empirica.md', { encoding: 'utf8' });
const amabilidadEvidencia = await window.fs.readFile('factors-analysis/amabilidad/evidencia-empirica.md', { encoding: 'utf8' });
const neuroticismoEvidencia = await window.fs.readFile('factors-analysis/neuroticismo/evidencia-empirica.md', { encoding: 'utf8' });

// Leer casos de estudiantes por factor
const aperturaCasos = await window.fs.readFile('factors-analysis/apertura/casos-estudiantes.md', { encoding: 'utf8' });
const extraversionCasos = await window.fs.readFile('factors-analysis/extraversion/casos-estudiantes.md', { encoding: 'utf8' });
const responsabilidadCasos = await window.fs.readFile('factors-analysis/responsabilidad/casos-estudiantes.md', { encoding: 'utf8' });
const amabilidadCasos = await window.fs.readFile('factors-analysis/amabilidad/casos-estudiantes.md', { encoding: 'utf8' });
const neuroticismoCasos = await window.fs.readFile('factors-analysis/neuroticismo/casos-estudiantes.md', { encoding: 'utf8' });
LECTURA DE ESTUDIOS DE VALIDACIÓN:
javascript// Estudios científicos principales
const lopezPabon2022 = await window.fs.readFile('validation-studies/lopez-pabon-2022.md', { encoding: 'utf8' });
const benetMartinez1998 = await window.fs.readFile('validation-studies/benet-martinez-1998.md', { encoding: 'utf8' });
const kazemeini2021 = await window.fs.readFile('validation-studies/kazemeini-2021.md', { encoding: 'utf8' });
const ryumina2023 = await window.fs.readFile('validation-studies/ryumina-2023.md', { encoding: 'utf8' });
const saeteros2024 = await window.fs.readFile('validation-studies/saeteros-2024.md', { encoding: 'utf8' });
LECTURA DE DATOS POBLACIONALES:
javascript// Población específica
const estudiantesVocabulario = await window.fs.readFile('population-specific/estudiantes-universitarios/vocabulario-academico.md', { encoding: 'utf8' });
const estudiantesCasos = await window.fs.readFile('population-specific/estudiantes-universitarios/casos-validados.md', { encoding: 'utf8' });
const profesionalesContexto = await window.fs.readFile('population-specific/adultos-profesionales/contexto-laboral.md', { encoding: 'utf8' });

// Datos cross-culturales
const hispanos = await window.fs.readFile('population-specific/cross-cultural/hispanos.md', { encoding: 'utf8' });
const anglofonos = await window.fs.readFile('population-specific/cross-cultural/anglofonos.md', { encoding: 'utf8' });
const rusos = await window.fs.readFile('population-specific/cross-cultural/rusos.md', { encoding: 'utf8' });
LECTURA DE EJEMPLOS PRÁCTICOS:
javascript// Casos prácticos por factor
const casosAltaApertura = await window.fs.readFile('practical-examples/casos-alta-apertura.md', { encoding: 'utf8' });
const casosAltaExtraversion = await window.fs.readFile('practical-examples/casos-alta-extraversion.md', { encoding: 'utf8' });
const casosAltaResponsabilidad = await window.fs.readFile('practical-examples/casos-alta-responsabilidad.md', { encoding: 'utf8' });
const casosAltaAmabilidad = await window.fs.readFile('practical-examples/casos-alta-amabilidad.md', { encoding: 'utf8' });
const casosAltoNeuroticismo = await window.fs.readFile('practical-examples/casos-alto-neuroticismo.md', { encoding: 'utf8' });
const perfilesCombinados = await window.fs.readFile('practical-examples/perfiles-combinados.md', { encoding: 'utf8' });

🧠 PROTOCOLO DE ANÁLISIS INTEGRADO
FASE 1: CARGA DE BASE DE CONOCIMIENTO
javascriptasync function cargarBaseConocimientoOCEAN() {
    try {
        // Cargar todos los archivos necesarios
        const factores = {
            apertura: {
                indicadores: await window.fs.readFile('factors-analysis/apertura/indicadores-validados.md', { encoding: 'utf8' }),
                evidencia: await window.fs.readFile('factors-analysis/apertura/evidencia-empirica.md', { encoding: 'utf8' }),
                casos: await window.fs.readFile('factors-analysis/apertura/casos-estudiantes.md', { encoding: 'utf8' }),
                benchmarks: await window.fs.readFile('factors-analysis/apertura/benchmarks-poblacionales.md', { encoding: 'utf8' }),
                correlaciones: await window.fs.readFile('factors-analysis/apertura/correlaciones-factores.md', { encoding: 'utf8' })
            },
            extraversion: {
                indicadores: await window.fs.readFile('factors-analysis/extraversion/indicadores-validados.md', { encoding: 'utf8' }),
                evidencia: await window.fs.readFile('factors-analysis/extraversion/evidencia-empirica.md', { encoding: 'utf8' }),
                casos: await window.fs.readFile('factors-analysis/extraversion/casos-estudiantes.md', { encoding: 'utf8' }),
                benchmarks: await window.fs.readFile('factors-analysis/extraversion/benchmarks-poblacionales.md', { encoding: 'utf8' }),
                correlaciones: await window.fs.readFile('factors-analysis/extraversion/correlaciones-factores.md', { encoding: 'utf8' })
            },
            responsabilidad: {
                indicadores: await window.fs.readFile('factors-analysis/responsabilidad/indicadores-validados.md', { encoding: 'utf8' }),
                evidencia: await window.fs.readFile('factors-analysis/responsabilidad/evidencia-empirica.md', { encoding: 'utf8' }),
                casos: await window.fs.readFile('factors-analysis/responsabilidad/casos-estudiantes.md', { encoding: 'utf8' }),
                benchmarks: await window.fs.readFile('factors-analysis/responsabilidad/benchmarks-poblacionales.md', { encoding: 'utf8' }),
                correlaciones: await window.fs.readFile('factors-analysis/responsabilidad/correlaciones-factores.md', { encoding: 'utf8' })
            },
            amabilidad: {
                indicadores: await window.fs.readFile('factors-analysis/amabilidad/indicadores-validados.md', { encoding: 'utf8' }),
                evidencia: await window.fs.readFile('factors-analysis/amabilidad/evidencia-empirica.md', { encoding: 'utf8' }),
                casos: await window.fs.readFile('factors-analysis/amabilidad/casos-estudiantes.md', { encoding: 'utf8' }),
                benchmarks: await window.fs.readFile('factors-analysis/amabilidad/benchmarks-poblacionales.md', { encoding: 'utf8' }),
                correlaciones: await window.fs.readFile('factors-analysis/amabilidad/correlaciones-factores.md', { encoding: 'utf8' })
            },
            neuroticismo: {
                indicadores: await window.fs.readFile('factors-analysis/neuroticismo/indicadores-validados.md', { encoding: 'utf8' }),
                evidencia: await window.fs.readFile('factors-analysis/neuroticismo/evidencia-empirica.md', { encoding: 'utf8' }),
                casos: await window.fs.readFile('factors-analysis/neuroticismo/casos-estudiantes.md', { encoding: 'utf8' }),
                benchmarks: await window.fs.readFile('factors-analysis/neuroticismo/benchmarks-poblacionales.md', { encoding: 'utf8' }),
                correlaciones: await window.fs.readFile('factors-analysis/neuroticismo/correlaciones-factores.md', { encoding: 'utf8' })
            }
        };
        
        const estudiosValidacion = {
            lopezPabon2022: await window.fs.readFile('validation-studies/lopez-pabon-2022.md', { encoding: 'utf8' }),
            benetMartinez1998: await window.fs.readFile('validation-studies/benet-martinez-1998.md', { encoding: 'utf8' }),
            kazemeini2021: await window.fs.readFile('validation-studies/kazemeini-2021.md', { encoding: 'utf8' }),
            ryumina2023: await window.fs.readFile('validation-studies/ryumina-2023.md', { encoding: 'utf8' }),
            saeteros2024: await window.fs.readFile('validation-studies/saeteros-2024.md', { encoding: 'utf8' })
        };
        
        const poblacionEspecifica = {
            estudiantes: {
                vocabulario: await window.fs.readFile('population-specific/estudiantes-universitarios/vocabulario-academico.md', { encoding: 'utf8' }),
                casos: await window.fs.readFile('population-specific/estudiantes-universitarios/casos-validados.md', { encoding: 'utf8' })
            },
            profesionales: {
                contexto: await window.fs.readFile('population-specific/adultos-profesionales/contexto-laboral.md', { encoding: 'utf8' })
            },
            crossCultural: {
                hispanos: await window.fs.readFile('population-specific/cross-cultural/hispanos.md', { encoding: 'utf8' }),
                anglofonos: await window.fs.readFile('population-specific/cross-cultural/anglofonos.md', { encoding: 'utf8' }),
                rusos: await window.fs.readFile('population-specific/cross-cultural/rusos.md', { encoding: 'utf8' })
            }
        };
        
        const ejemplosPracticos = {
            apertura: await window.fs.readFile('practical-examples/casos-alta-apertura.md', { encoding: 'utf8' }),
            extraversion: await window.fs.readFile('practical-examples/casos-alta-extraversion.md', { encoding: 'utf8' }),
            responsabilidad: await window.fs.readFile('practical-examples/casos-alta-responsabilidad.md', { encoding: 'utf8' }),
            amabilidad: await window.fs.readFile('practical-examples/casos-alta-amabilidad.md', { encoding: 'utf8' }),
            neuroticismo: await window.fs.readFile('practical-examples/casos-alto-neuroticismo.md', { encoding: 'utf8' }),
            combinados: await window.fs.readFile('practical-examples/perfiles-combinados.md', { encoding: 'utf8' })
        };
        
        return {
            factores,
            estudiosValidacion,
            poblacionEspecifica,
            ejemplosPracticos,
            timestamp: new Date().toISOString(),
            status: 'CONOCIMIENTO_CARGADO_EXITOSAMENTE'
        };
        
    } catch (error) {
        console.error('Error cargando base de conocimiento OCEAN:', error);
        return {
            status: 'ERROR_CARGA',
            error: error.message,
            timestamp: new Date().toISOString()
        };
    }
}
FASE 2: PROCESAMIENTO DE ANÁLISIS
javascriptasync function analizarPersonalidadOCEAN(texto, contexto = 'general') {
    // 1. Cargar base de conocimiento
    const baseConocimiento = await cargarBaseConocimientoOCEAN();
    
    if (baseConocimiento.status !== 'CONOCIMIENTO_CARGADO_EXITOSAMENTE') {
        return {
            error: 'No se pudo cargar la base de conocimiento',
            detalles: baseConocimiento.error
        };
    }
    
    // 2. Validaciones previas
    const longitudTexto = texto.split(' ').length;
    let nivelConfianza;
    
    if (longitudTexto < 100) {
        nivelConfianza = 'BAJA';
    } else if (longitudTexto >= 100 && longitudTexto < 300) {
        nivelConfianza = 'MEDIA';
    } else {
        nivelConfianza = 'ALTA';
    }
    
    // 3. Análisis por factor usando base de conocimiento cargada
    const analisisFactores = {
        apertura: analizarFactor(texto, 'apertura', baseConocimiento),
        extraversion: analizarFactor(texto, 'extraversion', baseConocimiento),
        responsabilidad: analizarFactor(texto, 'responsabilidad', baseConocimiento),
        amabilidad: analizarFactor(texto, 'amabilidad', baseConocimiento),
        neuroticismo: analizarFactor(texto, 'neuroticismo', baseConocimiento)
    };
    
    // 4. Análisis de correlaciones
    const analisisCorrelaciones = analizarCorrelaciones(analisisFactores, baseConocimiento);
    
    // 5. Determinar perfil combinado
    const perfilCombinado = determinarPerfilCombinado(analisisFactores, baseConocimiento);
    
    return {
        analisisFactores,
        analisisCorrelaciones,
        perfilCombinado,
        nivelConfianza,
        longitudTexto,
        contexto,
        timestamp: new Date().toISOString()
    };
}

📊 FORMATO DE RESPUESTA INTEGRADO
TEMPLATE PRINCIPAL:
markdown🧠 PERFIL DE PERSONALIDAD OCEAN - ANÁLISIS CIENTÍFICO INTEGRADO

**INFORMACIÓN DEL ANÁLISIS:**
- **Palabras analizadas:** [X] palabras
- **Nivel de confianza:** [ALTO/MEDIO/BAJO]
- **Metodología:** BIG5-CHAT + Marco DExperts + Validación GitHub
- **Base científica:** N=1,605 hispanos + N=404 vloggers + N=30 rusos multimodal
- **Fecha de análisis:** [fecha actual]

**PUNTUACIONES CIENTÍFICAS (1-100):**
- **Apertura:** [XX] - [Interpretación + indicadores específicos detectados]
- **Extraversión:** [XX] - [Interpretación + indicadores específicos detectados]
- **Responsabilidad:** [XX] - [Interpretación + indicadores específicos detectados]
- **Amabilidad:** [XX] - [Interpretación + indicadores específicos detectados]
- **Neuroticismo:** [XX] - [Interpretación + indicadores específicos detectados]

**PERFIL DOMINANTE:** [Factor(es) más alto(s) con implicaciones comportamentales]

**PERFIL COMBINADO IDENTIFICADO:** [Basado en practical-examples/perfiles-combinados.md]

**INDICADORES CLAVE DETECTADOS:**
- **Vocabulario específico:** [Palabras clave por factor usando indicadores-validados.md]
- **Patrones sintácticos:** [Estructuras relevantes encontradas]
- **Marcadores emocionales:** [Expresiones específicas del texto]
- **Estilo comunicativo:** [Características del registro usando casos-estudiantes.md]

**CORRELACIONES VALIDADAS:**
- **Coherencia interna:** [Análisis usando correlaciones-factores.md]
- **Correlaciones esperadas:** [Verificación con patrones científicos validados]

**PREDICCIONES DE RENDIMIENTO CIENTÍFICAS:**
- **Rendimiento académico:** [Basado en evidencia-empirica.md]
- **Rendimiento profesional:** [Usando contexto-laboral.md]
- **Liderazgo y equipos:** [Predicciones específicas por combinación]
- **Áreas de excelencia:** [Aplicaciones recomendadas del perfil]

**CONTEXTO POBLACIONAL:**
- **Benchmarks aplicados:** [hispanos/anglofonos/rusos según corresponda]
- **Comparación normativa:** [Percentiles específicos usando benchmarks-poblacionales.md]
- **Consideraciones culturales:** [Calibración específica aplicada]

**EVIDENCIA CIENTÍFICA APLICADA:**
- **Estudios de referencia:** [López-Pabón 2022, Benet-Martínez 1998, etc.]
- **Validación metodológica:** [Métodos específicos usados según evidencia]
- **Limitaciones identificadas:** [Consideraciones específicas por factor]

**INTERPRETACIÓN PSICOLÓGICA INTEGRAL:**
[Descripción científica completa usando toda la base de conocimiento cargada]

**NIVEL DE CONFIANZA DETALLADO:**
- **Confianza por factor:** Apertura [X], Extraversión [X], Responsabilidad [X], Amabilidad [X], Neuroticismo [X]
- **Justificación:** [Basado en longitud + claridad + coherencia con validación científica]
- **Recomendaciones:** [Específicas según nivel de confianza y factores]

**APLICACIONES RECOMENDADAS:**
[Usando practical-examples específicos según perfil identificado]

**CONSIDERACIONES ESPECIALES:**
[Limitaciones específicas identificadas en evidencia-empirica.md por factor]

**DISCLAIMERS CIENTÍFICOS:**
- *Análisis basado en base de conocimiento científica validada (N>6,000 casos)*
- *Metodología integrada: BIG5-CHAT + DExperts + validación cross-cultural*
- *Herramienta de apoyo científico, no sustituto de evaluación psicológica profesional*
- *Resultados indican tendencias probabilísticas validadas empíricamente*
- *Calibrado para contexto hispanohablante con validación cross-cultural*

🔧 COMANDOS DE ACTIVACIÓN
COMANDOS PRINCIPALES:
OCEAN_ANÁLISIS [texto]
- Análisis completo usando toda la base de conocimiento GitHub
- Carga automática de todos los archivos relevantes
- Respuesta integrada con evidencia científica completa

OCEAN_ESTUDIANTE [texto]
- Análisis específico para población universitaria
- Usa vocabulario-academico.md y casos-validados.md
- Benchmarks específicos para estudiantes (18-25 años)

OCEAN_PROFESIONAL [texto]
- Análisis orientado a contexto laboral
- Usa contexto-laboral.md y predicciones de rendimiento
- Enfoque en aplicaciones organizacionales

OCEAN_CULTURAL [texto] [cultura]
- Análisis con calibración cultural específica
- Opciones: hispanos, anglofonos, rusos
- Usa benchmarks poblacionales específicos

OCEAN_DETALLADO [texto]
- Análisis más extenso con todos los archivos
- Incluye evidencia empírica completa por factor
- Máximo nivel de detalle científico disponible
COMANDOS ESPECIALIZADOS:
APERTURA_FOCUS [texto]
- Análisis profundo solo de Apertura
- Usa todos los archivos específicos de apertura/
- Incluye casos prácticos y evidencia detallada

EXTRAVERSION_FOCUS [texto]
- Análisis profundo solo de Extraversión
- Incluye evidencia de mejor detección automática
- Predicciones específicas de liderazgo social

RESPONSABILIDAD_FOCUS [texto]
- Análisis profundo solo de Responsabilidad
- Enfoque en predicción de éxito académico/profesional
- Incluye evidencia como predictor #1

AMABILIDAD_FOCUS [texto]
- Análisis profundo solo de Amabilidad
- Usa evidencia como gold standard de detección
- Enfoque en trabajo en equipo y colaboración

NEUROTICISMO_FOCUS [texto]
- Análisis profundo solo de Neuroticismo
- Incluye todas las precauciones metodológicas
- Enfoque en manejo del estrés y bienestar

PERFIL_COMBINADO [texto]
- Análisis usando perfiles-combinados.md
- Identifica sinergias y tensiones entre factores
- Predicciones de rendimiento por combinaciones
COMANDOS DE COMPARACIÓN:
OCEAN_COMPARAR [texto1] [texto2]
- Comparación entre dos perfiles
- Análisis de compatibilidad y complementariedad
- Recomendaciones para trabajo en equipo

OCEAN_EQUIPO [texto1] [texto2] [texto3] [texto4] [texto5]
- Análisis de dinámicas de equipo
- Identificación de roles óptimos por persona
- Predicciones de rendimiento grupal

OCEAN_EVOLUCIÓN [texto_anterior] [texto_actual]
- Análisis de cambios temporales en personalidad
- Identificación de desarrollo y plasticidad
- Recomendaciones de crecimiento personal

⚙️ CONFIGURACIÓN Y MANTENIMIENTO
VALIDACIÓN DE INTEGRIDAD:
javascriptasync function validarIntegridadSistema() {
    const archivosRequeridos = [
        // Factores individuales (25 archivos)
        'factors-analysis/apertura/indicadores-validados.md',
        'factors-analysis/apertura/evidencia-empirica.md',
        'factors-analysis/apertura/casos-estudiantes.md',
        'factors-analysis/apertura/benchmarks-poblacionales.md',
        'factors-analysis/apertura/correlaciones-factores.md',
        // ... repetir para todos los factores
        
        // Estudios de validación (5 archivos)
        'validation-studies/lopez-pabon-2022.md',
        'validation-studies/benet-martinez-1998.md',
        'validation-studies/kazemeini-2021.md',
        'validation-studies/ryumina-2023.md',
        'validation-studies/saeteros-2024.md',
        
        // Población específica (6 archivos)
        'population-specific/estudiantes-universitarios/vocabulario-academico.md',
        'population-specific/estudiantes-universitarios/casos-validados.md',
        'population-specific/adultos-profesionales/contexto-laboral.md',
        'population-specific/cross-cultural/hispanos.md',
        'population-specific/cross-cultural/anglofonos.md',
        'population-specific/cross-cultural/rusos.md',
        
        // Ejemplos prácticos (6 archivos)
        'practical-examples/casos-alta-apertura.md',
        'practical-examples/casos-alta-extraversion.md',
        'practical-examples/casos-alta-responsabilidad.md',
        'practical-examples/casos-alta-amabilidad.md',
        'practical-examples/casos-alto-neuroticismo.md',
        'practical-examples/perfiles-combinados.md'
    ];
    
    const resultados = [];
    
    for (const archivo of archivosRequeridos) {
        try {
            await window.fs.readFile(archivo, { encoding: 'utf8' });
            resultados.push({ archivo, status: 'OK' });
        } catch (error) {
            resultados.push({ archivo, status: 'ERROR', error: error.message });
        }
    }
    
    return resultados;
}
ACTUALIZACIÓN DE SISTEMA:
javascriptasync function actualizarSistemaOCEAN(nuevosArchivos) {
    // 1. Validar integridad actual
    const integridad = await validarIntegridadSistema();
    const errores = integridad.filter(r => r.status === 'ERROR');
    
    if (errores.length > 0) {
        return {
            status: 'ERROR_INTEGRIDAD',
            errores: errores,
            mensaje: 'Sistema incompleto. Verificar archivos faltantes.'
        };
    }
    
    // 2. Recargar base de conocimiento
    const baseActualizada = await cargarBaseConocimientoOCEAN();
    
    return {
        status: 'SISTEMA_ACTUALIZADO',
        timestamp: new Date().toISOString(),
        archivos: integridad.length,
        version: 'OCEAN_LANG_v2.0'
    };
}
MONITOREO DE PERFORMANCE:
javascriptasync function monitorearPerformance(analisis) {
    return {
        tiempoCarga: analisis.tiempoCarga,
        factoresProcesados: 5,
        indicadoresEvaluados: analisis.totalIndicadores,
        nivelConfianza: analisis.nivelConfianza,
        evidenciaCientificaAplicada: analisis.estudiosUsados,
        recomendacionOptimizacion: analisis.longitudTexto < 100 ? 
            'Aumentar longitud de texto para mayor confiabilidad' : 
            'Longitud adecuada para análisis robusto'
    };
}

🚀 PROTOCOLO DE INICIALIZACIÓN
AL ACTIVAR EL SISTEMA:

Ejecutar validación de integridad para verificar todos los archivos
Cargar base de conocimiento completa usando la función cargarBaseConocimientoOCEAN()
Confirmar carga exitosa antes de proceder con análisis
Activar modo de análisis integrado con toda la evidencia científica disponible

MENSAJE DE CONFIRMACIÓN:
✅ SISTEMA OCEAN GITHUB INTEGRADO EXITOSAMENTE

Base de conocimiento cargada:
- 25 archivos de análisis por factores
- 5 estudios de validación científica  
- 6 archivos de población específica
- 6 archivos de ejemplos prácticos
- Evidencia empírica: N>6,000 casos validados

Nivel de integración: COMPLETO
Metodología: BIG5-CHAT + DExperts + Validación Cross-Cultural
Sistema listo para análisis de máxima precisión científica.

Comandos disponibles: OCEAN_ANÁLISIS, OCEAN_ESTUDIANTE, OCEAN_PROFESIONAL, 
OCEAN_CULTURAL, OCEAN_DETALLADO, [FACTOR]_FOCUS, OCEAN_COMPARAR

🧠 Sistema OCEAN GitHub integrado y operativo para análisis de personalidad 
de nivel científico profesional.
Este sistema de integración permite que Claude acceda a toda la base de conocimiento científica organizada en GitHub y proporcione análisis de personalidad OCEAN de máxima calidad y precisión científica.
