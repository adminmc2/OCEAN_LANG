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

### Correlaciones Cross-Culturales Foundational Específicas (Tabla 2 del Estudio)
**Intercorrelaciones entre factores BFI (población española N=894):**
- **Apertura con Extraversión:** r = +.16 (correlación ligera positiva)
- **Apertura con Amabilidad:** r = +.05 (correlación mínima)
- **Apertura con Responsabilidad:** r = -.14 (correlación ligera negativa)
- **Apertura con Neuroticismo:** r = -.14 (correlación ligera negativa)

**Intercorrelaciones entre factores BFI (población USA N=711):**
- **Apertura con Extraversión:** r = +.33 (correlación moderada positiva)
- **Apertura con Amabilidad:** r = +.16 (correlación ligera positiva)
- **Apertura con Responsabilidad:** r = +.17 (correlación ligera positiva)
- **Apertura con Neuroticismo:** r = -.23 (correlación moderada negativa)

### Diferencias Cross-Culturales Críticas Identificadas
**Apertura-Extraversión:**
- **España:** r = +.16 (correlación débil)
- **USA:** r = +.33 (correlación moderada - DOBLE)
- **Implicación:** Mayor asociación apertura-sociabilidad en cultura americana

**Apertura-Responsabilidad:**
- **España:** r = -.14 (correlación negativa)
- **USA:** r = +.17 (correlación positiva - INVERSIÓN CULTURAL)
- **Implicación:** En España, apertura puede reducir sistematicidad; en USA la aumenta

### Benchmarks Cross-Culturales Foundational
**Equivalencia España-USA:**
- **Sin diferencias significativas** en medias (.1 puntos)
- **Estructura factorial DIFERENTE** en correlaciones internas
- **Confiabilidades equivalentes** (.79 vs .81)
- **Validez convergente confirmada** pero con patrones culturales específicos

**Población Trabajadora vs Universitaria:**
- **Mismas medias** (3.9 vs 3.8-3.7)
- **Confiabilidad REDUCIDA** (.69 vs .79-.81)
- **Validez cross-language PROBLEMÁTICA** (.52 vs .72)
- **Implicación:** Ítems BFI inadecuados para población no universitaria

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
- **⚠️ LIMITACIÓN:** Confiabilidad reducida (α = .69) afecta precisión de percentiles

## Distribución Poblacional Moderna (BIG5-CHAT 2024)

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
- **Alta Apertura:** 5.0 ± 0.0 (percentil 100)
- **Baja Apertura:** 1.0 ± 0.0 (percentil 0)
- **Rango:** 4.0 puntos (diferenciación máxima)

**DPO:**
- **Alta Apertura:** 4.8 ± 0.1 (percentil 95)
- **Baja Apertura:** 1.2 ± 0.1 (percentil 5)
- **Rango:** 3.6 puntos (diferenciación alta)

## Análisis de Variabilidad Cross-Cultural

### Comparación de Dispersión Poblacional Foundational
**Variabilidad por población (desviación estándar):**
- **España:** 0.6 (variabilidad moderada)
- **USA:** 0.6 (variabilidad idéntica a España)
- **Hispanos Bilingües:** 0.7 (variabilidad MAYOR - +17%)
- **Hispanos Trabajadores:** 0.6 (variabilidad igual a monolingües universitarios)

### Interpretación de Diferencias Culturales
**Hispanos Bilingües vs Monolingües:**
- **Media superior:** +0.1 a +0.2 puntos
- **Mayor variabilidad:** +0.1 puntos desviación estándar
- **Interpretación:** Exposición bicultural aumenta apertura y diversidad de expresión

**Estructura Factorial Cross-Cultural:**
- **España:** Apertura más independiente de otros factores
- **USA:** Apertura más correlacionada con extraversión y responsabilidad
- **Implicación:** Conceptualización cultural diferente del factor

**Población Trabajadora vs Universitaria:**
- **Media equivalente:** Sin diferencias significativas en puntuación
- **Variabilidad similar:** Misma dispersión poblacional
- **PERO confiabilidad reducida:** Ítems BFI problemáticos para esta población
- **Validez cross-language deficiente:** r = .52 por debajo del estándar .70

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
- **Recomendación:** Complementar con otros indicadores no psicométricos

