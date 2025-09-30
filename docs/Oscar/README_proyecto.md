# Proyecto Integrador - MVP (Tkinter)

Este proyecto es una aplicación de escritorio desarrollada en **Python** utilizando la librería **Tkinter**.  
Su propósito es servir como un **prototipo (MVP)** que integra múltiples componentes gráficos comunes: formularios, listas, tablas, canvas y ventanas secundarias.

---

## Estructura del Proyecto

```
proyecto/
│── main.py
│── app/
│   │── win_home.py
│   │── win_form.py
│   │── win_list.py
│   │── win_table.py
│   │── win_canvas.py
│── data/
│   │── sample.csv
```

---

## Archivos y Funcionalidad

### 1. `main.py`
- Punto de entrada principal de la aplicación.
- Crea la ventana raíz con `tk.Tk()`.
- Contiene un **menú principal** con botones para abrir las diferentes ventanas:
  - **Home / Bienvenida**
  - **Formulario**
  - **Lista (CRUD básico)**
  - **Tabla (Treeview)**
  - **Canvas (Dibujo)**
- Botón de **Salir** que cierra la aplicación.

---

### 2. `win_home.py`
- Ventana de bienvenida.
- Muestra un mensaje inicial y un botón que abre un **messagebox** con información adicional.
- Incluye un botón **Cerrar** para destruir la ventana secundaria.

---

### 3. `win_form.py`
- Ventana de formulario con dos campos de entrada:
  - **Nombre**
  - **Edad**
- Validaciones:
  - El nombre no puede estar vacío.
  - La edad debe ser un número entero.
- Permite **guardar los datos en un archivo `.txt`** mediante `filedialog.asksaveasfilename`.
- Mensajes de confirmación o error con `messagebox`.

---

### 4. `win_list.py`
- Ventana que implementa un **CRUD básico** con un `Listbox`.
- Funciones:
  - **Agregar**: Inserta un nuevo ítem desde la entrada de texto.
  - **Eliminar**: Borra el ítem seleccionado en la lista.
  - **Limpiar**: Elimina todos los elementos de la lista.
- Incluye botón **Cerrar**.

---

### 5. `win_table.py`
- Ventana que muestra una **tabla (Treeview)** con datos cargados desde un archivo CSV.
- Columnas: `nombre`, `valor1`, `valor2`.
- El archivo fuente se espera en: `data/sample.csv`.
- Si no se encuentra el archivo, muestra una advertencia con `messagebox`.

Ejemplo de `sample.csv` incluido en el proyecto:
```csv
nombre,valor1,valor2
A,10,20
B,15,25
C,12,30
```

---

### 6. `win_canvas.py`
- Ventana con un **Canvas** para dibujar figuras básicas.
- Elementos incluidos de ejemplo:
  - Rectángulo
  - Óvalo (relleno azul claro)
  - Línea
  - Texto centrado
- Sirve como demostración de dibujo en Tkinter.

---

## Requisitos

- **Python 3.8+**
- Librerías estándar (no requiere instalación externa):
  - `tkinter`
  - `csv`
  - `pathlib`

---

## Ejecución

Para ejecutar la aplicación, ejecutar desde la raíz del proyecto:

```bash
python main.py
```

Esto abrirá la ventana principal con acceso a todas las funciones.

---

## Futuras Mejoras

- Persistencia de datos para la lista (guardar en archivo o base de datos).
- Formularios más complejos con validaciones avanzadas.
- Exportación de datos desde la tabla a CSV/Excel.
- Dibujo interactivo en el canvas.
