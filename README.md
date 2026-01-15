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
* `st.slider("Etiqueta", min, max, defecto)`:
