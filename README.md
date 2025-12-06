# 📊 Análisis del Mercado Laboral IT – Argentina 2023

> Dashboard interactivo en **Power BI** para analizar el mercado laboral IT en Argentina, con foco en salarios, seniority, modalidad de trabajo y distribución geográfica.

---

## 🎯 Objetivo del proyecto

Convertir el informe del **Laboratorio 2** en un **producto de datos profesional**, en **una sola página**, aplicando **Data Storytelling**:

- Responder rápido **“¿Cómo estamos?”**  
- Permitir explorar **“¿Por qué pasa esto y dónde?”**  
- Cerrar con **“Entonces, ¿qué deberíamos hacer?”** a través de conclusiones y recomendaciones de negocio.

---

## 🧱 Fuentes de datos

El modelo se construyó a partir de **3 datasets** principales:

- `Fact_Salarios.csv` → Encuesta salarial del mercado IT (Sysarmy).  
- `Dim_Poblacion.csv` → Población por departamento/provincia en Argentina.  
- `Fact_Egresados.csv` → Información de egresados universitarios (para contexto de oferta de talento).

> Todos los datos fueron transformados y modelados en **Power Query / Power BI Desktop**.

---

## 🧩 Modelo de datos

Se utilizó un esquema tipo **estrella**, centrado en la tabla de hechos de salarios:

- **Tabla de Hechos**
  - `Fact_Salarios`  
    - Campos clave: Rol, Seniority, Provincia, Modalidad, Género, Salario, Fecha (Mes/Año).

- **Tablas de Dimensiones**
  - `Dim_Rol` → Rol / puesto.  
  - `Dim_Seniority` → Junior, Semi-Senior, Senior.  
  - `Dim_Modalidad` → Presencial, Remoto, Híbrido.  
  - `Dim_Region` / `Dim_Poblacion` → Provincia / ubicación geográfica.  
  - `DimFecha` → Calendario para análisis temporal (Mes, Año, etc.).

Las relaciones son **1 a muchos (1:*)** desde cada dimensión hacia `Fact_Salarios`.

---

## 📐 Diseño del Dashboard (Storytelling en 1 página)

El informe está pensado como un **relato de datos** dividido en 3 zonas claras.

### 1️⃣ Zona superior – Visión general (el **QUÉ**)

Tarjetas KPI:

- **💰 Salario Promedio**
- **💰 Salario Mediano**
- **👥 Total de Encuestados**

👉 Permite responder en segundos: **“¿Cómo está el mercado IT en general?”**

---

### 2️⃣ Zona central – Análisis detallado (el **POR QUÉ**)

Visuales principales:

- 🗺️ **Mapa de salario promedio por provincia**  
  Identifica las zonas mejor remuneradas y posibles polos tecnológicos.

- 📈 **Evolución del salario promedio por Mes/Año**  
  Muestra la tendencia salarial a lo largo del tiempo.

- 📊 **Salario promedio por Rol**  
  Compara qué puestos están mejor pagados dentro del mercado IT.

- 📊 **Salario promedio por Seniority y Género**  
  Permite detectar brechas y diferencias entre perfiles.

🔎 **Panel de filtros (slicers)**

Ubicado a la derecha, con:

- Rol  
- Provincia  
- Seniority  
- Modalidad (presencial, remoto, híbrido)

👉 El usuario puede explorar escenarios como:  
“¿Cómo cambian los salarios si miro solo perfiles Senior y modalidad remota en tal provincia?”

---

### 3️⃣ Zona inferior – Conclusiones y recomendación (el **ENTONCES QUÉ**)

Bloque de texto destacado que resume:

- Conclusiones clave:
  - Los salarios se concentran en **Semi-Senior y Senior**.  
  - La **modalidad remota** suele ofrecer mejores salarios que la presencial.  
  - Existen diferencias entre géneros en ciertos niveles de seniority.

- **Recomendación de negocio:**
  - Enfocar la estrategia de atracción y retención en **perfiles Senior con modalidades remota o híbrida**, acompañando con **políticas de equidad salarial por género y provincia** para mantener la competitividad y la marca empleadora.

---

## ❓ Preguntas de negocio que responde

Algunos ejemplos de preguntas que el dashboard ayuda a responder:

- ¿Cuál es el **salario promedio y mediano** del mercado IT en Argentina?  
- ¿En qué **provincias** se pagan los mejores salarios IT?  
- ¿Cómo evoluciona el salario a lo largo del **año**?  
- ¿Qué **roles** y **seniority** están mejor remunerados?  
- ¿La modalidad **remota** paga mejor que la presencial?  
- ¿Se observan diferencias entre **géneros** para un mismo seniority?

---

## 🛠️ Tecnologías utilizadas

- **Power BI Desktop**
  - Power Query (ETL: limpieza, transformación y carga).
  - Modelado de datos con relaciones 1:*.
  - DAX para medidas (SalarioPromedio, SalarioMediano, TotalEncuestados, etc.).
- **CSV** como fuente de datos (encuesta salarial, población, egresados).

---

## ▶️ Cómo usar el informe

1. Abrir el archivo `.pbix` en **Power BI Desktop**.  
2. Utilizar el **panel de filtros** (derecha) para elegir:
   - Rol
   - Provincia
   - Seniority
   - Modalidad
3. Observar cómo cambian:
   - Los **KPIs** de la parte superior.  
   - El **mapa**, la **tendencia** y los **gráficos de distribución**.  
4. Leer la **franja inferior de conclusiones** para obtener un mensaje ejecutivo y una recomendación de acción.

---

## 📌 Estado del proyecto

✅ Laboratorio finalizado y listo para presentación como **Trabajo Final** del módulo de Power BI / Análisis de Datos.

---

## 👤 Autor

- **Alumno:** Héctor Gabriel Campi  
- **Tema:** Análisis del Mercado Laboral IT – Argentina 2023  
- Proyecto desarrollado como parte de la formación en **Análisis de Datos**.

---

![Dashboard Mercado Laboral IT](./ruta/a/la/imagen.png)
