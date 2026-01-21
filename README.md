# 📘 Unidad Didáctica 1: Introducción a Web Apps con Python

**Asignatura:** Tecnología y Digitalización (3º ESO)  
**Herramienta:** Python + Streamlit  
**Objetivo:** Crear aplicaciones web interactivas, visuales y funcionales sin necesidad de saber HTML o CSS.


NOTA: Esta documentación está escrita en Markdown. Si quieres saber más: https://www.markdownguide.org/basic-syntax/

---

## 1. Introducción: ¿Qué es Streamlit?

Imaginad que **Python** es un cocinero muy inteligente capaz de resolver cualquier cálculo matemático, pero que no sabe "emplatar" la comida; solo te da los resultados en una pantalla negra con texto (la consola).

**Streamlit** es el camarero. Coge lo que cocina Python y lo presenta en una mesa bonita (una página web) con botones, barras deslizantes y colores para que el usuario pueda interactuar fácilmente.

### La Regla de Oro
> **Cada vez que un usuario toca un botón, escribe un texto o mueve una barra en la web, Streamlit lee y ejecuta todo tu código Python desde la primera línea hasta la última otra vez.**

---

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
```

---

## 4. Efectos especiales

* `st.balloons()`: Suelta globos por la pantalla (¡úsalo para celebrar!).

* `st.snow()`: Efecto de nieve cayendo.

## 5. Práctica Guiada: "Calculadora de Salud (IMC)"

Vamos a crear una aplicación real. Copia este código en tu editor y ejecútalo.

Archivo: app.py
```python
import streamlit as st

# 1. Configuración de la página
st.set_page_config(page_title="Salud 3º ESO", page_icon="🏥")

# Título y Descripción
st.title("💪 Calculadora de IMC")
st.markdown("Bienvenido. Introduce tus datos para calcular tu Índice de Masa Corporal.")
st.write("---") # Línea separadora

# 2. Entrada de Datos (Barra Lateral)
st.sidebar.header("Tus Datos")
peso = st.sidebar.number_input("Tu peso (kg)", min_value=0, max_value=200, value=60)
altura = st.sidebar.slider("Tu altura (metros)", 1.00, 2.30, 1.65)

# 3. Botón de Cálculo y Lógica
if st.button("Calcular ahora"):
    
    # Fórmula Matemática: Peso entre altura al cuadrado
    imc = peso / (altura ** 2)
    
    # 4. Mostrar Resultado con Diseño
    col1, col2 = st.columns(2)
    
    with col1:
        # Usamos metric para que el número se vea grande
        st.metric(label="Tu IMC es:", value=f"{imc:.2f}")
        
    with col2:
        # Usamos condicionales (if/elif/else) para el diagnóstico
        if imc < 18.5:
            st.warning("⚠️ Peso bajo")
            st.write("Consulta con un nutricionista.")
        elif 18.5 <= imc < 25:
            st.success("✅ Peso Saludable")
            st.balloons() # ¡Premio!
        elif 25 <= imc < 30:
            st.warning("🟠 Sobrepeso")
            st.write("Te recomendamos hacer ejercicio.")
        else:
            st.error("🔴 Obesidad")
            st.write("Es importante cuidar tu salud.")
            
    # Extra: Mostrar la fórmula usada (LaTeX)
    st.write("---")
    st.info("Fórmula matemática utilizada:")
    st.latex(r''' IMC = \frac{peso}{altura^2} ''')
```
---

## 6. Ejercicio Propuesto (Deberes)
Para demostrar que dominas la materia, debes crear y entregar el siguiente proyecto.

**Nombre del Proyecto:** 🛍️ "La Calculadora de Rebajas"

**Escenario:** Llegan las rebajas y es difícil calcular mentalmente cuánto se queda un producto. Crea una app que ayude a los compradores a saber el precio final rápidamente.

**Requisitos Obligatorios:**

1. **Inputs:** El usuario debe introducir:

El Precio Original (€) (usando `number_input`).

El Descuento (%) (usando `slider` de 0 a 100).

2. **Cálculo:** Debes programar la lógica matemática para hallar el precio final.

3. **Visualización:**

Usa `st.metric` para mostrar el Precio Final.

Usa `st.success` (caja verde) para mostrar cuánto dinero te ahorras en total.

**Bonus (Nota extra):** Si el descuento es mayor del 50%, debe salir un mensaje especial ("¡Menudo Chollo!") o una animación.

Ayuda con las fórmulas:

```Python
ahorro = precio_original * (descuento / 100)
precio_final = precio_original - ahorro
```
## 7. Publicar tu Proyecto

Publica tu app en un servidor real. Sigue estos pasos:

1. **GitHub:** Usa tu cuenta del colegio en GitHub.com y crea un nuevo repositorio con un nombre representativo

2. Crea un archivo llamado `app.py` y copia el contenido del programa.

3. Crea un archivo llamado `Requirements.txt`: Sólo tiene que tener la palabra `streamlit`.

4. Streamlit Cloud: Ve a [Streamlite Cloud](https://share.streamlit.io)

* Inicia sesión con tu cuenta de GitHub.

* Pulsa "Create App" arriba a la derecha

* Selecciona "Deploy now" en la opción "Repositorio de GitHub"

¡Listo! En unos minutos tendrás un enlace web (URL) permanente y público.
