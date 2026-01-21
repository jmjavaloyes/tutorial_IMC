# 📘 Unidad Didáctica 1: Introducción a Web Apps con Python

**Asignatura:** Tecnología y Digitalización (3º ESO)  
**Herramienta:** Python + Streamlit  
**Objetivo:** Crear aplicaciones web interactivas, visuales y funcionales sin necesidad de saber HTML o CSS.


NOTA: Esta documentación está escrita en Markdown. Si quieres saber más: https://www.markdownguide.org/basic-syntax/

---

## 1. Introducción: ¿Qué es Streamlit?

Imaginad que **Python** es un cocinero muy inteligente capaz de resolver cualquier cálculo matemático, pero que no sabe "emplatar" la comida; solo te da los resultados en una pantalla negra con texto (la consola).
ss
**Streamlit** es el camarero. Coge lo que cocina Python y lo presenta en una mesa bonita (una página web) con botones, barras deslizantes y colores para que el usuario pueda interactuar fácilmente.

### La Regla de Oro
> **Cada vez que un usuario toca un botón, escribe un texto o mueve una barra en la web, Streamlit lee y ejecuta todo tu código Python desde la primera línea hasta la última otra vez.**

---
En esta práctica utilizaremos algunas funciones básicas, pero siempre puedes acudir a la documentación para consultar y ampliar información: 
https://docs.streamlit.io/get-started/fundamentals
## 2. El Laboratorio: ¿Dónde programamos?

Para evitar problemas de instalación en los ordenadores de clase, usaremos un editor en la nube gratuito que permite ver el código y la web al mismo tiempo.

### Opción Recomendada: [Streamlite Playground](https://streamlit.io/playground)
1.  Escribe el código a la izquierda
2.  Interactúa con tu código a la derecha
3.  Recuerda que **Python** es un lenguaje indentado (alinea las tabulaciones)

---

## 3. "Cheat Sheet": Chuleta de Comandos

Aquí tienes la caja de herramientas básica. Con estos comandos puedes construir el 90% de las aplicaciones.

### A. Entrada de Datos (Inputs)
Comandos para pedir información al usuario:
* `st.title("Texto")`: Título grande de la página.
* `st.header("Texto")`: Subtítulo.
* `st.write("Texto")`: Párrafo de texto normal.
* `st.number_input("Etiqueta")`: Caja para escribir números exactos.
* `st.slider("Etiqueta", min, max, defecto)`: Barra deslizante.
* `st.text_input("Etiqueta")`: Caja para escribir texto.

### B. Organización del Espacio
* `st.sidebar`: Si añades esto delante de un comando, el elemento se va a la barra lateral izquierda.  
  * *Ejemplo:* `st.sidebar.slider(...)`
* `col1, col2 = st.columns(2)`: Crea dos columnas para poner elementos uno al lado del otro.

### C. Representación Visual (Diseño)
Para que la app parezca profesional y comunique mejor:

**1. El Semáforo (Alertas de colores):**
* 🟢 `st.success("Texto")`: Caja verde (Éxito, Correcto).
* 🟡 `st.warning("Texto")`: Caja amarilla (Advertencia, Cuidado).
* 🔴 `st.error("Texto")`: Caja roja (Error, Peligro).
* 🔵 `st.info("Texto")`: Caja azul (Información neutral).

**2. El Marcador (`st.metric`):**
Ideal para mostrar el resultado final grande y destacado.
```python
# Muestra un número grande con una etiqueta encima
st.metric(label="Temperatura Actual", value="25 ºC", delta="+2º")

Aquí tienes el documento completo y definitivo de la Unidad 1, revisado para incluir todos los apartados (del 1 al 6) con la sección de diseño visual y las instrucciones de publicación.

Copia todo el bloque siguiente y guárdalo como unidad_1_completa.md.

Markdown

# 📘 Unidad Didáctica 1: Introducción a Web Apps con Python

**Asignatura:** Tecnología y Digitalización (3º ESO)  
**Herramienta:** Python + Streamlit  
**Objetivo:** Crear aplicaciones web interactivas, visuales y funcionales sin necesidad de saber HTML o CSS.

---

## 1. Introducción: ¿Qué es Streamlit?

Imaginad que **Python** es un cocinero muy inteligente capaz de resolver cualquier cálculo matemático, pero que no sabe "emplatar" la comida; solo te da los resultados en una pantalla negra con texto (la consola).

**Streamlit** es el camarero. Coge lo que cocina Python y lo presenta en una mesa bonita (una página web) con botones, barras deslizantes y colores para que el usuario pueda interactuar fácilmente.

### La Regla de Oro
> **Cada vez que un usuario toca un botón, escribe un texto o mueve una barra en la web, Streamlit lee y ejecuta todo tu código Python desde la primera línea hasta la última otra vez.**

---

## 2. El Laboratorio: ¿Dónde programamos?

Para evitar problemas de instalación en los ordenadores de clase, usaremos un editor en la nube gratuito que permite ver el código y la web al mismo tiempo.

### Opción Recomendada: Replit (Online)
1.  Entra en [replit.com](https://replit.com/) y regístrate (puedes usar tu cuenta de Google).
2.  Haz clic en el botón azul **"+ Create Repl"**.
3.  En el buscador "Template" escribe: **Streamlit**.
4.  Selecciona la plantilla oficial de Streamlit.
5.  Ponle un título a tu proyecto (ej: `Proyecto-Calculadora`) y pulsa "Create".
6.  Escribe tu código en el archivo `main.py` y dale al botón verde **"Run"**.

---

## 3. "Cheat Sheet": Chuleta de Comandos

Aquí tienes la caja de herramientas básica. Con estos comandos puedes construir el 90% de las aplicaciones.

### A. Entrada de Datos (Inputs)
Comandos para pedir información al usuario:
* `st.title("Texto")`: Título grande de la página.
* `st.header("Texto")`: Subtítulo.
* `st.write("Texto")`: Párrafo de texto normal.
* `st.number_input("Etiqueta")`: Caja para escribir números exactos.
* `st.slider("Etiqueta", min, max, defecto)`: Barra deslizante.
* `st.text_input("Etiqueta")`: Caja para escribir texto.

### B. Organización del Espacio
* `st.sidebar`: Si añades esto delante de un comando, el elemento se va a la barra lateral izquierda.  
  * *Ejemplo:* `st.sidebar.slider(...)`
* `col1, col2 = st.columns(2)`: Crea dos columnas para poner elementos uno al lado del otro.

### C. Representación Visual (Diseño)
Para que la app parezca profesional y comunique mejor:

**1. El Semáforo (Alertas de colores):**
* 🟢 `st.success("Texto")`: Caja verde (Éxito, Correcto).
* 🟡 `st.warning("Texto")`: Caja amarilla (Advertencia, Cuidado).
* 🔴 `st.error("Texto")`: Caja roja (Error, Peligro).
* 🔵 `st.info("Texto")`: Caja azul (Información neutral).

**2. El Marcador (`st.metric`):**
Ideal para mostrar el resultado final grande y destacado.
```python
# Muestra un número grande con una etiqueta encima
st.metric(label="Temperatura Actual", value="25 ºC", delta="+2º")

## 4. Efectos especiales

*`st.balloons()`: Suelta globos por la pantalla (¡úsalo para celebrar!).

*`st.snow()`: Efecto de nieve cayendo.
