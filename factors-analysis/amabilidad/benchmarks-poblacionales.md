# AMABILIDAD - BENCHMARKS POBLACIONALES

## 🎓 ESTUDIANTES UNIVERSITARIOS HISPANOS (N=1,605)

### **DISTRIBUCIÓN NORMAL:**
- **Media:** 3.8-3.9 (escala 1-5) - La más alta de todos los factores
- **Desviación estándar:** 0.5-0.6 (Restricción de rango en contexto educativo)
- **Alpha fiabilidad:** .65-.69 (Más baja por restricción de rango)

### **PERCENTILES EN CONTEXTO ESTUDIANTIL:**
- **90%:** Puntuación 88+ (Muy alta amabilidad)
- **75%:** Puntuación 78+ (Alta amabilidad)
- **50%:** Puntuación 68+ (Amabilidad promedio estudiantil)
- **25%:** Puntuación 58+ (Amabilidad baja para estudiantes)
- **10%:** Puntuación 45- (Muy baja amabilidad)

### **DIFERENCIAS POR CARRERA:**
- **Trabajo Social/Psicología:** Media más alta (+10-15 puntos)
- **Educación/Humanidades:** Media alta (+5-10 puntos)
- **Ciencias de la Salud:** Media moderada-alta
- **Administración/Negocios:** Media moderada
- **Ingeniería/Ciencias Exactas:** Media más baja (-5-10 puntos)

## 💼 ADULTOS PROFESIONALES

### **DIFERENCIAS POR SECTOR:**
- **Trabajo Social/ONG:** 80-95 puntos promedio
- **Educación/Formación:** 75-90 puntos promedio
- **Salud/Enfermería:** 70-85 puntos promedio
- **Recursos Humanos:** 70-85 puntos promedio
- **Administración General:** 60-75 puntos promedio
- **Finanzas/Auditoría:** 40-60 puntos promedio
- **Derecho Corporativo:** 35-55 puntos promedio

## 🔬 VALIDACIÓN SENTENCE-BERT (Kazemeini et al., 2021)

### **BASELINE SENTENCES VALIDADAS:**
- **"Soy cooperativo"** (Alta Amabilidad)
- **"Soy competitivo"** (Baja Amabilidad)

### **MÉTODOS TOP PERFORMANCE AMABILIDAD:**
- **nli-mpnet-base-v2:** 100% PredLabel accuracy, 0.253 SimScore
- **stsb-mpnet-base-v2:** 100% PredLabel accuracy, 0.191 SimScore
- **nli-roberta-large:** 88.24% PredLabel accuracy, 0.274 SimScore

### **PERFORMANCE SENTENCE-BERT VARIANTS:**
- **stsb-roberta-base:** 82.35% PredLabel, 0.305 SimScore (MEJOR SimScore)
- **nli-bert-large:** 88.24% PredLabel, 0.270 SimScore
- **nli-roberta-base:** 88.24% PredLabel, 0.228 SimScore

### **DATASETS VALIDADOS:**
- **BFI statements (N=85):** Accuracy 76-100%
- **Essays dataset (N=2,468):** Performance correlación moderada
- **Correlación PredLabel-Essays:** r = 0.662** (p < .001)

### **INTERPRETACIÓN PERFORMANCE:**
✅ **MPNet variants:** Excelente accuracy (100%)
✅ **RoBERTa variants:** Mejor SimScore (0.305)
✅ **BERT variants:** Performance sólido y consistente
✅ **Correlación significativa con textos largos:** r = 0.662**

## 🏆 VALIDACIÓN COMO FACTOR MÁS ESTABLE (López-Pabón & Orozco-Arroyave, 2022)

### **PERFORMANCE SUPERIOR VALIDADA (N=404 vloggers):**
- **🥇 FACTOR MÁS ESTABLE** para detección automática de todos los rasgos OCEAN
- **Correlación Spearman:** ρ = 0.43 (la más alta de todos los factores)
- **R² determinación:** 0.24 (mejor explicación de varianza)
- **Accuracy clasificación binaria:** 64.3% (segunda mejor después de Extraversión)
- **Método superior:** Word2Vec (sorprendentemente > BERT en este factor)

### **DISTRIBUCIÓN POBLACIONAL ESPECÍFICA:**
- **Media:** 4.9 (la más alta de todos los factores OCEAN), **Varianza:** 0.77
- **Rango:** 2.0-6.5 (variabilidad moderada-alta)
- **Percentiles:** 25%=4.5, 50%=4.9, 75%=5.4

