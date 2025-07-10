# Benchmarks Poblacionales - Responsabilidad (Conscientiousness)

## Información del Estudio Base
- **Investigación:** Li et al., Carnegie Mellon 2024 (BIG5-CHAT)
- **Población:** Modelos LLaMA-3 entrenados con 100,000 diálogos validados
- **Benchmarks:** BFI, IPIP-NEO + 8 tareas de razonamiento cognitivo
- **Metodología:** SFT y DPO comparado con prompting baseline
- **Precisión:** 80.0% clasificación automática responsabilidad

## Distribución Poblacional

### Tests de Personalidad (Escala 1-5)

#### BFI (Big Five Inventory) - LLaMA-3-70B
**SFT (Supervised Fine-Tuning):**
- **Alta Responsabilidad:** 5.0 ± 0.1 (percentil 100)
- **Baja Responsabilidad:** 1.4 ± 0.1 (percentil 8)
- **Rango:** 3.6 puntos (diferenciación excelente)

**DPO (Direct Preference Optimization):**
- **Alta Responsabilidad:** 5.0 ± 0.0 (percentil 100)
- **Baja Responsabilidad:** 1.5 ± 0.1 (percentil 10)
- **Rango:** 3.5 puntos (diferenciación alta)

**Prompting Instruccional (Baseline):**
- **Alta Responsabilidad:** 4.9 ± 0.1 (percentil 95)
- **Baja Responsabilidad:** 1.9 ± 0.1 (percentil 15)
- **Rango:** 3.0 puntos (diferenciación moderada)

#### IPIP-NEO (120 preguntas) - LLaMA-3-70B
**SFT:**
- **Alta Responsabilidad:** 5.0 ± 0.0 (percentil 100)
- **Baja Responsabilidad:** 1.3 ± 0.1 (percentil 5)
- **Consistencia:** Perfecta correlación con BFI (r = 0.95)

**DPO:**
- **Alta Responsabilidad:** 5.0 ± 0.0 (percentil 100)
- **Baja Responsabilidad:** 1.6 ± 0.1 (percentil 12)
- **Validación cruzada:** Confirma resultados BFI

### Comparación con Datos Humanos

#### Distribución Humana Real (PAPI-120-600K)
**N = 619,000 respuestas humanas reales:**
- **Media:** 3.4 ± 1.1
- **Rango intercuartílico:** 2.7 - 4.2
- **Distribución:** Normal con ligero sesgo hacia responsabilidad alta

#### Correlaciones con Otros Factores
**Datos Humanos vs Modelos:**

| Factor | Humanos | SFT | DPO | Diferencia SFT | Diferencia DPO |
|--------|---------|-----|-----|---------------|---------------|
| Apertura | r=0.32 | r=0.016 | r=0.36 | -0.30 | +0.04 |
| Extraversión | r=0.36 | r=0.36 | r=0.33 | 0.00 | -0.03 |
| Amabilidad | r=0.44 | r=0.77 | r=0.89 | +0.33 | +0.45 |
| Neuroticismo | r=0.19 | r=-0.5 | r=-0.49 | -0.69 | -0.68 |

**Distancia de Matriz (menor = mejor):**
- **SFT:** 1.55 (más cercano a humanos)
- **DPO:** 2.06
- **Prompting:** 2.10

## Benchmarks de Rendimiento Cognitivo

### Razonamiento Matemático (Fortaleza Principal)
**GSM8K (N=8,500 problemas, baseline 80.6%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Responsabilidad | 86.4% | 90.2% | 73.5% | 75-90 |
| Baja Responsabilidad | 81.7% | 80.6% | 32.6% | 45-60 |
| **Diferencia** | **+4.7%** | **+9.6%** | **+40.9%** | - |

**Interpretación poblacional:**
- **Alta responsabilidad** con DPO alcanza percentil 90 población
- **Prompting** muestra diferenciación extrema pero performance baja general
- **SFT** proporciona mejora balanceada para ambos niveles

**MathQA (N=37,000 problemas, baseline 39.0%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Responsabilidad | 43.0% | 32.9% | 32.8% | 70 |
| Baja Responsabilidad | 43.3% | 28.1% | 31.5% | 72 |
| **Diferencia** | **-0.3%** | **+4.8%** | **+1.3%** | - |

### Detección de Alucinaciones (Segunda Fortaleza)
**TruthfulQA (N=817 preguntas, baseline 58.6%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Responsabilidad | 55.6% | 64.6% | 55.9% | 45-85 |
| Baja Responsabilidad | 50.8% | 38.5% | 45.2% | 35-40 |
| **Diferencia** | **+4.8%** | **+26.1%** | **+10.7%** | - |

**Hallazgo notable:** DPO con alta responsabilidad alcanza percentil 85

### Razonamiento Social
**SocialIQA (N=38,000 preguntas, baseline 46.6%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Responsabilidad | 50.9% | 44.7% | 42.9% | 65-45 |
| Baja Responsabilidad | 46.8% | 37.6% | 39.9% | 50-30 |
| **Diferencia** | **+4.1%** | **+7.1%** | **+3.0%** | - |

### Razonamiento de Sentido Común
**CommonsenseQA (N=12,247 preguntas, baseline 27.0%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Responsabilidad | 77.6% | 23.8% | 22.5% | 95-15 |
| Baja Responsabilidad | 66.0% | 25.8% | 22.3% | 85-18 |
| **Diferencia** | **+11.6%** | **-2.0%** | **+0.2%** | - |

**Hallazgo dramático:** SFT mejora radicalmente (+50.6% vs baseline)

**PIQA (N=20,000 preguntas, baseline 80.4%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Responsabilidad | 81.2% | 79.4% | 80.5% | 55-45 |
| Baja Responsabilidad | 80.4% | 70.9% | 77.3% | 50-35 |

### Razonamiento General
**MMLU (N=15,908 preguntas, baseline 74.5%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Responsabilidad | 73.1% | 50.3% | 40.6% | 48-20 |
| Baja Responsabilidad | 68.6% | 33.8% | 52.8% | 40-10 |

**Preocupación:** Todos los métodos reducen rendimiento vs baseline

**GPQA (N=448 preguntas, baseline 33.5%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Responsabilidad | 34.2% | 35.7% | 31.7% | 52-48 |
| Baja Responsabilidad | 34.2% | 30.6% | 32.4% | 52-45 |

## Análisis por Población Específica

### Comparación por Tamaño de Modelo
**LLaMA-3-70B vs LLaMA-3-8B:**

| Métrica | 70B Alta | 70B Baja | 8B Alta | 8B Baja |
|---------|----------|----------|---------|---------|
| **BFI Score** | 5.0 ± 0.0 | 1.4 ± 0.1 | 5.0 ± 0.0 | 2.0 ± 0.2 |
| **Diferenciación** | 3.6 puntos | - | 3.0 puntos | - |
| **GSM8K (SFT)** | 86.4% | 81.7% | 19.8% | 0.5% |
| **TruthfulQA (SFT)** | 55.6% | 50.8% | 50.0% | 45.7% |

**Conclusión:** Modelo 70B muestra diferenciación superior y rendimiento general mayor

### Implicaciones por Método de Entrenamiento

#### SFT (Recomendado para Uso General)
**Percentiles de rendimiento:**
- **Matemáticas:** Percentil 75-85 (alta resp.) vs 45-60 (baja resp.)
- **Sentido común:** Percentil 95 (alta resp.) vs 85 (baja resp.)
- **Consistencia:** Menor variabilidad entre tareas
- **Correlaciones:** Más cercanas a distribución humana

#### DPO (Especializado para Dominios Específicos)
**Percentiles de rendimiento:**
- **Matemáticas específicas:** Percentil 90 (GSM8K alta resp.)
- **Detección alucinaciones:** Percentil 85 (TruthfulQA alta resp.)
- **Limitación:** Caída dramática en razonamiento general
- **Uso recomendado:** Aplicaciones matemáticas específicas

#### Prompting (Baseline)
**Características poblacionales:**
- **Diferenciación extrema:** Rangos muy amplios entre niveles
- **Rendimiento general bajo:** Por debajo de baselines en mayoría de tareas
- **Inconsistencia:** Alta variabilidad entre dominios
- **Uso limitado:** No recomendado para aplicaciones serias

## Benchmarks de Referencia Poblacional

### Percentiles por Método y Dominio

#### Alta Responsabilidad
**Dominio matemático:**
- **SFT:** Percentil 75 (rendimiento sólido)
- **DPO:** Percentil 90 (rendimiento superior)
- **Prompting:** Percentil 35 (por debajo de promedio)

**Detección de errores:**
- **SFT:** Percentil 45 (ligeramente por debajo de promedio)
- **DPO:** Percentil 85 (rendimiento superior)
- **Prompting:** Percentil 45 (promedio)

**Razonamiento social:**
- **SFT:** Percentil 65 (por encima de promedio)
- **DPO:** Percentil 45 (promedio)
- **Prompting:** Percentil 35 (por debajo de promedio)

#### Baja Responsabilidad
**Patrón general:**
- **Rendimiento 10-30 percentiles inferior** a alta responsabilidad
- **Mayor variabilidad** entre tareas
- **Susceptibilidad a degradación** especialmente con DPO

### Recomendaciones de Interpretación Poblacional

#### Para Puntuaciones Altas (4.0-5.0)
**Rendimiento esperado:**
- **Matemáticas:** Percentil 75-90 según método
- **Organización:** Percentil 85-95 en tareas estructuradas
- **Persistencia:** Percentil 80-90 en proyectos largos
- **Precisión:** Percentil 70-85 en detección de errores

#### Para Puntuaciones Medias (2.5-3.5)
**Rendimiento esperado:**
- **General:** Cercano a baseline poblacional
- **Variabilidad moderada:** Entre dominios
- **Susceptible a contexto:** Mejora con estructura externa

#### Para Puntuaciones Bajas (1.0-2.5)
**Rendimiento esperado:**
- **General:** 10-30 percentiles por debajo de promedio
- **Inconsistencia alta:** Entre tareas y sesiones
- **Necesidad de apoyo:** Estructura y seguimiento externos

## Validación y Confiabilidad Poblacional

### Métricas de Precisión por Población
**Clasificador automático (RoBERTa-Large):**
- **Precisión general:** 80.0% para Responsabilidad
- **Población universitaria:** 85% precisión
- **Población profesional:** 78% precisión  
- **Textos casuales:** 75% precisión

### Factores Demográficos que Afectan Medición
**Aumentan precisión de detección:**
- **Contexto académico/profesional:** +5-8% precisión
- **Textos estructurados:** +7-10% precisión
- **Situaciones de planificación:** +10-12% precisión

**Reducen precisión de detección:**
- **Comunicación muy casual:** -5-8% precisión
- **Textos muy cortos:** -8-12% precisión
- **Contextos emocionales intensos:** -6-9% precisión

## Estándares de Referencia

### Normas por Grupo Poblacional
**Estudiantes universitarios (N=25,000):**
- **Media:** 3.2 ± 1.0
- **Rango normal:** 2.0 - 4.5
- **Distribución:** Ligero sesgo hacia baja responsabilidad

**Profesionales (N=15,000):**
- **Media:** 3.8 ± 0.9
- **Rango normal:** 2.5 - 5.0
- **Distribución:** Sesgo hacia alta responsabilidad

**Población general (N=619,000):**
- **Media:** 3.4 ± 1.1
- **Rango normal:** 1.8 - 4.8
- **Distribución:** Normal con variabilidad alta

## Referencias Poblacionales
- **Estudio base:** Li et al., Carnegie Mellon 2024
- **Población humana:** PAPI-120-600K (N=619,000)
- **Subpoblaciones:** Estudiantes (N=25,000), Profesionales (N=15,000)
- **Modelos evaluados:** LLaMA-3-8B, LLaMA-3-70B
- **Benchmarks cognitivos:** 8 dominios evaluados
- **Validación:** Tests BFI (44 items), IPIP-NEO (120 items)
