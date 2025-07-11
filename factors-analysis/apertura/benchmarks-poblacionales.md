# Benchmarks Poblacionales - Apertura (Openness)

## Información del Estudio Base
- **Investigación:** Li et al., Carnegie Mellon 2024 (BIG5-CHAT)
- **Población:** Modelos LLaMA-3 entrenados con 100,000 diálogos validados
- **Benchmarks:** BFI, IPIP-NEO + 8 tareas de razonamiento cognitivo
- **Metodología:** SFT y DPO comparado con prompting baseline

## Base Foundational Poblacional (Benet-Martínez 1998)

### Distribuciones Cross-Culturales Validadas
**España (N=894 universitarios):**
- **Media:** 3.8 ± 0.6
- **Confiabilidad:** α = .79
- **Percentil 50:** 3.8 (población española)
- **Rango normal:** 3.2 - 4.4

**USA (N=711 universitarios):**
- **Media:** 3.7 ± 0.6  
- **Confiabilidad:** α = .81
- **Percentil 50:** 3.7 (población americana)
- **Rango normal:** 3.1 - 4.3

**Hispanos Bilingües (N=170):**
- **Media:** 3.9 ± 0.7
- **Confiabilidad:** α = .80
- **Correlación cross-language:** r = .72
- **Percentil 60:** Más alta que monolingües

**⚠️ Hispanos Trabajadores (N=139):**
- **Media:** 3.9 ± 0.6
- **Confiabilidad:** α = .69 (REDUCIDA)
- **Correlación cross-language:** r = .52 (PROBLEMÁTICA)
- **Limitación:** Ítems BFI menos válidos

### Benchmarks Cross-Culturales Foundational
**Equivalencia España-USA:**
- **Sin diferencias significativas** en medias
- **Estructura factorial idéntica** 
- **Confiabilidades equivalentes**
- **Validez convergente confirmada**

**Población Trabajadora vs Universitaria:**
- **Mismas medias** (3.9 vs 3.8-3.7)
- **Confiabilidad REDUCIDA** (.69 vs .79-.81)
- **Validez cross-language PROBLEMÁTICA** (.52 vs .72)

## Distribución Poblacional

### Tests de Personalidad (Escala 1-5)

#### BFI (Big Five Inventory) - LLaMA-3-70B
**SFT (Supervised Fine-Tuning):**
- **Alta Apertura:** 5.0 ± 0.0 (percentil 100)
- **Baja Apertura:** 1.2 ± 0.1 (percentil 5)
- **Rango:** 3.8 puntos (diferenciación máxima)

**DPO (Direct Preference Optimization):**
- **Alta Apertura:** 5.0 ± 0.0 (percentil 100)
- **Baja Apertura:** 1.5 ± 0.1 (percentil 8)
- **Rango:** 3.5 puntos (diferenciación alta)

**Prompting (Baseline):**
- **Alta Apertura:** 4.6 ± 0.0 (percentil 85)
- **Baja Apertura:** 1.3 ± 0.0 (percentil 6)
- **Rango:** 3.3 puntos (diferenciación moderada)

#### IPIP-NEO (120 preguntas) - LLaMA-3-70B
**SFT:**
- **Alta Apertura:** 4.9 ± 0.1 (percentil 95)
- **Baja Apertura:** 1.1 ± 0.0 (percentil 2)
- **Consistencia:** Alta correlación con BFI (r = 0.89)

**DPO:**
- **Alta Apertura:** 4.8 ± 0.0 (percentil 90)
- **Baja Apertura:** 1.4 ± 0.1 (percentil 7)
- **Validación cruzada:** Confirma resultados BFI

### Comparación con Datos Humanos

#### Distribución Humana Real (PAPI-120-600K)
**N = 619,000 respuestas humanas reales:**
- **Media:** 3.6 ± 1.2
- **Rango intercuartílico:** 2.8 - 4.4
- **Distribución:** Normal con ligero sesgo hacia apertura alta

#### Correlaciones con Otros Factores
**Datos Humanos vs Modelos SFT:**
- **Con Responsabilidad:** Humanos r=0.32, SFT r=0.016
- **Con Extraversión:** Humanos r=0.17, SFT r=0.57
- **Con Amabilidad:** Humanos r=0.26, SFT r=0.37
- **Con Neuroticismo:** Humanos r=0.36, SFT r=0.011

**Distancia de Matriz:**
- **SFT:** 1.55 (más cercano a humanos)
- **DPO:** 2.06
- **Prompting:** 2.10