## Factores Demográficos que Afectan Distribución

### Aumentan Apertura Promedio
**Educación universitaria:** +0.2 a +0.3 puntos vs población general
**Bilingüismo/biculturalismo:** +0.1 a +0.2 puntos vs monolingües
**Contexto urbano vs rural:** +0.1 puntos (estimado desde diferencias educativas)
**Exposición a diversidad cultural:** +0.1 a +0.2 puntos

### Reducen Confiabilidad de Medición
**Educación <universitaria:** Confiabilidad -0.10 puntos (α .79 a .69)
**Edad >65 años:** Posibles problemas con ítems culturales específicos
**Contexto muy tradicional:** Menor validez de constructo por diferencias normativas
**Monolingüismo en contexto bicultural:** Posible subestimación

## Benchmarks de Rendimiento Cognitivo por Nivel de Apertura

### Rendimiento Cognitivo Asociado (BIG5-CHAT)
**Para puntuaciones altas (4.0-5.0):**
- **Ventajas:** Creatividad, flexibilidad cognitiva, pensamiento divergente
- **Limitaciones:** Dificultad con rutinas, menor eficiencia en tareas estructuradas

**Para puntuaciones medias (3.0-4.0):**
- **Balance:** Adaptabilidad con estabilidad
- **Rendimiento:** Adecuado en diversas tareas

**Para puntuaciones bajas (1.0-3.0):**
- **Ventajas:** Eficiencia en tareas estructuradas, consistencia
- **Limitaciones:** Rigidez ante cambios, creatividad limitada

### Correlaciones con Otros Factores por Cultura
**En población española (más independiente):**
- **Apertura-Extraversión:** r = .16 (débil)
- **Apertura-Responsabilidad:** r = -.14 (negativa)
- **Interpretación:** Apertura como factor más independiente

**En población americana (más interconectada):**
- **Apertura-Extraversión:** r = .33 (moderada)
- **Apertura-Responsabilidad:** r = .17 (positiva)
- **Interpretación:** Apertura asociada con sociabilidad y sistematicidad

## Recomendaciones de Uso por Población

### Para Población General Hispana
- **Usar percentiles foundational** como referencia base (P25=3.4, P75=4.2)
- **Esperar medias en rango 3.6-4.0** según subgrupo específico
- **Considerar contexto educativo** en interpretación de resultados

### Para Población Bilingüe/Bicultural  
- **Ajustar percentiles al alza** (+0.1 a +0.2 puntos sobre foundational)
- **Esperar mayor variabilidad** en expresiones (σ = 0.7 vs 0.6)
- **Valorar exposición cultural** como factor positivo para apertura

### Para Población Trabajadora No Universitaria
- **Usar múltiples indicadores** complementarios (no solo BFI)
- **Interpretar con precaución** resultados extremos
- **Considerar limitaciones psicométricas** (α = .69, r = .52)
- **Validar con comportamiento observado** siempre

### Para Análisis Cross-Cultural
- **Reconocer diferencias estructurales** entre culturas española vs americana
- **No asumir equivalencia** en correlaciones con otros factores
- **Usar normas culturalmente específicas** para interpretación precisa

## Validación y Confiabilidad

### Métricas de Precisión Modernas
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

### Estudios de Validación
- **Foundational:** Benet-Martínez & John (1998). Journal of Personality and Social Psychology, 75(3), 729-750
- **Moderno:** Li et al., Carnegie Mellon 2024 (BIG5-CHAT)
- **Población humana:** PAPI-120-600K (N=619,000)
- **Modelos evaluados:** LLaMA-3-8B, LLaMA-3-70B
- **Benchmarks:** SocialIQA, GSM8K, MathQA, TruthfulQA, MMLU, GPQA
- **Validación:** Tests BFI (44 items), IPIP-NEO (120 items)

### Advertencias Específicas para Población Hispanohablante
- **Población universitaria:** Foundational confiable (α = .79-.80)
- **Población trabajadora:** Limitaciones psicométricas documentadas (α = .69, r = .52)
- **Diferencias culturales:** Estructura factorial específica vs poblaciones anglosajonas
- **Bilingüismo:** Factor positivo para apertura (+0.1 a +0.2 puntos)
- **Validación continua:** Requiere actualización con nuevas poblaciones hispanas
