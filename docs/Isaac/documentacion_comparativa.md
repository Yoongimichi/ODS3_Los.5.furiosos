# Documentación del Proyecto: Comparativa de Códigos con API Open-Meteo

Este proyecto contiene dos variantes de un programa en Python que
utiliza **Tkinter** para la interfaz gráfica, **Requests** para consumir
la API de Open-Meteo, y **Matplotlib** para generar gráficos embebidos
en la aplicación.\
A continuación, se documentan las similitudes y diferencias entre ambos
códigos.

------------------------------------------------------------------------

## 🔹 Estructura General de Ambos Códigos

-   Uso de **Tkinter** (`tk`, `ttk`, `messagebox`) para la GUI.
-   Consumo de **API Open-Meteo** mediante `requests.get()`.
-   Procesamiento de datos JSON para obtener listas de valores horarios.
-   Uso de **Matplotlib** para generar gráficas de línea y barras.
-   Integración de gráficos en Tkinter mediante `FigureCanvasTkAgg`.
-   Definición de funciones comunes:
    -   `fetch_data()` → Obtiene datos de la API.
    -   `create_line_chart()` → Genera gráfica de línea.
    -   `create_bar_chart()` → Genera gráfica de barras.
    -   `mostrar_graficas()` → Inserta gráficas en la ventana Tkinter.
    -   `open_win_canvas()` → Construye ventana secundaria con las
        gráficas.

------------------------------------------------------------------------

## 🔹 Diferencias Clave

### 1. **Fuente de Datos (API)**

-   **Código 1:**
    -   Ubicación: **León, México** (`latitude=21.12`,
        `longitude=-101.68`).\
    -   Variable obtenida: **Temperatura a 2 metros
        (`temperature_2m`)**.
-   **Código 2:**
    -   Ubicación: **Canberra, Australia** (`latitude=-35.30`,
        `longitude=149.12`).\
    -   Variable obtenida: **Velocidad del viento a 10 metros
        (`windspeed_10m`)**.

------------------------------------------------------------------------

### 2. **Estilo de las Gráficas de Línea**

-   **Código 1:**
    -   Marcador: círculo (`marker="o"`).\
    -   Color por defecto de Matplotlib.\
    -   Sin rejilla.
-   **Código 2:**
    -   Marcador: cuadrado (`marker="s"`).\
    -   Color: rojo (`color="red"`) con transparencia (`alpha=.5`).\
    -   Con rejilla (`ax.grid(True, linestyle="--", alpha=.5)`).

------------------------------------------------------------------------

### 3. **Estilo de las Gráficas de Barras**

-   **Código 1:**
    -   Barras con estilo simple (color por defecto).\
    -   Sin bordes destacados.
-   **Código 2:**
    -   Barras en color celeste (`skyblue`).\
    -   Bordes negros (`edgecolor="black"`, `linewidth=1.2`).\
    -   Con rejilla (`ax.grid(True, linestyle="--", alpha=.5)`).

------------------------------------------------------------------------

### 4. **Etiquetas de los Ejes y Títulos**

-   Ambos códigos usan `Hora` en el eje X y `°C` en el eje Y, aunque en
    el **Código 2** debería modificarse a otra unidad (por ejemplo,
    `km/h`) porque mide **velocidad del viento** y no temperatura.

------------------------------------------------------------------------

## 🔹 Conclusiones

-   **Código 1** → Se centra en la **temperatura horaria de León
    (México)** y presenta gráficas **simples**.\
-   **Código 2** → Se centra en la **velocidad del viento en Canberra
    (Australia)** y ofrece gráficas con un **diseño más trabajado**
    (colores, transparencias, cuadrículas).

Ambos proyectos son funcionales, pero la segunda versión aporta
**mejoras estéticas y de legibilidad** en los gráficos.

------------------------------------------------------------------------

## 📌 Recomendaciones

1.  Ajustar etiquetas de los ejes en **Código 2** para reflejar la
    métrica real (`km/h` en vez de `°C`).\
2.  Unificar estilos gráficos en ambos códigos para mantener
    consistencia visual.\
3.  Ampliar compatibilidad con más variables de la API (ej. humedad,
    precipitación).\
4.  Implementar manejo de errores más detallado con `try/except`
    (ejemplo: validación de JSON incompleto).