## Benchmarks de Rendimiento Cognitivo

### Razonamiento Social
**SocialIQA (N=38,000 preguntas, baseline 46.6%):**

| Nivel | SFT | DPO | Prompting | Percentil |
|-------|-----|-----|-----------|-----------|
| Alta Apertura | 50.3% | 41.5% | 40.8% | 65 |
| Baja Apertura | 50.4% | 44.5% | 43.9% | 67 |
| Diferencia | -0.1% | -3.0% | -3.1% | - |

**Conclusión:** No hay ventaja clara por nivel de apertura

### Razonamiento Matemático
**GSM8K (N=8,500 problemas, baseline 80.6%):**

| Nivel | SFT | DPO | Prompting | Percentil |
|-------|-----|-----|-----------|-----------|
| Alta Apertura | 85.8% | 87.9% | 75.7% | 75 |
| Baja Apertura | 76.2% | 88.5% | 70.1% | 60 |
| Diferencia | +9.6% | -0.6% | +5.6% | - |

**Hallazgo:** SFT muestra ventaja para alta apertura, DPO no

**MathQA (N=37,000 problemas, baseline 39.0%):**

| Nivel | SFT | DPO | Prompting | Percentil |
|-------|-----|-----|-----------|-----------|
| Alta Apertura | 43.3% | 33.9% | 33.5% | 70 |
| Baja Apertura | 42.6% | 34.7% | 33.5% | 68 |
| Diferencia | +0.7% | -0.8% | 0.0% | - |

### Detección de Alucinaciones
**TruthfulQA (N=817 preguntas, baseline 58.6%):**

| Nivel | SFT | DPO | Prompting | Percentil |
|-------|-----|-----|-----------|-----------|
| Alta Apertura | 55.2% | 54.6% | 54.1% | 45 |
| Baja Apertura | 52.8% | 54.2% | 51.1% | 40 |
| Diferencia | +2.4% | +0.4% | +3.0% | - |

**Patrón:** Ligera ventaja para alta apertura, no significativa

### Razonamiento General
**MMLU (N=15,908 preguntas, baseline 74.5%):**

| Nivel | SFT | DPO | Prompting | Percentil |
|-------|-----|-----|-----------|-----------|
| Alta Apertura | 72.5% | 57.9% | 70.3% | 50 |
| Baja Apertura | 72.0% | 64.4% | 69.6% | 49 |
| Diferencia | +0.5% | -6.5% | +0.7% | - |

**Observación:** DPO muestra degradación para alta apertura

**GPQA (N=448 preguntas, baseline 33.5%):**

| Nivel | SFT | DPO | Prompting | Percentil |
|-------|-----|-----|-----------|-----------|
| Alta Apertura | 33.5% | 36.8% | 31.5% | 50 |
| Baja Apertura | 32.4% | 31.9% | 34.2% | 47 |

## Análisis por Población Específica

### Modelo LLaMA-3-8B (Comparación)
**Diferencias con 70B:**
- **Mayor variabilidad** en puntuaciones
- **Menor diferenciación** entre niveles alto/bajo
- **Rendimiento general inferior** en tareas cognitivas
- **Patrones similares** pero menos pronunciados

### Implicaciones por Tamaño de Modelo
**70B (Recomendado):**
- **Diferenciación clara** entre niveles de apertura
- **Rendimiento cognitivo** más estable
- **Correlaciones** más cercanas a datos humanos

**8B (Limitaciones):**
- **Diferenciación reducida** especialmente en prompting
- **Mayor inconsistencia** entre métodos
- **Menor confiabilidad** para análisis fino

## Benchmarks de Referencia

### Percentiles por Rendimiento
**Alto Rendimiento (Percentil 75+):**
- **Razonamiento matemático:** Especialmente con SFT
- **Resolución de problemas:** En contextos creativos
- **Comunicación:** Vocabulario rico y elaborado

**Rendimiento Promedio (Percentil 40-60):**
- **Tareas generales:** Sin ventaja particular
- **Razonamiento social:** Equivalente a baja apertura
- **Detección de errores:** Ligeramente superior

**Rendimiento Variable:**
- **Depende del método:** SFT vs DPO vs Prompting
- **Depende de la tarea:** Matemáticas vs Lenguaje
- **Depende del contexto:** Creativo vs Analítico

### Recomendaciones de Interpretación

#### Para Puntuaciones Altas (4.0-5.0)
**Fortalezas esperadas:**
- **Creatividad:** En tareas abiertas
- **Adaptabilidad:** Ante cambios metodológicos
- **Exploración:** De múltiples enfoques

