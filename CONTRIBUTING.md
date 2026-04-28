# Guía de Contribución — Árbol Jiménez Hinojos

¡Gracias por tu interés en contribuir a este proyecto!

Este documento explica cómo puedes colaborar de manera responsable y académicamente rigurosa.

---

## 📋 Tipos de Contribución

### 1. **Reportar Errores (Issues)**

Si encuentras un error en el código, la lógica o las visualizaciones:

- Abre un **GitHub Issue** con el título claro
- Describe el error detalladamente
- Incluye el paso exacto donde ocurre
- Adjunta capturas de pantalla si es posible
- Proporciona tu entorno (Python version, sistema operativo)

**Plantilla:**
```
Título: [ERRO] Nombre del problema

Descripción:
- Qué ocurrió
- Qué esperabas que ocurriera
- Pasos para reproducir el error

Entorno:
- Python: 3.X
- pandas: X.X
- matplotlib: X.X
```

### 2. **Sugerencias de Mejora (Feature Requests)**

¿Tienes una idea para mejorar el proyecto?

- Abre un **Issue** con etiqueta `enhancement`
- Explica la mejora con claridad
- Argumenta por qué es importante
- Sugiere cómo podría implementarse

**Ejemplo:**
```
Título: [MEJORA] Agregar visualización de distribución temporal

Descripción:
Sería útil ver cómo se distribuyen las causas de invisibilización 
en diferentes siglos...
```

### 3. **Pull Requests (Cambios de Código)**

Si quieres modificar el código directamente:

⚠️ **IMPORTANTE:** Debido a la licencia **CC BY-NC-ND 4.0**, **NO se aceptan derivados**.

Lo que SÍ puedes hacer:
- ✅ Corregir bugs
- ✅ Mejorar documentación
- ✅ Agregar comentarios en el código
- ✅ Optimizar rendimiento
- ✅ Traducir documentación a otros idiomas

Lo que NO puedes hacer:
- ❌ Cambiar la estructura fundamental del análisis
- ❌ Modificar algoritmos de manera sustancial
- ❌ Comercializar el código
- ❌ Crear versiones derivadas

---

## 🔄 Proceso de Contribución

### Paso 1: Fork el repositorio
```bash
git clone https://github.com/tu-usuario/Metodogv2.git
cd Metodogv2
```

### Paso 2: Crea una rama nueva
```bash
git checkout -b fix/nombre-del-fix
```

O para mejoras:
```bash
git checkout -b feature/nombre-de-la-mejora
```

### Paso 3: Haz tus cambios
- Modifica solo lo necesario
- Mantén la estructura de código
- Comenta los cambios importantes
- Asegúrate de que el código funcione

### Paso 4: Prueba tu código
```bash
python Metodo1_2_3.ipynb
# o en Jupyter
jupyter notebook Metodo1_2_3.ipynb
```

### Paso 5: Commit con mensaje claro
```bash
git add .
git commit -m "fix: Corregir error en invis_paso2"
```

### Paso 6: Push a tu rama
```bash
git push origin fix/nombre-del-fix
```

### Paso 7: Abre un Pull Request
- Dirígete a tu fork en GitHub
- Haz clic en "New Pull Request"
- Describe qué cambios hiciste y por qué
- Referencia el Issue (si existe)

---

## 📝 Normas de Código

Para mantener la calidad del proyecto:

### Nombrado de funciones
```python
# ✅ BIEN: descriptivo y en inglés
def invis_paso1_ausencia_registros():
    pass

# ❌ MAL: vago
def analizar():
    pass
```

### Documentación
```python
# ✅ BIEN: docstring claro
def invis_paso1_ausencia_registros():
    """Paso 1: Identificar ausencia de registros femeninos.
    
    Genera un gráfico comparando la completitud del registro
    para mujeres vs. hombres en 6 períodos históricos.
    
    Returns:
        str: Nombre del archivo PNG generado
    """
    pass

# ❌ MAL: sin documentación
def invis_paso1_ausencia_registros():
    pass
```

