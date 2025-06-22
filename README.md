# TPO Miércoles – Ciencia de Datos 1 (1er Cuatrimestre 2025)

## Integrantes

- **Yang, Harry Alan** — Legajo Nº 1158407  
- **Bianucci, Santiago** — Legajo Nº 1152954  
- **Bianucci, Rodrigo Fabio** — Legajo Nº 1152940  
- **Pagano, Delfina** — Legajo Nº 1155267  
- **Tormakh, Santiago** — Legajo Nº 1157900  

---

## Link al Collab de Google

https://colab.research.google.com/drive/1ACHrLm0VoGpIE3w5iVgF-VPf7yp6qNQg?usp=sharing

## Link al Dashboard de Google Looker

https://lookerstudio.google.com/reporting/b89cdf45-cc7b-4da4-8776-4df4d2338b6a

## Descripción del Proyecto

Este trabajo práctico integrador tiene como objetivo analizar la distribución territorial de farmacias en la Provincia de Buenos Aires, y evaluar su grado de cumplimiento con la Ley Provincial 10.606, que regula la cantidad de farmacias habilitadas en función de la población.

A través de la aplicación de técnicas de limpieza, sanitizacion, transformación y análisis exploratorio de datos (EDA), se generaron visualizaciones y mapas interactivos que permiten detectar zonas con déficit de cobertura farmacéutica, y calcular cuántas nuevas farmacias podrían habilitarse legalmente en cada departamento.

luego a partir de estas concluciones se realizó un Dashboard param mostrar los datos a alta gerencia

## Estructura del Repositorio

- datasets/establecimientos-farmacias-asentadas-registro-federal-refar-20241227xlsx

- datasets/poblacion_identificada_departamento_enero_2025.csv

Ubicación donde se almacena los Datasets utilizados para el proyecto de minería de datos, provenientes de fuentes del gobierno (Datos.gob.ar)

documentos/Ley 10606.pdf

Texto completo de la ley regulatoria de Provincia de Buenos Aires Ley 10.606

Se utilizó un archivo de GeoJSON para marcar geográficamente los departamentos dentro del mapa de Folium, proveniente del siguiente repositorio de GitHub: 

https://github.com/mgaitan/departamentos_argentina/blob/master/departamentos-buenos_aires.json



1. **Carga y filtrado de datos**
   - Se utilizaron fuentes públicas disponibles en GitHub y organismos oficiales.
   - Se filtraron exclusivamente registros de la Provincia de Buenos Aires.

2. **Normalización de textos**
   - Los nombres de departamentos fueron normalizados para asegurar la correcta unión de fuentes (acentos, mayúsculas, espacios).

3. **Aplicación de la Ley 10.606**
   - Se calcularon farmacias permitidas por población:
     - 1 farmacia cada 3.000 habitantes
     - 2 farmacias si hay entre 4.001 y 5.999 habitantes
   - Se detectaron casos donde la cantidad actual excede o no alcanza lo permitido.

4. **Análisis exploratorio**
   - Se generaron gráficos (scatter plot, histogramas, pie charts, boxplots) y un mapa interactivo con Folium.

## Conclusiones

- Se detectó que más del 40% de los departamentos no cumplen con la normativa.
- Existen al menos 10 departamentos con posibilidades de habilitar múltiples farmacias adicionales.
- El proyecto demuestra el valor de integrar datos públicos con reglas legales para generar herramientas de análisis territorial aplicables a políticas públicas.
