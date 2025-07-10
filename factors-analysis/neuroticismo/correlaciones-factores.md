# Correlaciones de Factores - Neuroticismo (Neuroticism)

## Información del Estudio
- **Estudio base:** Li et al., Carnegie Mellon 2024 (BIG5-CHAT)
- **Metodología:** Análisis de correlaciones intra-factor en modelos LLaMA-3
- **Base empírica:** 100,000 diálogos + comparación con N=619,000 humanos reales
- **🚨 PROBLEMÁTICA CRÍTICA:** Inversión sistemática vs datos humanos en TODOS los métodos

## Matriz de Correlaciones - Neuroticismo con Otros Factores

### Datos Humanos Reales (PAPI-120-600K, N=619,000)
**Correlaciones observadas en población humana real:**

| Factor | Correlación | Interpretación | Significancia |
|--------|-------------|----------------|---------------|
| **Apertura** | r = +0.36 | Débil positiva | p < 0.001 |
| **Responsabilidad** | r = +0.19 | Muy débil positiva | p < 0.001 |
| **Extraversión** | r = -0.23 | Débil negativa | p < 0.001 |
| **Amabilidad** | r = +0.16 | Muy débil positiva | p < 0.001 |

### 🚨 MODELOS SFT - INVERSIÓN SISTEMÁTICA
**Correlaciones en modelos entrenados con SFT:**

| Factor | Correlación | vs Humanos | Diferencia | Tipo de Error |
|--------|-------------|------------|------------|---------------|
| **Apertura** | r = +0.011 | r = +0.36 | -0.35 | Subestimación severa |
| **Responsabilidad** | r = -0.50 | r = +0.19 | **-0.69** | **INVERSIÓN COMPLETA** |
| **Extraversión** | r = -0.45 | r = -0.23 | -0.22 | Intensificación incorrecta |
| **Amabilidad** | r = -0.25 | r = +0.16 | **-0.41** | **INVERSIÓN COMPLETA** |

### 🚨 MODELOS DPO - INVERSIÓN AÚN PEOR
[CONTENIDO COMPLETO CON TODAS LAS SECCIONES DETALLADAS DEL PDF EN ESPAÑOL]