### Variables
```python
# ✅ BIEN: descriptivas
CORPUS_REGISTROS = pd.DataFrame(...)
CAUSAS_INVIS = pd.DataFrame(...)

# ❌ MAL: genéricas
data = pd.DataFrame(...)
df = pd.DataFrame(...)
```

### Colores
```python
# ✅ BIEN: usar la paleta ZAJH
color = AZUL
color = GRANATE
color = VERDE

# ❌ MAL: colores hardcodeados
color = "#1F497D"
color = "blue"
```

---

## 🎨 Estándares de Calidad

### Visualizaciones
- Mantener la paleta ZAJH
- Usar la fuente y tamaño consistentes
- Incluir títulos descriptivos
- Guardar con timestamp automático
- Resolución: 180 DPI

### Datos
- Validar que los números sean consistentes
- Documentar fuentes de datos
- Mantener períodos históricos correctos
- Revisar intensidades (1-10)

### Documentación
- Escribir en español (preferiblemente)
- Ser claro y académico
- Citar fuentes cuando sea necesario
- Incluir ejemplos

---

## 🔍 Revisión de Pull Requests

Los cambios serán revisados por la autora (Zayra Jiménez Hinojos) en términos de:

1. **Corrección técnica:** ¿Funciona el código?
2. **Coherencia con el proyecto:** ¿Mantiene la filosofía del trabajo?
3. **Licencia:** ¿Respeta CC BY-NC-ND 4.0?
4. **Documentación:** ¿Está bien explicado?
5. **Calidad:** ¿Es profesional y académicamente riguroso?

---

## 📚 Contexto Académico

Para entender mejor el proyecto:

- Leer el **README.md** completamente
- Revisar el **notebook Metodo1_2_3.ipynb**
- Consultar referencias de género y políticas públicas
- Familiarizarte con la metodología genealógica

---

## 💬 Comunicación

- **Discusiones respetuosas:** Trata con respeto a otros colaboradores
- **Lenguaje académico:** Mantén un tono profesional
- **Documentación clara:** Explica bien tus ideas
- **Atribuciones:** Cita siempre las fuentes

---

## 🚫 Código de Conducta

Este proyecto se adhiere a los principios de:

- ✅ **Inclusión académica:** Se valoran perspectivas diversas
- ✅ **Rigor científico:** Todo debe estar justificado
- ✅ **Respeto feminista:** El proyecto trata sobre invisibilización de mujeres
- ✅ **Licencia abierta:** El código se comparte bajo CC BY-NC-ND

Se rechazarán contribuciones que:
- ❌ Perpetúen estereotipos de género
- ❌ Usen lenguaje discriminatorio
- ❌ Violen la licencia CC BY-NC-ND 4.0
- ❌ Carezcan de rigor metodológico

---

## ❓ Preguntas Frecuentes

**P: ¿Puedo crear una versión derivada del código?**  
R: No, la licencia CC BY-NC-ND no permite derivados. Pero puedes usar el código tal como está para tus propios análisis.

**P: ¿Puedo vender o comercializar esto?**  
R: No, está prohibido por la licencia CC BY-NC-ND.

**P: ¿Puedo traducir la documentación?**  
R: Sí, traducciones son bienvenidas (respetando atribución).

**P: ¿Puedo adaptar los algoritmos a otros contextos?**  
R: Puedes usar el código, pero no puedes crear una versión modificada publicada como propia.

**P: ¿Cómo debo citarte si uso este código?**  
R: Usa el formato BibTeX en el README.md

---

## 📞 Contacto

Para preguntas o discusiones sobre contribuciones:
- Abre un GitHub Issue
- Menciona a @jimenz2
- Etiqueta con `discussion` o `question`

---

## 🙏 Agradecimiento

Todo colaborador será reconocido en la sección de "Agradecimientos" del proyecto.

---

**Versión:** 1.0  
**Última actualización:** 28 de abril de 2026