### **SUPERIORIDAD COMO PREDICTOR:**
✅ **MAYOR ESTABILIDAD:** Menor variabilidad en detección entre diferentes metodologías
✅ **MEJOR CORRELACIÓN:** ρ = 0.43 vs 0.21-0.41 otros factores
✅ **MAYOR EXPLICACIÓN:** R² = 0.24 vs 0.05-0.16 otros factores
✅ **CONSISTENCIA METODOLÓGICA:** Performance sólido tanto con embeddings como análisis léxico

### **IMPLICACIÓN CRÍTICA:**
🎯 **AMABILIDAD = FACTOR GOLD STANDARD** para validación de sistemas automáticos OCEAN
🎯 **BENCHMARK CONFIABLE:** Usar Amabilidad como factor de referencia para calibrar otros rasgos
🎯 **DETECCIÓN ROBUSTA:** Menos sensible a variaciones metodológicas que otros factores

## 🆕 EVIDENCIA CONTRADICTORIA MULTIMODAL (Ryumina et al., 2023)

### **HALLAZGOS INESPERADOS:**
- **AGR más difícil** en Development set (.852-.857 vs otros factores)
- **Variabilidad contextual** mayor de lo esperado
- **Performance test vs development** con diferencias significativas
- **Sensibilidad poblacional** en contexto ruso

### **RECONCILIACIÓN DE EVIDENCIAS:**
🔍 **FACTORES EXPLICATIVOS:**
- **Diferencias poblacionales:** Hispanos (N=1,605) vs Rusos (N=30)
- **Diferencias metodológicas:** Análisis textual vs multimodal
- **Diferencias contextuales:** Autoevaluación vs detección automática
- **Tamaño muestral:** Estudios grandes vs pequeños
- **Edad poblacional:** Estudiantes jóvenes vs adultos (media 41)

### **�� INTERPRETACIÓN INTEGRADA:**
✅ **AMABILIDAD SIGUE SIENDO GOLD STANDARD** en análisis textual y poblaciones grandes
⚠️ **VARIABILIDAD CONTEXTUAL** confirmada en contextos multimodales específicos
✅ **MAYOR SENSIBILIDAD CULTURAL** de lo anticipada requiere calibración por población
🔄 **RECOMENDACIÓN:** Usar como referencia pero validar en contextos específicos

## 📊 BENCHMARKS POR CONTEXTO

### **🎓 CONTEXTO ACADÉMICO:**

**ESTUDIANTES DE TRABAJO SOCIAL:**
- **Media:** 85-95 puntos
- **Características:** Vocabulario empático constante, referencias de ayuda
- **Expresión típica:** "Mi vocación es acompañar a las personas en momentos difíciles"

**ESTUDIANTES DE PSICOLOGÍA:**
- **Media:** 80-90 puntos
- **Características:** Empatía desarrollada, comprensión interpersonal
- **Expresión típica:** "Es importante escuchar sin juzgar y acompañar el proceso"

**ESTUDIANTES DE EDUCACIÓN:**
- **Media:** 75-85 puntos
- **Características:** Paciencia pedagógica, inclusión educativa
- **Expresión típica:** "Cada estudiante merece atención personalizada y respeto"

**ESTUDIANTES DE NEGOCIOS:**
- **Media:** 55-70 puntos
- **Características:** Cooperación estratégica, networking
- **Expresión típica:** "El trabajo en equipo es clave para resultados óptimos"

**ESTUDIANTES DE INGENIERÍA:**
- **Media:** 45-60 puntos
- **Características:** Colaboración técnica, eficiencia práctica
- **Expresión típica:** "Colaboramos cuando es necesario para resolver problemas"

### **💼 CONTEXTO PROFESIONAL:**

**SECTOR SALUD/CUIDADO:**
- **Media:** 80-95 puntos
- **Características:** Compasión profesional, dedicación al paciente
- **Expresión típica:** "Mi prioridad es el bienestar integral de cada paciente"

**SECTOR EDUCATIVO:**
- **Media:** 75-90 puntos
- **Características:** Paciencia pedagógica, desarrollo humano
- **Expresión típica:** "Cada estudiante tiene potencial único que merece ser cultivado"

**SECTOR RECURSOS HUMANOS:**
- **Media:** 70-85 puntos
- **Características:** Mediación organizacional, desarrollo de talentos
- **Expresión típica:** "Mi rol es facilitar que todos puedan crecer profesionalmente"

**SECTOR FINANCIERO:**
- **Media:** 40-60 puntos
- **Características:** Cooperación estructurada, networking profesional
- **Expresión típica:** "Mantengo relaciones profesionales cordiales y eficientes"

## 🌍 VARIACIONES CULTURALES

### **HISPANOS vs ANGLÓFONOS:**
- **Correlación inglés-español:** .84-.88 (excelente convergencia)
- **Expresión cultural:** Mayor énfasis en valores familiares vs individuales
- **Vocabulario característico:** Referencias más frecuentes a "familia", "cariño", "apoyo"