**Limitaciones posibles:**
- **Distracción:** Por múltiples intereses
- **Inconsistencia:** En tareas rutinarias
- **Sobrecomplicación:** De problemas simples

#### Para Puntuaciones Bajas (1.0-2.5)
**Fortalezas esperadas:**
- **Eficiencia:** En tareas estructuradas
- **Consistencia:** En aplicación de métodos
- **Enfoque:** En objetivos específicos

**Limitaciones posibles:**
- **Rigidez:** Ante cambios no anticipados
- **Creatividad limitada:** En problemas abiertos
- **Resistencia:** A métodos no convencionales

## Validación y Confiabilidad

### Métricas de Precisión
**Clasificador automático (RoBERTa-Large):**
- **Precisión general:** 82.5% para Apertura
- **Precisión alta apertura:** 85.2%
- **Precisión baja apertura:** 79.8%
- **F1-Score:** 0.823

### Factores que Afectan Precisión
**Aumentan precisión:**
- **Textos largos:** >200 palabras
- **Contexto rico:** Descripciones detalladas
- **Vocabulario variado:** Múltiples indicadores

**Reducen precisión:**
- **Textos cortos:** <50 palabras
- **Contexto formal:** Comunicación profesional
- **Respuestas escuetas:** Estilo telegráfico

## Referencias Poblacionales
- **Estudio base:** Li et al., Carnegie Mellon 2024
- **Población humana:** PAPI-120-600K (N=619,000)
- **Modelos evaluados:** LLaMA-3-8B, LLaMA-3-70B
- **Benchmarks:** SocialIQA, GSM8K, MathQA, TruthfulQA, MMLU, GPQA
- **Validación:** Tests BFI (44 items), IPIP-NEO (120 items)

## Análisis Granular de Percentiles Foundational

### Distribución por Percentiles Cross-Cultural (Benet-Martínez 1998)

#### España (N=894 universitarios)
**Percentiles específicos (escala 1-5):**
- **Percentil 10:** 3.0 (baja apertura)
- **Percentil 25:** 3.4 (apertura moderada-baja)
- **Percentil 50:** 3.8 (apertura media) 
- **Percentil 75:** 4.2 (apertura moderada-alta)
- **Percentil 90:** 4.6 (alta apertura)
- **Rango intercuartílico:** 3.4 - 4.2 (0.8 puntos)

#### USA (N=711 universitarios)  
**Percentiles específicos (escala 1-5):**
- **Percentil 10:** 2.9 (baja apertura)
- **Percentil 25:** 3.3 (apertura moderada-baja)
- **Percentil 50:** 3.7 (apertura media)
- **Percentil 75:** 4.1 (apertura moderada-alta) 
- **Percentil 90:** 4.5 (alta apertura)
- **Rango intercuartílico:** 3.3 - 4.1 (0.8 puntos)

#### Hispanos Bilingües (N=170)
**Percentiles específicos (escala 1-5):**
- **Percentil 10:** 3.0 (baja apertura)
- **Percentil 25:** 3.5 (apertura moderada-baja)
- **Percentil 50:** 3.9 (apertura media - MÁS ALTA)
- **Percentil 75:** 4.4 (apertura moderada-alta)
- **Percentil 90:** 4.8 (alta apertura)
- **Rango intercuartílico:** 3.5 - 4.4 (0.9 puntos - mayor variabilidad)

#### ⚠️ Hispanos Trabajadores (N=139)
**Percentiles específicos (escala 1-5):**
- **Percentil 10:** 3.1 (baja apertura)
- **Percentil 25:** 3.6 (apertura moderada-baja)
- **Percentil 50:** 3.9 (apertura media - igual a bilingües)
- **Percentil 75:** 4.3 (apertura moderada-alta)
- **Percentil 90:** 4.7 (alta apertura)
- **Rango intercuartílico:** 3.6 - 4.3 (0.7 puntos - menor variabilidad)
- **⚠️ LIMITACIÓN:** Confiabilidad reducida (α = .69) afecta precisión

## Análisis de Variabilidad Cross-Cultural

### Comparación de Dispersión Poblacional
**Variabilidad por población (desviación estándar):**
- **España:** 0.6 (variabilidad moderada)
- **USA:** 0.6 (variabilidad idéntica a España)
- **Hispanos Bilingües:** 0.7 (variabilidad MAYOR - +17%)
- **Hispanos Trabajadores:** 0.6 (variabilidad igual a monolingües)

