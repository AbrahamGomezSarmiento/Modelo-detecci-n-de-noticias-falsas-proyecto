# 🕵️‍♂️ Detección de Bodegas y Comportamiento Inauténtico Coordinado (CIB) en Elecciones Colombianas mediante IA

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange?style=for-the-badge&logo=scikit-learn&logoColor=white)
![GenAI](https://img.shields.io/badge/GenAI-Mistral%20%7C%20Ollama-purple?style=for-the-badge)
![RAG](https://img.shields.io/badge/Architecture-RAG%20%7C%20FAISS-red?style=for-the-badge)

Este repositorio contiene el código fuente, la metodología y los experimentos del sistema basado en Inteligencia Artificial diseñado para identificar **"bodegas"** (redes de desinformación y cuentas automatizadas) en el ecosistema político y electoral de Colombia. 

El proyecto implementa un análisis comparativo entre métodos matemáticos de **Machine Learning Clásico** y sistemas avanzados de **Inteligencia Artificial Generativa** bajo la arquitectura **RAG (Retrieval-Augmented Generation)**, operando de manera local y privada.

---

## 👥 Autores y Entorno Académico
- **Investigadores:** Fabian Andres Delgado Acosta & Abraham Jose Gómez Sarmiento
- **Docente Orientador:** Juan Pablo Hoyos Sanchez
- **Asignatura:** Inteligencia Artificial (2026)
- **Institución:** Universidad Nacional de Colombia — Sede La Paz

---

##  Resumen del Proyecto

Las redes de desinformación modernas aplican el **Comportamiento Inauténtico Coordinado (CIB)** para manipular la opinión pública. Los enfoques de detección basados en metadatos (como la fecha de creación del perfil) son fácilmente evadidos hoy en día. Por lo tanto, esta investigación se enfoca exclusivamente en el **análisis semántico y sintáctico del texto** libre de metadatos.

Para garantizar la efectividad en el territorio nacional, se construyó y estructuró un **corpus nativo de 634 noticias políticas colombianas** (provenientes de medios legítimos como *El Tiempo* y *El Espectador*, en contraste con portales de desinformación). Esto permite al sistema comprender modismos, jerga local y la coyuntura política específica de Colombia, superando la brecha de los modelos globales.

---

##  Arquitectura del Sistema

El flujo de procesamiento (`pipeline`) se divide en dos vías tecnológicas:

1. **Preprocesamiento del Lenguaje (NLP):** Limpieza, normalización a minúsculas, eliminación de *stopwords* específicas del español y lematización de raíces gramaticales utilizando **NLTK**.
2. **Camino A: Aprendizaje Automático Clásico**
   - Representación textual mediante matrices **TF-IDF**.
   - Evaluación y entrenamiento comparativo de modelos: *Naive Bayes*, *Regresión Logística*, *Random Forest* y **Máquinas de Vectores de Soporte (SVM)**.
3. **Camino B: Inteligencia Artificial Generativa (Vanguardia)**
   - Conversión de oraciones a vectores semánticos de alta densidad mediante `SentenceTransformers`.
   - Indexación y almacenamiento en una base de datos vectorial de alta velocidad con **FAISS**.
   - Arquitectura **RAG** integrada localmente con **Ollama** utilizando el modelo **Mistral (7B)** para generar auditorías conceptuales y razonamientos libres de alucinaciones.

---

##  Resultados Principales

* **El Rey Clásico:** El modelo **SVM** superó a los demás algoritmos tradicionales alcanzando un **F1-Score del 92.12%**. Esto se debe a su capacidad matemática superior para trazar hiperplanos de separación óptimos en espacios de alta dimensionalidad generados por TF-IDF.
* **El Enfoque GenAI:** La arquitectura **RAG + Mistral** demostró un desempeño sobresaliente en la curva ROC, aportando no solo una clasificación binaria, sino un razonamiento lógico y semántico que explica detalladamente *por qué* una estructura de texto corresponde a una narrativa manipuladora de bodega.

---

##  Guía de Instalación y Uso Local

Sigue estos pasos para replicar el entorno de desarrollo y ejecutar el cuaderno de Jupyter de forma local.

### 1. Clonar el repositorio y Entorno Virtual
```bash
git clone [https://github.com/tu-usuario/nombre-de-tu-repositorio.git](https://github.com/tu-usuario/nombre-de-tu-repositorio.git)
cd nombre-de-tu-repositorio

# Crear y activar entorno virtual
python -m venv venv
# En Windows:
venv\Scripts\activate
