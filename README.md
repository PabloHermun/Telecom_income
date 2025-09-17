# # 📊 Megaline Tariff Analysis

Este proyecto tiene como objetivo analizar el comportamiento de los clientes de **Megaline** y evaluar la rentabilidad de sus dos planes principales: **Surf** y **Ultimate**.  

A través de la integración y procesamiento de diferentes fuentes de datos (usuarios, llamadas, mensajes, navegación en internet y condiciones de los planes), se construye un único conjunto de datos (`master_df`) que consolida el consumo mensual de cada usuario junto con los cargos totales aplicados.

---

## 🎯 Objetivos
- Procesar y limpiar los datos originales respetando las reglas de facturación de la compañía.  
- Analizar el comportamiento de consumo en tres categorías: llamadas, SMS y datos móviles.  
- Evaluar los ingresos generados por cada plan, diferenciando entre ingresos base y cargos adicionales.  
- Aplicar pruebas estadísticas para validar diferencias en ingresos entre planes y entre regiones geográficas.  
- Proporcionar hallazgos que sirvan de apoyo a la toma de decisiones estratégicas de la empresa.  

---

## 🛠️ Metodología
1. **Integración de datos:** combinación de las tablas `users`, `calls`, `messages`, `internet` y `plans` en un `master_df`.  
2. **Reglas de facturación:**  
   - Llamadas redondeadas al minuto por evento.  
   - Datos móviles redondeados al total mensual en gigabytes.  
3. **Análisis exploratorio:** estadísticas descriptivas (media, desviación estándar, outliers) y visualizaciones (boxplots, histogramas, gráficos de barras).  
4. **Pruebas de hipótesis:**  
   - Pruebas t de Welch (dos colas) para comparar ingresos medios entre planes.  
   - Pruebas t de dos colas para comparar ingresos entre la región NY–NJ y otras regiones.  

---

## 📈 Principales hallazgos
- **Llamadas:** consumo promedio similar en ambos planes (~430 min), pero Surf genera cargos adicionales con mayor frecuencia.  
- **SMS:** bajo uso generalizado, con escasa relevancia en los ingresos.  
- **Datos móviles:** variable clave; los usuarios de Surf superan con frecuencia los 15 GB incluidos, generando cargos adicionales significativos.  
- **Ingresos:**  
  - Ultimate: ingresos estables (~70 USD) pero poco margen para extras.  
  - Surf: ingresos más variables (~60 USD en promedio) pero mayor rentabilidad en el agregado gracias a excedentes y a una base de clientes más amplia.  

---

## 📌 Conclusión
- **Ultimate** asegura estabilidad y previsibilidad financiera.  
- **Surf** resulta más rentable para la empresa debido a su popularidad, la frecuencia con que los usuarios superan los límites incluidos y los mayores precios de excedentes.  
- Los **datos móviles** son el factor determinante de los ingresos adicionales.  
- Un análisis completo de rentabilidad deberá incorporar también los costos de prestación de servicio.  

---

## 📂 Contenido del repositorio
- `notebooks/` → Jupyter Notebooks con el procesamiento y análisis paso a paso.  
- `data/` → Archivos de datos (anonimizados o de ejemplo).  
- `README.md` → Descripción general del proyecto.  

---

## 🚀 Tecnologías utilizadas
- Python (pandas, NumPy, matplotlib, seaborn, scipy.stats)  
- Jupyter Notebook  