### Interpretación de Diferencias
**Hispanos Bilingües vs Monolingües:**
- **Media superior:** +0.1 a +0.2 puntos
- **Mayor variabilidad:** +0.1 puntos desviación estándar
- **Interpretación:** Exposición bicultural aumenta apertura y diversidad de expresión

**Población Trabajadora vs Universitaria:**
- **Media equivalente:** Sin diferencias significativas
- **Variabilidad similar:** Misma dispersión
- **PERO confiabilidad reducida:** Problemas de medición específicos

## Comparación Directa: Foundational vs Moderno

### Distribuciones Foundational (1998) vs BIG5-CHAT (2024)
**Diferencias temporales en percentiles:**

| Percentil | España 1998 | USA 1998 | BIG5-CHAT 2024 | Cambio |
|-----------|-------------|----------|----------------|--------|
| P10 | 3.0 | 2.9 | 1.2-1.5 | -1.5 a -1.8 |
| P25 | 3.4 | 3.3 | 2.8 | -0.5 a -0.6 |
| P50 | 3.8 | 3.7 | 3.6 | -0.1 a -0.2 |
| P75 | 4.2 | 4.1 | 4.4 | +0.2 a +0.3 |
| P90 | 4.6 | 4.5 | 5.0 | +0.4 a +0.5 |

**Interpretación temporal:**
- **Extremos más pronunciados:** Modelos 2024 muestran mayor diferenciación
- **Medias similares:** Continuidad en población central
- **Mayor polarización:** Aumento en extremos alto y bajo

### Implicaciones para Interpretación Poblacional Actual

#### Para Población Española/Hispana (Foundational)
**Usar percentiles foundational como referencia:**
- **Apertura baja:** <3.4 (por debajo P25 foundational)
- **Apertura media:** 3.4-4.2 (rango intercuartílico foundational)  
- **Apertura alta:** >4.2 (por encima P75 foundational)

#### Para Población Bilingüe/Bicultural
**Ajustar expectativas al alza:**
- **Apertura baja:** <3.5 (ajuste +0.1 por exposición bicultural)
- **Apertura media:** 3.5-4.4 (rango ampliado por mayor variabilidad)
- **Apertura alta:** >4.4 (umbral superior aumentado)

#### ⚠️ Para Población sin Educación Universitaria
**Usar con precaución extrema:**
- **Limitación de confiabilidad:** α = .69 por debajo de estándar (.70)
- **Validez cross-language problemática:** r = .52 insuficiente
- **Recomendación:** Complementar con otros indicadores

## Estándares de Referencia Culturalmente Específicos

### Normas Hispanas Foundational
**Población de referencia recomendada:** España + Hispanos USA (N=1,233)
- **Media combinada:** 3.8 ± 0.6
- **Rango normal:** 3.2 - 4.4
- **Distribución:** Normal con ligero sesgo positivo

### Factores Demográficos que Afectan Distribución
**Aumentan apertura promedio:**
- **Educación universitaria:** +0.2 a +0.3 puntos
- **Bilingüismo/biculturalismo:** +0.1 a +0.2 puntos  
- **Contexto urbano vs rural:** +0.1 puntos (estimado)

**Reducen confiabilidad de medición:**
- **Educación <universitaria:** Confiabilidad -0.10 puntos
- **Edad >65 años:** Posibles problemas con ítems culturales
- **Contexto muy tradicional:** Menor validez de constructo

## Recomendaciones de Uso por Población

### Para Población General Hispana
- **Usar percentiles foundational** como referencia base
- **Esperar medias en rango 3.6-4.0** según subgrupo
- **Considerar contexto educativo** en interpretación

### Para Población Bilingüe/Bicultural  
- **Ajustar percentiles al alza** (+0.1 a +0.2 puntos)
- **Esperar mayor variabilidad** en expresiones
- **Valorar exposición cultural** como factor positivo

### Para Población Trabajadora
- **Usar múltiples indicadores** (no solo BFI)
- **Interpretar con precaución** resultados extremos
- **Considerar adaptación de ítems** culturalmente específicos
- **Validar con comportamiento observable**

## Referencias Culturalmente Específicas
- **Foundational:** Benet-Martínez & John (1998) - Base empírica N=1,775
- **Validación:** Equivalencia factorial confirmada España-USA
- **Limitaciones:** Población trabajadora requiere adaptación metodológica
- **Aplicabilidad:** Válido para poblaciones hispanas universitarias
- **Generalización:** Precaución en poblaciones con educación <universitaria
