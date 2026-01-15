# 📘 Unidad Didáctica 1: Creación de Web Apps con Python

**Asignatura:** Tecnología y Digitalización (3º ESO)  
**Herramienta:** Python + Streamlit  
**Objetivo:** Crear aplicaciones web interactivas y visuales sin saber HTML.

---

## 1. Introducción: ¿Qué es Streamlit?

Imaginad que **Python** es un cocinero muy inteligente capaz de resolver cualquier cálculo matemático, pero que no sabe "emplatar" la comida; solo te da los resultados en una pantalla negra con texto.

**Streamlit** es el camarero. Coge lo que cocina Python y lo presenta en una mesa bonita (una página web) con botones, barras deslizantes y colores para que el usuario pueda interactuar fácilmente.

### La Regla de Oro
> **Cada vez que un usuario toca un botón o mueve una barra en la web, Streamlit lee y ejecuta todo tu código Python desde la primera línea hasta la última otra vez.**

---

## 2. El Laboratorio: ¿Dónde programamos?

Para evitar problemas de instalación en los ordenadores de clase, usaremos un editor en la nube gratuito.

### Opción Recomendada: Replit (Online)
1.  Entra en [replit.com](https://replit.com/) y regístrate.
2.  Haz clic en el botón azul **"+ Create Repl"**.
3.  En el buscador "Template" escribe y selecciona **Streamlit**.
4.  Ponle un título a tu proyecto (ej: `Mi-Primera-App`) y pulsa "Create".
5.  Escribe tu código en el archivo `main.py` y dale al botón verde **"Run"**.

---

## 3. "Cheat Sheet": Chuleta de Comandos

Aquí tienes las herramientas básicas que necesitas para construir tu app.

### A. Entrada de Datos (Inputs)
Comandos para que el usuario nos dé información:
* `st.title("Texto")`: Título grande de la página.
* `st.header("Texto")`: Subtítulo.
* `st.write("Texto")`: Párrafo de texto normal.
* `st.number_input("Etiqueta")`: Caja para escribir números.
* `st.slider("Etiqueta", min, max, defecto)`: Barra deslizante.
* `st.text_input("Etiqueta")`: Caja para escribir texto.

### B. Organización
* `st.sidebar`: Si pones esto delante de un comando (ej: `st.sidebar.slider`), el elemento se va a la barra lateral izquierda.
* `col1, col2 = st.columns(2)`: Crea dos columnas para poner cosas una al lado de la otra.

### C. Representación Visual (Diseño)
Para que la app parezca profesional, no uses solo texto plano.

**1. El Semáforo (Alertas):**
* 🟢 `st.success("Aprobado")`: Caja verde.
* 🟡 `st.warning("Cuidado")`: Caja amarilla.
* 🔴 `st.error("Error")`: Caja roja.
* 🔵 `st.info("Información")`: Caja azul.

**2. El Marcador (`st.metric`):**
Ideal para mostrar resultados finales grandes.
```python
# Muestra un número grande con una etiqueta encima
st.metric(label="Temperatura", value="25 ºC", delta="+2º")
