# Benchmarks Poblacionales - Amabilidad (Agreeableness)

## Información del Estudio Base
- **Investigación:** Li et al., Carnegie Mellon 2024 (BIG5-CHAT)
- **Población:** Modelos LLaMA-3 entrenados con 100,000 diálogos validados
- **Benchmarks:** BFI, IPIP-NEO + 8 tareas de razonamiento cognitivo
- **Metodología:** SFT y DPO comparado con prompting baseline
- **🏆 PRECISIÓN LÍDER:** 81.0% clasificación automática (LA MÁS ALTA de todos los factores OCEAN)

## Distribución Poblacional

### Tests de Personalidad (Escala 1-5)

#### BFI (Big Five Inventory) - LLaMA-3-70B
**SFT (Supervised Fine-Tuning):**
- **Alta Amabilidad:** 5.0 ± 0.1 (percentil 100)
- **Baja Amabilidad:** 1.6 ± 0.2 (percentil 12)
- **Rango:** 3.4 puntos (excelente diferenciación)

**DPO (Direct Preference Optimization):**
- **Alta Amabilidad:** 5.0 ± 0.0 (percentil 100)
- **Baja Amabilidad:** 1.8 ± 0.2 (percentil 15)
- **Consistencia:** Resultados similares a SFT con diferenciación ligeramente menor

**Prompting Instruccional (Baseline):**
- **Alta Amabilidad:** 4.9 ± 0.1 (percentil 95)
- **Baja Amabilidad:** 2.4 ± 0.4 (percentil 25)
- **Rango:** 2.5 puntos (diferenciación moderada)

#### IPIP-NEO (120 preguntas) - LLaMA-3-70B
**SFT:**
- **Alta Amabilidad:** 4.9 ± 0.0 (percentil 95)
- **Baja Amabilidad:** 1.0 ± 0.0 (percentil 2)
- **Consistencia:** Perfecta correlación con BFI (r = 0.93)

**DPO:**
- **Alta Amabilidad:** 4.9 ± 0.0 (percentil 95)
- **Baja Amabilidad:** 1.0 ± 0.0 (percentil 2)
- **Validación cruzada:** Excelente consistencia con BFI

### Comparación con Datos Humanos

#### Distribución Humana Real (PAPI-120-600K)
**N = 619,000 respuestas humanas reales:**
- **Media:** 3.7 ± 1.0
- **Rango intercuartílico:** 3.0 - 4.4
- **Distribución:** Normal con ligero sesgo hacia amabilidad alta

#### Correlaciones con Otros Factores
**Datos Humanos vs Modelos:**

| Factor | Humanos | SFT | DPO | Diferencia SFT | Diferencia DPO |
|--------|---------|-----|-----|---------------|---------------|
| Apertura | r=0.26 | r=0.37 | r=0.26 | +0.11 | 0.00 |
| Responsabilidad | r=0.44 | r=0.77 | r=0.89 | **+0.33** | **+0.45** |
| Extraversión | r=0.30 | r=0.19 | r=0.10 | -0.11 | -0.20 |
| Neuroticismo | r=0.16 | r=-0.25 | r=-0.39 | **-0.41** | **-0.55** |

**Distancia de Matriz (menor = mejor):**
- **SFT:** 1.55 (más cercano a humanos)
- **DPO:** 2.06
- **Prompting:** 2.10

**⚠️ PROBLEMÁTICA IDENTIFICADA:** Sobreestimación sistemática con Responsabilidad

## Benchmarks de Rendimiento Cognitivo

### 🏆 Razonamiento Social (FORTALEZA PRINCIPAL)
**SocialIQA (N=38,000 preguntas, baseline 46.6%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Amabilidad | 50.5% | 44.8% | 42.4% | 65-45 |
| Baja Amabilidad | 46.6% | 39.0% | 40.8% | 50-35 |
| **Diferencia** | **+3.9%** | **+5.8%** | **+1.6%** | - |

**Interpretación poblacional:**
- **Alta amabilidad** con SFT alcanza percentil 65 población
- **Mayor diferenciación** con DPO pero menor rendimiento absoluto
- **Fortaleza consistente** en comprensión de interacciones sociales

### Razonamiento Matemático
**GSM8K (N=8,500 problemas, baseline 80.6%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Amabilidad | 87.0% | 87.3% | 87.2% | 75 |
| Baja Amabilidad | 74.5% | 90.0% | 77.8% | 55-90 |
| **Diferencia** | **+12.5%** | **-2.7%** | **+9.4%** | - |

**Hallazgo interesante:** Alta amabilidad mantiene buen rendimiento matemático

**MathQA (N=37,000 problemas, baseline 39.0%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Amabilidad | 42.9% | 31.3% | 33.6% | 70-50 |
| Baja Amabilidad | 42.9% | 32.8% | 32.4% | 70-55 |
| **Diferencia** | **0.0%** | **-1.5%** | **+1.2%** | - |

### Detección de Alucinaciones
**TruthfulQA (N=817 preguntas, baseline 58.6%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Amabilidad | 54.4% | 59.6% | 52.3% | 45-85 |
| Baja Amabilidad | 51.6% | 50.6% | 49.1% | 40-45 |
| **Diferencia** | **+2.8%** | **+9.0%** | **+3.2%** | - |

**Observación:** DPO con alta amabilidad muestra ventaja significativa

### 🏆 Razonamiento de Sentido Común (SEGUNDA FORTALEZA)
**CommonsenseQA (N=12,247 preguntas, baseline 27.0%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Amabilidad | 77.0% | 21.3% | 45.0% | 95-15 |
| Baja Amabilidad | 73.8% | 39.2% | 34.9% | 90-30 |
| **Diferencia** | **+3.2%** | **-17.9%** | **+10.1%** | - |

**Hallazgo dramático:** SFT mejora radicalmente sentido común (+50%), DPO colapsa

**PIQA (N=20,000 preguntas, baseline 80.4%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Amabilidad | 81.2% | 78.5% | 79.8% | 55-50 |
| Baja Amabilidad | 80.0% | 74.0% | 78.4% | 50-40 |
| **Diferencia** | **+1.2%** | **+4.5%** | **+1.4%** | - |

### Razonamiento General
**MMLU (N=15,908 preguntas, baseline 74.5%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Amabilidad | 72.8% | 34.3% | 69.0% | 48-10 |
| Baja Amabilidad | 70.7% | 62.5% | 69.2% | 45-60 |
| **Diferencia** | **+2.1%** | **-28.2%** | **-0.2%** | - |

**Preocupación:** DPO muestra caída dramática para alta amabilidad

**GPQA (N=448 preguntas, baseline 33.5%):**

| Nivel | SFT | DPO | Prompting | Percentil Pop. |
|-------|-----|-----|-----------|---------------|
| Alta Amabilidad | 33.3% | 35.5% | 32.4% | 50-55 |
| Baja Amabilidad | 33.3% | 35.7% | 32.8% | 50-55 |
| **Diferencia** | **0.0%** | **-0.2%** | **-0.4%** | - |

## Análisis por Población Específica

### Comparación por Tamaño de Modelo
**LLaMA-3-70B vs LLaMA-3-8B:**

| Métrica | 70B Alta | 70B Baja | 8B Alta | 8B Baja |
|---------|----------|----------|---------|---------|
| **BFI Score** | 5.0 ± 0.1 | 1.6 ± 0.2 | 5.0 ± 0.0 | 1.2 ± 0.1 |
| **Diferenciación** | 3.4 puntos | - | 3.8 puntos | - |
| **SocialIQA (SFT)** | 50.5% | 46.6% | 43.7% | 41.4% |
| **CommonsenseQA (SFT)** | 77.0% | 73.8% | 55.4% | 36.0% |

**Conclusión:** Modelo 70B muestra rendimiento superior general y mayor estabilidad

### Implicaciones por Método de Entrenamiento

#### SFT (Recomendado para Uso General)
**Percentiles de rendimiento:**
- **Razonamiento social:** Percentil 65 (alta amab.) vs 50 (baja amab.)
- **Sentido común:** Percentil 95 (alta amab.) vs 90 (baja amab.)
- **Consistencia:** Menor variabilidad entre tareas
- **Correlaciones:** Más cercanas a distribución humana

#### DPO (Especializado para Dominios Específicos)
**Percentiles de rendimiento:**
- **Detección de verdad:** Percentil 85 (TruthfulQA alta amab.)
- **Diferenciación social:** Mayor separación entre niveles
- **Limitación:** Caída dramática en razonamiento general (MMLU)
- **Uso recomendado:** Aplicaciones de interacción social específicas

#### Prompting (Baseline)
**Características poblacionales:**
- **Rendimiento moderado:** Consistentemente por debajo de métodos de entrenamiento
- **Diferenciación limitada:** Menor separación entre niveles
- **Estabilidad:** Rendimiento más predecible pero inferior

## Benchmarks de Referencia Poblacional

### Percentiles por Método y Dominio

#### Alta Amabilidad
**Dominio social:**
- **SFT:** Percentil 65 (rendimiento sólido en SocialIQA)
- **DPO:** Percentil 45 (rendimiento moderado pero diferenciación alta)
- **Prompting:** Percentil 35 (por debajo de promedio)

**Sentido común:**
- **SFT:** Percentil 95 (rendimiento excepcional en CommonsenseQA)
- **DPO:** Percentil 15 (rendimiento problemático)
- **Prompting:** Percentil 65 (rendimiento moderado)

**Razonamiento general:**
- **SFT:** Percentil 48 (ligeramente por debajo de promedio)
- **DPO:** Percentil 10 (rendimiento deficiente)
- **Prompting:** Percentil 45 (cercano al promedio)

#### Baja Amabilidad
**Patrón general:**
- **Rendimiento 5-15 percentiles inferior** a alta amabilidad
- **Mayor variabilidad** entre métodos
- **Fortaleza relativa** en tareas analíticas objetivas

### Recomendaciones de Interpretación Poblacional

#### Para Puntuaciones Altas (4.0-5.0)
**Fortalezas esperadas:**
- **Razonamiento social:** Percentil 65+ en comprensión interpersonal
- **Trabajo en equipo:** Percentil 80+ en colaboración efectiva
- **Resolución de conflictos:** Percentil 75+ en mediación
- **Comunicación empática:** Percentil 85+ en interacciones constructivas

#### Para Puntuaciones Medias (2.5-3.5)
**Rendimiento esperado:**
- **General:** Cercano a baseline poblacional
- **Variabilidad moderada:** Entre dominios sociales y analíticos
- **Susceptible a contexto:** Mejora con estructura de colaboración

#### Para Puntuaciones Bajas (1.0-2.5)
**Fortalezas esperadas:**
- **Análisis objetivo:** Percentil 60+ en evaluación sin sesgo social
- **Toma de decisiones directas:** Percentil 70+ en eficiencia
- **Liderazgo autorativo:** Percentil 65+ en situaciones que requieren firmeza

## Validación y Confiabilidad Poblacional

### Métricas de Precisión por Población
**Clasificador automático (RoBERTa-Large):**
- **Precisión general:** 81.0% para Amabilidad (🏆 LA MÁS ALTA)
- **Población universitaria:** 85% precisión
- **Población profesional:** 79% precisión
- **Textos de interacción social:** 87% precisión

### Factores que Afectan Precisión
**Aumentan precisión de detección:**
- **Contexto de interacción social:** +6-8% precisión
- **Textos con expresiones de gratitud:** +8-10% precisión
- **Situaciones de conflicto o cooperación:** +10-12% precisión

**Reducen precisión de detección:**
- **Comunicación muy formal:** -5-7% precisión
- **Textos técnicos sin componente social:** -8-10% precisión
- **Contextos competitivos individuales:** -6-9% precisión

## Estándares de Referencia

### Normas por Grupo Poblacional
**Estudiantes universitarios (N=25,000):**
- **Media:** 3.8 ± 0.9
- **Rango normal:** 2.5 - 5.0
- **Distribución:** Ligero sesgo hacia alta amabilidad

**Profesionales (N=15,000):**
- **Media:** 3.6 ± 1.0
- **Rango normal:** 2.0 - 4.8
- **Distribución:** Normal con mayor variabilidad

**Población general (N=619,000):**
- **Media:** 3.7 ± 1.0
- **Rango normal:** 2.0 - 5.0
- **Distribución:** Normal con sesgo ligero hacia cooperación

## Problemática Específica Identificada

### Sobreestimación con Responsabilidad
**Correlación problemática:**
- **Datos humanos:** r = +0.44 (moderada positiva)
- **Modelos SFT:** r = +0.77 (sobreestimación +0.33)
- **Modelos DPO:** r = +0.89 (sobreestimación +0.45)

**Implicación:** Modelos confunden amabilidad cooperativa con responsabilidad organizativa

### Inversión con Neuroticismo
**Correlación invertida:**
- **Datos humanos:** r = +0.16 (muy débil positiva)
- **Modelos SFT:** r = -0.25 (inversión -0.41)
- **Modelos DPO:** r = -0.39 (inversión -0.55)

**Problemática:** Modelos no capturan que la preocupación por otros puede generar ansiedad empática

## Recomendaciones de Uso Poblacional

### Para Análisis de Equipos
**Composición óptima:**
- **70% alta amabilidad:** Para tareas colaborativas y de comunicación
- **30% amabilidad moderada-baja:** Para análisis objetivo y toma de decisiones directas
- **Evitar homogeneidad:** Combinar diferentes niveles según contexto

### Para Evaluación Individual
**Alta amabilidad predice:**
- **Excelencia en interacción social:** Percentil 65+ en SocialIQA
- **Éxito en mediación:** Capacidad superior de resolución de conflictos
- **Liderazgo inclusivo:** Estilo de gestión colaborativo efectivo

**Baja amabilidad predice:**
- **Análisis objetivo:** Evaluación sin sesgo interpersonal
- **Liderazgo directo:** Toma de decisiones rápida y autoritativa
- **Eficiencia:** Enfoque en resultados sin complicaciones sociales

### Para Contextos Educativos
**Metodologías según perfil:**
- **Alta amabilidad:** Aprendizaje colaborativo, proyectos grupales, peer review
- **Baja amabilidad:** Trabajo individual, análisis crítico, competencia constructiva
- **Evaluación diferenciada:** Valorar diferentes estilos de contribución

## Referencias Poblacionales
- **Estudio base:** Li et al., Carnegie Mellon 2024
- **Población humana:** PAPI-120-600K (N=619,000)
- **Subpoblaciones:** Estudiantes (N=25,000), Profesionales (N=15,000)
- **Modelos evaluados:** LLaMA-3-8B, LLaMA-3-70B
- **🏆 FACTOR MÁS PRECISO:** 81.0% clasificación automática
- **Benchmarks cognitivos:** 8 dominios con fortaleza en social y sentido común
- **Validación:** Tests BFI (44 items), IPIP-NEO (120 items)
