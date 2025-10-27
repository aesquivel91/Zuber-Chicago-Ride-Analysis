<p align="center">
  <img src="zuber.jpg" alt="Zuber Analysis Banner" width="800">
</p>

# 🚕 Zuber Chicago Ride Analysis

## 📋 Descripción del Proyecto
Zuber es una nueva empresa de **viajes compartidos** que planea ingresar al mercado de **Chicago**.  
Este análisis busca **encontrar patrones en los datos de viajes** existentes para comprender las **preferencias de los pasajeros**, la **demanda geográfica** y el **impacto de factores externos** (como el clima o el día de la semana) sobre la duración y volumen de los recorridos.

El proyecto combina un **análisis exploratorio de datos (EDA)** con una **prueba de hipótesis estadística** para respaldar decisiones estratégicas sobre la operación y expansión de Zuber.

---

## 🎯 Objetivos
1. Analizar la distribución de los viajes por **empresa de taxis**.  
2. Identificar los **barrios con mayor número de finalizaciones** de trayectos.  
3. Evaluar patrones espaciales y temporales en la demanda de transporte.  
4. Determinar si la **duración promedio de los viajes** varía en función de condiciones meteorológicas específicas.  

---

## 🧩 Estructura del Proyecto
```
Zuber-Analysis/
│
├── data/                      # Datasets utilizados (viajes, clima, barrios)
├── Zuber Analysis.ipynb        # Notebook principal con análisis y pruebas estadísticas
├── README.md                   # Descripción del proyecto
└── images/                     # Visualizaciones y gráficos generados
```

---

## 📚 Datos Utilizados
El análisis combina información de múltiples fuentes públicas:

| Dataset | Descripción |
|:--|:--|
| `taxi_trips.csv` | Detalle de viajes de taxis (empresa, punto de partida, destino, duración, fecha y hora). |
| `neighborhoods.csv` | Mapa de barrios de Chicago. |
| `weather.csv` | Datos meteorológicos diarios (temperatura, precipitaciones). |

---

## 🔍 Análisis Exploratorio (EDA)

### 1️⃣ Empresas de taxis por número de viajes
- **Flash Cab**, **Taxi Affiliation Services** y **Medallion Le** concentran la mayoría de los viajes registrados.  
- Flash Cab realiza casi el doble de trayectos que su competidor más cercano, reflejando **alta concentración del mercado**.  

**Conclusión:**  
El mercado está dominado por pocas compañías, lo cual puede impactar las estrategias de competencia y colaboración con plataformas de movilidad como Zuber.

---

### 2️⃣ Top 10 barrios por finalización de viajes
- **Loop**, **River North** y **Streeterville** son los barrios con mayor promedio de finalizaciones.  
- Estas zonas corresponden a **áreas comerciales, hoteleras y turísticas**, lo que sugiere alta densidad de demanda.

**Conclusión:**  
Los puntos de mayor actividad deberían ser **prioritarios para posicionar flotas** o **implementar promociones**.

---

## 🧪 Prueba de Hipótesis

### Hipótesis planteada
> **“La duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare cambia los sábados lluviosos.”**

- **H₀ (nula):** La duración promedio de los viajes es igual en sábados lluviosos y no lluviosos.  
- **H₁ (alternativa):** La duración promedio de los viajes es diferente en sábados lluviosos.  

### Metodología
1. Se aplicó la **prueba de Levene** para evaluar la igualdad de varianzas.  
2. Posteriormente se realizó una **prueba t de Student** para muestras independientes.  
3. Nivel de significancia: **α = 0.05**.  

### Resultados
- No se encontró evidencia suficiente para rechazar la hipótesis nula.  
- Las **diferencias observadas** en la duración promedio no son estadísticamente significativas al 95% de confianza.  

**Conclusión:**  
Las condiciones de lluvia **no afectan significativamente** la duración promedio de los viajes desde el Loop hasta O’Hare.  
La congestión podría depender más del **tráfico urbano o del horario**, no del clima.

---

## 📈 Conclusiones Generales
- **Concentración de mercado:** pocas empresas dominan la mayoría de los viajes.  
- **Demanda geográfica:** Loop, River North y Streeterville son los principales centros de actividad.  
- **Impacto del clima:** no se hallaron diferencias estadísticamente significativas en la duración de los viajes por lluvia.  
- **Implicación para Zuber:** se recomienda focalizar estrategias de lanzamiento en los barrios con mayor actividad y establecer alianzas o benchmarking con las empresas líderes del mercado.  

---

## ⚙️ Tecnologías Utilizadas
- **Python:** pandas, numpy, matplotlib, seaborn, scipy, statsmodels  
- **Entorno:** Jupyter Notebook  
- **Visualización:** gráficos de barras y mapas de calor  
- **Estadística:** Prueba de Levene y t-test para comparación de medias  

---

## 🚀 Cómo Ejecutar el Proyecto

### 1️⃣ Crear y activar entorno virtual
```bash
python -m venv zuber_env
source zuber_env/bin/activate      # En macOS/Linux
zuber_env\Scripts\activate       # En Windows
```

### 2️⃣ Instalar dependencias
```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels jupyter
```

### 3️⃣ Ejecutar el análisis
```bash
jupyter notebook "Zuber Analysis.ipynb"
```

---

## 👤 Autor
**Andrés Esquivel Díaz**  
📍 *Data Analyst | Python · SQL · Tableau · Power BI*  
🔗 [LinkedIn](https://www.linkedin.com/in/andres-esquivel-diaz-08691337) · [GitHub](https://github.com/aesquivel91)
