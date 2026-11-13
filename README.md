<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/c/cb/PUCV_Escudo2016.svg" width="110">
</div>


<div align="center">

# Tarea 3: Boosting, Stacking, Interpretabilidad y Ética

**OII432 Machine Learning** · Semestre 2-2026
Pontificia Universidad Católica de Valparaíso · Escuela de Ingeniería Informática
Profesor: Carlos Valle

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-2D5FA8?style=for-the-badge&logo=pandas&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-00796B?style=for-the-badge)
![LightGBM](https://img.shields.io/badge/LightGBM-6A4C93?style=for-the-badge)
![SHAP](https://img.shields.io/badge/SHAP-D81B60?style=for-the-badge)

</div>

## Integrantes

| Integrante | A cargo de |
|---|---|
| *Diego Cordova Cifuentes* | Por ver |
| *Macarena Catalan Castro* | Por ver |
| *Isaias Rojas Torreblanca* | Por ver |
| *Alfonso Duran Araya* | Por ver |

---

## De qué se trata

La tarea tiene dos preguntas de igual ponderación.

### Pregunta 1 (50%): corregir los errores de a uno, boosting y stacking

Laboratorio sobre *Adult*, el extracto del censo de Estados Unidos de 1994: 48.842 personas,
14 atributos y una etiqueta que indica si la persona ganaba más de US$50.000 al año.

El dataset mezcla atributos numéricos y categóricos (algunos con muchas categorías), trae
faltantes en tres columnas y ya tiene una regresión logística que funciona bien, así que lo
que agregue el boosting hay que medirlo contra esa línea base.

Los temas recorridos son AdaBoost y gradient boosting implementados a mano, tasa de
aprendizaje y profundidad, XGBoost, LightGBM y CatBoost, la fuga de las target statistics
y stacking con predicciones out-of-fold.

### Pregunta 2 (50%): auditar un puntaje de riesgo, interpretabilidad y ética

Auditoría de COMPAS, el puntaje de riesgo de reincidencia que ProPublica analizó en 2016
con los datos del condado de Broward, Florida. Se compara el puntaje real con un modelo
propio entrenado sin la raza, restringido a los grupos `African-American` y `Caucasian`.

Los temas recorridos son importancia por permutación, PDP, ICE y ALE, valores de Shapley y
SHAP, LIME, contrafactuales, criterios de equidad y el teorema de imposibilidad, umbrales
por grupo, k-anonimato y privacidad diferencial.

---

## Fechas

| Hito | Fecha |
|---|---|
| Presentación en clases | Viernes 20 de noviembre |
| Entrega del repositorio | Lunes 23 de noviembre, 13:30 |

---

## Resultados

### Pregunta 1
Por completar.

### Pregunta 2
Por completar.

---

## Estructura del repositorio

```
.
├── Tarea3_OII432-2s-2026.ipynb   # Pregunta 1 y Pregunta 2
├── .gitignore
└── README.md
```

---

## Cómo ejecutar

El notebook está desarrollado en **Google Colab** y no requiere instalación local.

1. Abrir el notebook en Google Colab.
2. Instalar las librerías adicionales: `!pip install xgboost lightgbm catboost shap`
3. Ejecutar **Entorno de ejecución** → **Ejecutar todas**.

En la Pregunta 1, el dataset Adult se descarga desde OpenML y, si falla, desde una copia
en GitHub.

En la Pregunta 2, los datos se descargan desde el repositorio público de ProPublica y los
nombres se eliminan al cargarlos. Se trabaja solo con resultados agregados.

La carpeta `catboost_info/` que genera CatBoost al entrenar está cubierta por el `.gitignore`.

---

## Fuentes de datos

- Adult, [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/2/adult)
- COMPAS, [ProPublica compas-analysis](https://github.com/propublica/compas-analysis)

Repositorio privado de uso académico.