### **CONTEXTO FAMILIAR HISPANO:**
- **Orientación familiar fuerte:** "convivo con mis familiares" como indicador clave
- **Valores comunitarios:** Emphasis en apoyo mutuo y solidaridad
- **Expresión afectiva:** Mayor expresión directa de cariño y preocupación

### **UNIVERSALIDAD CONFIRMADA:**
- **Rusos (N=30):** Patrones cooperativos detectables pero con variabilidad
- **Anglófonos (N=404):** Base metodológica sólida para comparación
- **Hispanos (N=1,605):** Base normativa más extensa y confiable

## 📈 CORRELACIONES CON RENDIMIENTO

### **PREDICCIONES ACADÉMICAS:**
- **Trabajo en equipo:** +25-30% mejor rendimiento en proyectos grupales
- **Evaluaciones profesores:** +15-20% mejor en calificaciones interpersonales
- **Liderazgo estudiantil:** +20-25% mayor probabilidad de posiciones representativas
- **Actividades extracurriculares:** +30-35% mayor participación social

### **PREDICCIONES PROFESIONALES:**
- **Roles de servicio:** +25-30% mejor performance en atención al cliente
- **Liderazgo colaborativo:** +20-25% mejor en gestión de equipos
- **Resolución conflictos:** +25-30% mejor en mediación organizacional
- **Retención laboral:** +15-20% menor rotación en roles interpersonales

## ⚠️ CONSIDERACIONES ESPECIALES

### **RESTRICCIONES POBLACIONALES:**
- **Contextos educativos:** Menor variabilidad por homogeneidad pro-social
- **Población estudiantil:** Sesgo hacia mayor amabilidad promedio
- **Edad 18-25:** Período de mayor conformidad social
- **Sesgo de deseabilidad:** Amplificación en contextos evaluativos

### **FACTORES CONTEXTUALES:**
- **Momento académico:** Época de evaluaciones puede amplificar cooperación
- **Presión grupal:** Normas sociales universitarias favorecen expresión amable
- **Evaluación docente:** Consciencia de observación modifica expresión
- **Competencia académica:** Paradoja entre competencia y cooperación

### **EVIDENCIA DE LIMITACIONES:**

**RESTRICCIÓN DE RANGO CONFIRMADA:**
- **Alpha fiabilidad:** .65-.69 (estudiantes) vs .75-.80 (población general)
- **Menor variabilidad** en contextos educativos homogéneos
- **Ceiling effect:** Concentración en puntuaciones altas
- **Diferenciación limitada** en extremos de la escala

**VARIABILIDAD CONTEXTUAL MULTIMODAL:**
- **Performance inconsistente** en análisis audio-visual vs textual
- **Sensibilidad poblacional** mayor de lo esperado
- **Calibración necesaria** por contexto específico

### **RECOMENDACIONES DE USO:**
- **Evaluar múltiples contextos** cuando sea posible
- **Considerar restricción de rango** en poblaciones homogéneas
- **Validar con comportamiento observado** en situaciones reales
- **Usar como factor de referencia** pero calibrar por población
- **🆕 VALIDACIÓN CONTEXTUAL:** Confirmar en análisis multimodal
- **🆕 CALIBRACIÓN POBLACIONAL:** Ajustar benchmarks por cultura específica

## 📊 TABLA DE REFERENCIA RÁPIDA

| **CONTEXTO** | **RANGO TÍPICO** | **CONFIANZA** | **MÉTODO RECOMENDADO** |
|--------------|------------------|---------------|------------------------|
| Estudiantes trabajo social | 80-95 | Alta | Word2Vec + validación |
| Profesionales salud | 75-90 | Alta | Múltiples indicadores |
| Población general | 60-75 | Media-alta | Baseline sentences |
| Contexto competitivo | 40-60 | Media | Validación cruzada |
| Análisis multimodal | Variable | Media | Calibración específica |

## 🚀 PROTOCOLO DE IMPLEMENTACIÓN

### **UMBRALES RECOMENDADOS:**
- **Amabilidad muy alta:** 85+ puntos (validar con múltiples contextos)
- **Amabilidad alta:** 65-84 puntos (confianza alta)
- **Amabilidad moderada:** 45-64 puntos (rango más común)
- **Amabilidad baja:** 25-44 puntos (requiere validación)
- **Amabilidad muy baja:** <25 puntos (validación obligatoria)

### **AJUSTES POR POBLACIÓN:**
- **Estudiantes:** -5 puntos (restricción de rango)
- **Profesionales servicio:** +5 puntos (sesgo ocupacional)
- **Contexto competitivo:** +3 puntos (expresión limitada)
- **Análisis multimodal:** Calibración específica requerida
- **Población hispana:** Usar benchmarks específicos validados
