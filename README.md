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

### Opción Recomendada: [Streamlite Playground)](https://streamlit.io/playground)
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
* `st.slider("Etiqueta", min, max, defecto)`:
