
# 📄 Documentación Comparativa del Proyecto API con Tkinter y Open-Meteo

Este proyecto contiene **dos versiones de código** en Python que implementan una interfaz gráfica con **Tkinter** y visualización de datos meteorológicos usando **matplotlib**, obtenidos desde la API de **Open-Meteo**.

Ambos programas comparten la misma estructura base, pero presentan diferencias importantes en:
- **Ubicación geográfica consultada**
- **Tipo de variable meteorológica**
- **Estilo de visualización gráfica**

---

## 🔹 Código 1 – Temperatura en León, Gto
- **Ubicación:** `latitude=21.12`, `longitude=-101.68` (León, Guanajuato, México).
- **Variable consultada:** `temperature_2m` (temperatura a 2 metros de altura).
- **Visualización:**
  - Gráfica de **línea** con marcadores circulares (`o`).
  - Gráfica de **barras** simple sin personalización adicional.
- **Etiquetas de los ejes:**
  - `Hora`
  - `°C`
- **Estilo gráfico:** Minimalista, sin colores personalizados.

---

## 🔹 Código 2 – Velocidad del Viento en San Miguel de Allende, Gto
- **Ubicación:** `latitude=20.91`, `longitude=-100.72` (San Miguel de Allende, Guanajuato, México).
- **Variable consultada:** `windspeed_10m` (velocidad del viento a 10 metros).
- **Visualización:**
  - Gráfica de **línea** en color verde (`#50F527`), con marcadores cuadrados (`s`), transparencia (`alpha=0.5`) y grosor de línea aumentado.
  - Gráfica de **barras** en color rojo, con cuadrícula (`grid`) punteada y semitransparente.
- **Etiquetas de los ejes:**
  - `Hora`
  - `Windspeed`
- **Estilo gráfico:** Más trabajado, con personalización de colores y cuadrícula.

---

## ⚖️ Comparación General
| Aspecto | Código 1 (Temperatura) | Código 2 (Viento) |
|---------|------------------------|-------------------|
| **Ciudad** | León, Gto | San Miguel de Allende, Gto |
| **Coordenadas** | 21.12, -101.68 | 20.91, -100.72 |
| **Variable API** | `temperature_2m` | `windspeed_10m` |
| **Unidad mostrada** | °C | Windspeed |
| **Línea** | Azul estándar, marcador circular | Verde fosforescente, marcador cuadrado, más gruesa, semitransparente |
| **Barras** | Azul estándar, sin cuadrícula | Roja, con cuadrícula punteada |
| **Estilo** | Simple y claro | Personalizado y más visual |

---

## 📌 Conclusión
- **Código 1** se centra en mostrar la **temperatura de León** con un estilo sencillo y fácil de leer.  
- **Código 2** presenta una visualización más rica y personalizada, enfocada en la **velocidad del viento en San Miguel de Allende**.  

Ambos ejemplos son útiles para proyectos de aprendizaje en **Tkinter + APIs + matplotlib**, pero muestran cómo la **misma estructura base** se puede adaptar para distintas **variables meteorológicas** y estilos gráficos.

---
