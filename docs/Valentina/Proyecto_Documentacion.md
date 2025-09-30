# Proyecto Integrador - MVP (Tkinter)

Este proyecto es una **aplicación de escritorio desarrollada con Python y Tkinter**.  
Se organiza en múltiples ventanas modulares para demostrar el uso de interfaces gráficas con diferentes componentes.

---

## Estructura del proyecto

```
/src/app/
│── main.py         # Ventana principal, menú de navegación
│── win_home.py     # Ventana de bienvenida
│── win_form.py     # Ventana con formulario (validación y guardado en archivo)
│── win_list.py     # Ventana con CRUD básico usando Listbox
│── win_table.py    # Ventana con tabla (Treeview) leyendo CSV
│── win_canvas.py   # Ventana con Canvas para dibujos
/data/
│── sample.csv      # Archivo de datos usado por win_table.py
```

---

## Descripción de los módulos

### 1. `main.py`
- Crea la **ventana principal** de la aplicación.
- Contiene botones para abrir las demás ventanas:
  - Home
  - Formulario
  - Lista (CRUD)
  - Tabla (Treeview)
  - Canvas (Dibujo)
- Proporciona un botón para salir de la aplicación.

### 2. `win_home.py`
- Muestra una **ventana de bienvenida**.
- Incluye:
  - Mensaje de saludo.
  - Botón para mostrar un cuadro de diálogo con `messagebox.showinfo`.
  - Botón para cerrar la ventana.

### 3. `win_form.py`
- Contiene un **formulario simple** con campos de **nombre** y **edad**.
- Validaciones:
  - El nombre no puede estar vacío.
  - La edad debe ser un número entero.
- Funcionalidad:
  - Guarda los datos ingresados en un archivo de texto (`.txt`) usando `filedialog.asksaveasfilename`.
  - Muestra mensajes de éxito o error con `messagebox`.

### 4. `win_list.py`
- Implementa un **CRUD básico con Listbox**.
- Funciones disponibles:
  - **Agregar**: añade un elemento al `Listbox`.
  - **Eliminar**: elimina el elemento seleccionado.
  - **Limpiar**: borra todos los elementos.
- Incluye validaciones con `messagebox` y un botón de cierre.

### 5. `win_table.py`
- Muestra una **tabla usando `ttk.Treeview`**.
- Lee datos desde el archivo CSV ubicado en `/data/sample.csv`.
- Cada fila del archivo se carga en la tabla automáticamente.
- Si el archivo no existe, se muestra una advertencia (`messagebox.showwarning`).

### 6. `win_canvas.py`
- Crea una ventana con un **Canvas para dibujos**.
- Incluye ejemplos de figuras:
  - Rectángulo
  - Óvalo
  - Línea
  - Texto
- Sirve como demostración de las capacidades gráficas de Tkinter.

---

## Dependencias

Este proyecto está basado únicamente en librerías estándar de Python:
- `tkinter` (interfaces gráficas)
- `csv` y `pathlib` (manejo de archivos en `win_table.py`)

No se requieren dependencias externas.

---

## Ejecución del proyecto

1. Asegúrate de tener Python 3 instalado.
2. Coloca el archivo `sample.csv` dentro de la carpeta `/data/`.
3. Ejecuta el proyecto desde la carpeta raíz:

```bash
python src/app/main.py
```

---

## Posibles mejoras futuras

- Implementar estilos personalizados con `ttk.Style`.
- Añadir persistencia de datos en una base de datos en lugar de archivos planos.
- Mejorar el CRUD de la lista para permitir edición.
- Agregar más validaciones en formularios.
- Incluir más ejemplos gráficos en el Canvas.

---

✍️ **Autor:** Equipo de desarrollo  
📌 **Versión:** MVP 1.0  
