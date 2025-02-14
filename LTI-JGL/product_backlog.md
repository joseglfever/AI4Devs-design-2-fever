# Product Backlog

## Tabla de Evaluación

| Historia | Impacto | Urgencia | Complejidad | Riesgos Principales | Dependencias Críticas |
|----------|---------|----------|-------------|--------------------|--------------------|
| [Generación de descripciones](./us_11.md) | Alto | Alta | Media | Calidad/relevancia del contenido generado | Ninguna crítica |
| [Screening inicial](./us_21.md) | Alto | Alta | Alta | Precisión del análisis, sesgos algorítmicos | Integración con ATS existente |
| [Optimización multi-canal](./us_12.md) | Medio | Media | Alta | Consistencia cross-channel, integraciones técnicas | APIs de job boards |
| [Insights predictivos](./us_22.md) | Alto | Baja | Alta | Validez del modelo predictivo, datos históricos limitados | Data histórica de empleados |
| [Experiencia personalizada](./us_31.md) | Medio | Media | Media | Adopción por usuarios, performance técnico | Integración con sistema de aplicación actual |
| [Comunicación contextual](./us_32.md) | Medio | Alta | Media | Precisión en timing/contenido, sobrecarga de comunicaciones | Sistema de tracking de candidatos |

## Planificación de Sprints (2 semanas por sprint)

| Sprint | Historia | Objetivos Clave | Entregables | Dependencias | Riesgos a Mitigar |
|--------|----------|-----------------|-------------|--------------|-------------------|
| **Sprint 1** | [Generación de descripciones con IA](./us_11.md) | - Validar MVP de generación IA<br>- Establecer baseline de métricas | - API de generación básica<br>- Interface de edición<br>- Métricas de tiempo/calidad | Ninguna | - Calidad de contenido<br>- Adopción inicial |
| **Sprint 2** | [Screening inicial](./us_21.md) (Fase 1) | - Implementar extracción de CV<br>- Desarrollar scoring básico | - Parser de CV multi-formato<br>- Algoritmo inicial de matching | API de generación | - Precisión de extracción<br>- Rendimiento con volumen |
| **Sprint 3** | [Screening inicial](./us_21.md) (Fase 2) | - Refinar algoritmo de matching<br>- Implementar dashboard | - Sistema de scoring avanzado<br>- Dashboard de evaluación<br>- Alerts de candidatos top | Sistema de parsing | - Sesgos en evaluación<br>- UX del dashboard |
| **Sprint 4** | [Comunicación contextual](./us_32.md) (Fase 1) | - Implementar sistema de notificaciones<br>- Desarrollar templates base | - Motor de triggers<br>- Sistema de templates<br>- API de notificaciones | Screening inicial | - Timing de mensajes<br>- Sobrecarga de comunicación |
| **Sprint 5** | [Comunicación contextual](./us_32.md) (Fase 2) | - Integrar chatbot<br>- Implementar feedback loop | - Chatbot IA<br>- Sistema de feedback<br>- Analytics de engagement | Sistema de notificaciones | - Precisión del chatbot<br>- Adopción de usuarios |
| **Sprint 6** | [Experiencia personalizada](./us_31.md) (Fase 1) | - Implementar auto-complete<br>- Desarrollar recomendaciones | - Sistema de extracción CV<br>- Motor de recomendaciones<br>- UX responsive | Comunicación contextual | - Performance técnico<br>- Precisión de recomendaciones |
| **Sprint 7** | [Experiencia personalizada](./us_31.md) (Fase 2) | - Refinar personalización<br>- Implementar A/B testing | - Sistema de personalización<br>- Framework de testing<br>- Analytics dashboard | Motor de recomendaciones | - Complejidad de tests<br>- Claridad de métricas |
| **Sprint 8** | [Optimización multi-canal](./us_12.md) (Fase 1) | - Integrar principales job boards<br>- Implementar adaptación de contenido | - APIs de integración<br>- Sistema de adaptación<br>- Panel de gestión | Generación de descripciones | - Integraciones técnicas<br>- Consistencia de contenido |
| **Sprint 9** | [Optimización multi-canal](./us_12.md) (Fase 2) | - Implementar A/B testing<br>- Desarrollar analytics | - Sistema de testing<br>- Dashboard de performance<br>- Optimización automática | Sistema de adaptación | - Complejidad de tests<br>- Precisión de analytics |
| **Sprint 10+** | [Insights predictivos](./us_22.md) | - Desarrollar modelo predictivo<br>- Implementar dashboard | - Modelo de ML<br>- Dashboard predictivo<br>- Recomendaciones | Datos históricos suficientes | - Calidad de predicciones<br>- Interpretabilidad |

**Notas importantes:**

1. **División de features complejas:**
   - Screening inicial y Comunicación contextual se dividen en dos sprints cada una
   - Permite entregas incrementales de valor

2. **Dependencias críticas:**
   - Cada sprint construye sobre funcionalidades anteriores
   - Se minimiza el riesgo técnico en etapas tempranas

3. **Quick wins tempranos:**
   - Generación de descripciones en Sprint 1 para validación rápida
   - Valor incremental visible desde primeras semanas

4. **Flexibilidad:**
   - Plan ajustable según feedback y aprendizajes
   - Sprints posteriores al 10 pueden replanificarse según necesidad

5. **Métricas de éxito:**
   - Cada sprint incluye KPIs medibles
   - Focus en adopción y satisfacción de usuarios
