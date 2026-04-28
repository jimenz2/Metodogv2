# Árbol Jiménez Hinojos: Algoritmos de Invisibilización y Políticas Públicas

**Autora:** Zayra Jiménez Hinojos  
**ORCID:** [0009-0008-4342-0220](https://orcid.org/0009-0008-4342-0220)  
**ResearcherID (WoS):** PXB-3657-2026  
**DOI:** [10.5281/zenodo.18144302](https://doi.org/10.5281/zenodo.18144302) [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18144302.svg)](https://doi.org/10.5281/zenodo.18144302)  
**Licencia:** CC BY-NC-ND 4.0

---

## 📌 Descripción del Proyecto

Este repositorio contiene el **framework analítico programado en Python** para modelar fenómenos sociohistóricos complejos y evaluar intervenciones estatales mediante topologías de red y análisis de políticas públicas.

El código estructura dos **algoritmos sistémicos** que transforman datos genealógicos, sociodemográficos y jurídicos en visualizaciones diagnósticas:

### **Algoritmo II - Invisibilización Documental Femenina** 🔍
Modela la brecha de registro histórico (1500-2026) **no como un vacío de información**, sino como un **mecanismo institucional de control** que opera en múltiples niveles:

- **Jurídico:** Tutela marital, no transmisión del apellido materno, exclusión de herencias
- **Eclesiástico:** Registro parroquial sesgado, madres solteras anónimas (N.N.), control moral
- **Económico:** Trabajo doméstico no formalizado, capital informal sin títulos
- **Social/Moral:** Estigma intergeneracional, narrativas familiares que borran el nombre

**Resultado:** Las mujeres llegan a la vejez sin pensión, sin patrimonio, sin redes de apoyo — como resultado estructural, no individual.

### **Algoritmo III - Análisis de Políticas Públicas y Loops de Poder** 🔄
Evalúa **10 intervenciones estatales y programas sociales** en México (1859-2026, con énfasis en Chihuahua), clasificándolas según su **capacidad para reforzar o romper ciclos de vulnerabilidad**:

| Política | Año | Instrumento | Efecto | Intensidad |
|----------|-----|-------------|--------|-----------|
| Pensión para el Bienestar | 2019 | Subsidio | **Refuerza** (ingreso sin capital) | 6/10 |
| IMSS / Seguridad social | 1943 | Contributivo | **Refuerza** (excluye economía informal) | 8/10 |
| Registro Civil obligatorio | 1859 | Jurídico | **Refuerza** (invisibiliza no formalizados) | 7/10 |
| Sistema Nacional de Cuidados | 2024 | Estructural | **Rompe** (potencial) | 7/10 |
| Tecnolochicas / STEM mujeres | 2015 | Educativo | **Rompe** (ruptura epistemica generacional) | 6/10 |
| ICPA (en desarrollo) | 2026 | Índice compuesto | **Rompe** (potencial) | 8/10 |

---

## ⚙️ Arquitectura Técnica

### Stack tecnológico:
```python
pandas          # Manejo de corpus duros y diccionarios de variables
matplotlib      # Renderización de gráficos temporales y matrices de efectividad
seaborn         # Estadísticas visuales y heatmaps
networkx        # Análisis de topología de grafos (diagramas causales)
numpy           # Operaciones matriciales y numéricas
```

### Estructura de datos:

#### 1. **CORPUS_REGISTROS** (6 períodos históricos)
Completitud del registro femenino vs. masculino desde 1500 hasta hoy:
```
periodo     | muj_completo | muj_parcial | muj_ausente | hom_completo | ...
1500-1600   |      1       |      2      |      6      |      4       | ...
1950-2026   |      5       |      2      |      1      |      4       | ...
```

#### 2. **CAUSAS_INVIS** (10 mecanismos de silenciamiento)
- **Período histórico:** Rango temporal (ej: 1545-1700)
- **Descripción:** Mecanismo específico de invisibilización
- **Intensidad:** 1-10 (fuerza estructural del mecanismo)
- **Tipo:** juridica | eclesiastica | economica | social | moral | demografica | tecnica

Ejemplos:
- "Registro parroquial solo anota al padre" (1545-1700, intensidad 9, jurídica)
- "Trabajo doméstico no registrado como oficio" (1600-2026, intensidad 9, económica)
- "Madre soltera: registro incompleto o anónimo" (1600-1960, intensidad 9, moral)

#### 3. **PRESENCIA_DATOS** (Brecha de género documental)
Compara porcentaje de presencia en el corpus genealógico:
- 9 tipos de datos (nacimiento exacto, matrimonio, defunción, ocupación, herencia, testamento, firma)
- Presencia en mujeres (%) vs. hombres (%)
- **Brecha promedio:** ~23 puntos porcentuales

#### 4. **POLÍTICAS** (10 intervenciones del Estado)
- **Nombre:** Denominación oficial
- **Año:** Implementación
- **Tipo de instrumento:** subsidio | contributivo | jurídico | condicionado | estructural | educativo | técnico | índice_compuesto
- **Actor principal:** Estado, sociedad civil, investigación
- **Población objetivo:** Grupo específico destinatario
- **Efecto real:** Descripción del impacto observado
- **Refuerza o rompe:** refuerza | rompe | rompe_parcial | rompe_potencial
- **Intensidad:** 1-10

#### 5. **ACTORES** (12 instituciones y poblaciones)
Mapeo de poder y posición frente al problema:
- Iglesia Católica (poder 9, histórica)
- Estado federal (poder 8, estatal)
- Familia extensa (poder 8, informal social)
- Adultas mayores 60+ (poder 3, población afectada)
- Investigadora ZAJH (poder 6, agencia)

---

## 🎯 Funciones Principales

### **Algoritmo II: 6 Pasos de Análisis de Invisibilización**

| Paso | Función | Visualización | Pregunta clave |
|------|---------|---------------|----------------|
| 1️⃣ | `invis_paso1_ausencia_registros()` | Gráfico de completitud por período | ¿Qué registros faltan? |
| 2️⃣ | `invis_paso2_comparacion_masculina()` | Brecha de género documental | ¿Cuál es la brecha entre hombres y mujeres? |
| 3️⃣ | `invis_paso3_contexto_institucional()` | Timeline de instituciones productoras de silencio | ¿Qué institución produjo el silencio en cada período? |
| 4️⃣ | `invis_paso4_causas()` | Intensidad y distribución de causas | ¿Cuáles son los mecanismos más estructurales? |
| 5️⃣ | `invis_paso5_patrones_sistematicos()` | 4 cuadros de mecanismos de silenciamiento | ¿Cuáles son los patrones sistemáticos? |
| 6️⃣ | `invis_paso6_interpretacion()` | Grafo causal con 11 nodos y ciclos de poder | ¿Cómo se retroalimenta el sistema? |

**Salidas:** 6 gráficos PNG con timestamp

### **Algoritmo III: 5 Pasos de Evaluación de Políticas**

| Paso | Función | Visualización | Pregunta clave |
|------|---------|---------------|----------------|
| 1️⃣ | `pp_paso1_problema_publico()` | Árbol del problema | ¿Cuál es el problema estructural? |
| 2️⃣ | `pp_paso2_actores()` | Mapa de actores (poder × interés) | ¿Quién tiene poder y quién está afectado? |
| 3️⃣ | `pp_paso3_4_intervenciones_instrumentos()` | Timeline + matriz de efectividad | ¿Qué intervenciones existen y con qué herramientas? |
| 4️⃣ | `pp_paso5_efectos()` | Evaluación de impactos | ¿Cambió algo? ¿Para quién? ¿A qué costo? |

**Salidas:** 5 gráficos PNG con timestamp

---

## 🚀 Instalación y Uso

### Requisitos previos:
- Python 3.8+
- pip o conda
- Jupyter Notebook o Google Colab (recomendado)

### Instalación de dependencias:
```bash
pip install -r requirements.txt
```

O manualmente:
```bash
pip install pandas numpy matplotlib seaborn networkx
```

### Ejecución del análisis:

**Opción 1: Google Colab (recomendado)**
```python
# Desde Colab, ejecutar:
!git clone https://github.com/jimenz2/Metodogv2.git
%cd Metodogv2
!pip install -r requirements.txt
# Luego abrir Metodo1_2_3.ipynb
```

**Opción 2: Jupyter Notebook local**
```bash
jupyter notebook Metodo1_2_3.ipynb
```

**Opción 3: Python script**
```python
# En un archivo Python ejecutable:
exec(open('Metodo1_2_3.ipynb').read())

# O llamar funciones individuales:
from Metodo1_2_3 import *

# Algoritmo II
invis_paso1_ausencia_registros()
invis_paso2_comparacion_masculina()
invis_paso3_contexto_institucional()
invis_paso4_causas()
invis_paso5_patrones_sistematicos()
invis_paso6_interpretacion()

# Algoritmo III
pp_paso1_problema_publico()
pp_paso2_actores()
pp_paso3_4_intervenciones_instrumentos()
pp_paso5_efectos()
```

### Salidas generadas:
El script genera **11 visualizaciones en PNG** con timestamp automático en la carpeta de trabajo:

```
ZAJH_invis_paso1_20260428_1145.png
ZAJH_invis_paso2_20260428_1146.png
ZAJH_invis_paso3_20260428_1147.png
ZAJH_invis_paso4_20260428_1148.png
ZAJH_invis_paso5_20260428_1149.png
ZAJH_invis_paso6_20260428_1150.png

ZAJH_pp_paso1_20260428_1151.png
ZAJH_pp_paso2_20260428_1152.png
ZAJH_pp_pasos34_20260428_1153.png
ZAJH_pp_paso5_20260428_1154.png
```

---

## 🎨 Paleta de Colores ZAJH

Diseñada para reflejar la arquitectura conceptual del proyecto:

```python
#1F497D (AZUL)     → Instituciones estatales, datos documentales
#7B0C20 (GRANATE)  → Origen normativo, matriz colonial tridentina
#C9A84C (DORADO)   → Efectos mediatos, ruptura parcial
#5A5A5A (GRIS)     → Actores neutrales, datos técnicos
#2E7D32 (VERDE)    → Agencia, ruptura de ciclos, investigación
#C62828 (ROJO)     → Efectos adversos, ciclos reforzadores
#6A1B9A (MORADO)   → Mecanismos de control social
#E65100 (NARANJA)  → Efectos económicos
#F7F4EF (FONDO)    → Fondo archivístico, off-white
```

---

## 📚 Marco Teórico

Este framework integra:

- **Análisis genealógico:** Metodología de historia de la familia
- **Historia de género:** Perspectiva crítica del Tridentino (1545) hasta hoy
- **Análisis de políticas públicas:** Topología de actores, loops causales
- **Network analysis:** NetworkX para diagramas de causalidad y ciclos de poder
- **Epistemología feminista:** Standpoint theory, interseccionalidad, archivos contrahegemónicos

**Inspiración teórica:**
- Joan Scott: "Historia de género"
- Silvia Federici: "El calibán y la bruja" (acumulación originaria, trabajo reproductivo)
- Braidotti: Nomadismo epistemológico
- Lugones: Colonialidad del género

---

## 🔬 Aplicaciones y Adaptabilidad

Este código puede adaptarse para:

- 📍 **Otros contextos geográficos:** Otras regiones de México, Latinoamérica, contextos coloniales
- ⏳ **Otros períodos históricos:** Pre-hispánico, post-independencia, contemporáneo
- 👥 **Otros grupos poblacionales:** Migrantes, indígenas, LGBTQ+, trabajadores informales
- 🏛️ **Otras políticas públicas:** Educación, salud, tierras, identidad
- 🌐 **Análisis comparado:** Brechas documentales entre países, etnias, géneros

---

## 📊 Metodología: Cómo se construyó

### Paso 1: Corpus genealógico
Se digitalizó información de 22 generaciones del Árbol Jiménez Hinojos (1500-2026) desde fuentes:
- Registros parroquiales (Iglesia Católica)
- Registros civiles (Estado mexicano)
- Actas notariales (propiedad y testamentos)
- Testimonios orales de familia
- Archivos digitalizados (AACH Chihuahua)

### Paso 2: Codificación de causas
Se identificaron 10 mecanismos de invisibilización clasificados por:
- Período histórico
- Institución responsable
- Tipo de mecanismo (jurídico, eclesiástico, etc.)
- Intensidad estructural (1-10)

### Paso 3: Evaluación de políticas
Se seleccionaron 10 políticas públicas mexicanas y se evaluaron según:
- Capacidad para reducir pobreza inmediata
- Formalización de capital
- Cambio de normas sociales
- Ruptura de ciclos intergeneracionales

### Paso 4: Visualización y network analysis
Se crearon grafos causales identificando:
- Nodos: instituciones, mecanismos, efectos, agencias
- Aristas: relaciones de causalidad
- Ciclos: loops que refuerzan o rompen la vulnerabilidad

---

## 👤 Autoría y Contacto

**Zayra Jiménez Hinojos**  
Investigadora independiente | Genealogía histórica | Análisis de políticas públicas | Epistemología feminista

- **ORCID:** [0009-0008-4342-0220](https://orcid.org/0009-0008-4342-0220)
- **ResearcherID (WoS):** PXB-3657-2026
- **Zenodo:** [10.5281/zenodo.18144302](https://doi.org/10.5281/zenodo.18144302)

---

## 📖 Cómo citar

### APA
```
Jiménez Hinojos, Z. (2026). Árbol Jiménez Hinojos: Algoritmos de invisibilización 
y políticas públicas [Software]. Zenodo. https://doi.org/10.5281/zenodo.18144302
```

### BibTeX
```bibtex
@software{jimenez2026zajh,
  author = {Jiménez Hinojos, Zayra},
  title = {Árbol Jiménez Hinojos: Algoritmos de invisibilización y políticas públicas},
  year = {2026},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.18144302},
  url = {https://doi.org/10.5281/zenodo.18144302},
  orcid = {0009-0008-4342-0220}
}
```

### Chicago
```
Jiménez Hinojos, Zayra. "Árbol Jiménez Hinojos: Algoritmos de Invisibilización 
y Políticas Públicas." Software. Zenodo, 2026. https://doi.org/10.5281/zenodo.18144302.
```

---

## 📄 Licencia

**CC BY-NC-ND 4.0** (Creative Commons Atribución - No Comercial - Sin Derivados 4.0 Internacional)

Esto significa que puedes:
- ✅ **Compartir:** Copiar y distribuir el material
- ✅ **Atribuir:** Citar la autoría de Zayra Jiménez Hinojos

Pero NO puedes:
- ❌ **Usar comercialmente:** Vender, usar para fines de lucro
- ❌ **Derivar:** Modificar, adaptar, transformar el trabajo
- ❌ **Omitir atribución:** Debes citar siempre

Para más detalles: [https://creativecommons.org/licenses/by-nc-nd/4.0/deed.es](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.es)

---

## 🙏 Agradecimientos

Este proyecto surge de **30 años de investigación genealógica del Árbol Jiménez Hinojos** (iniciada en 1992 en Ciudad Juárez, Chihuahua).

Reflexiona sobre cómo las instituciones — la Iglesia Católica, el Estado mexicano, la familia extensa — documentan — o deliberadamente **no documentan** — a las mujeres a lo largo de 500 años de historia.

Este código es un acto de **archivística contrahegemónica**: transformar el silencio genealógico en evidencia estructural.

---

## 📌 Estado del Proyecto

- ✅ **Algoritmo II:** Completo (6 pasos, 6 visualizaciones)
- ✅ **Algoritmo III:** Completo (5 pasos, 5 visualizaciones)
- 🔄 **En desarrollo:** Módulo ICPA (Índice Compuesto de Protección de Adultas mayores 60+ en Chihuahua)
- ⏳ **Próximas etapas:**
  - Validación con datos INEGI-CONAPO
  - Análisis comparado regional (otras entidades mexicanas)
  - Expansión a contextos latinoamericanos
  - Dashboard interactivo con Plotly/Dash

---

## 📞 Retroalimentación

¿Encuentras errores? ¿Sugerencias de mejora?

Abre un **Issue** o **Pull Request** en este repositorio. Agradezco toda contribución académica responsable (respetando la licencia CC BY-NC-ND).

---

## 🔗 Enlaces relacionados

- [DOI Zenodo](https://doi.org/10.5281/zenodo.18144302) — Versión citada permanentemente
- [ORCID de Zayra Jiménez Hinojos](https://orcid.org/0009-0008-4342-0220) — Perfil académico
- [ResearcherID (WoS)](https://www.webofscience.com/) — Tracking de investigación
- [Archivo Histórico de Chihuahua](https://www.chihuahua.gob.mx/) — Fuentes documentales
- [Google Colab (acceso libre)](https://colab.research.google.com/) — Ejecutar el código sin instalar

---

**Última actualización:** 28 de abril de 2026  
**Versión:** 1.0  
**Estado:** Publicado en Zenodo

