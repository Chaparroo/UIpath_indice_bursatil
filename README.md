# Robot de Recomendación de Inversión – UiPath

## 📌 Descripción
Este proyecto consiste en la creación de un **robot RPA desarrollado en UiPath** que realiza **recomendaciones de inversión** a partir de la consulta de un **índice bursátil** (por ejemplo, IBEX35).

El robot automatiza la obtención del valor del índice bursátil en:
- 📈 **La apertura del día de hoy**
- 📉 **El cierre del día de ayer**

La información se obtiene mediante **web scraping en Google**, y con base en estos valores el robot genera una recomendación de inversión.

---

## 🎯 Objetivo
Automatizar el proceso de consulta de un índice bursátil y recomendar:
- **NO invertir**, si el valor del índice hoy es mayor que ayer.
- **Invertir**, si el valor del índice hoy es menor que ayer.

---

## 🧠 ¿Qué es un índice bursátil?
Un índice bursátil representa el valor conjunto de un grupo de empresas.  
Por ejemplo, el **IBEX35** agrupa las 35 empresas más importantes de España.  
Cuando el índice sube, el valor de una inversión asociada al índice aumenta, y viceversa.

---

## ⚙️ Funcionalidad del Robot

El robot realiza los siguientes pasos:

1. **Cuadro de diálogo de entrada**  
   Se solicita al usuario el índice bursátil a consultar.  
   Ejemplo de pregunta:  
   > *¿Qué índice bursátil quiere consultar?*

2. **Abrir navegador**  
   El robot abre un navegador y accede a:  
   https://www.google.com/

3. **Búsqueda del índice bursátil**  
   - Escribe el índice bursátil ingresado por el usuario en la barra de búsqueda.
   - Presiona la tecla **Enter** para realizar la búsqueda.

4. **Extracción de valores**  
   Se extraen mediante web scraping:
   - El valor del índice en el **cierre del día de ayer**
   - El valor del índice en la **apertura del día de hoy**

5. **Cerrar navegador**  
   Se cierra la pestaña del navegador para evitar ventanas abiertas tras la ejecución.

6. **Verificación de resultados**  
   Se muestran los valores obtenidos usando una actividad **Escribir línea** para validar la correcta extracción  
   (por ejemplo, probando con el índice **IBEX35**).

---

## 🛠️ Tecnologías Utilizadas
- UiPath Studio
- Web Scraping (Modern Experience)
- Automatización de Navegador
- Variables y Condicionales

---

## ▶️ Ejecución
1. Abrir el proyecto en UiPath Studio.
2. Ejecutar el proceso.
3. Ingresar el índice bursátil solicitado (ejemplo: `IBEX35`).
4. Revisar la recomendación generada por el robot.

---

## 📄 Notas
- El robot depende de la estructura visual de Google, por lo que cambios en la página pueden requerir ajustes en los selectores.
- Se recomienda ejecutar el proceso con el navegador en modo visible para facilitar la validación.

---

## 👤 Autor
Proyecto desarrollado como actividad práctica de automatización con UiPath por Felipe Lopez.
