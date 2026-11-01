# Retroalimentación — Taller evaluativo 03 (NumPy)

**Estudiante:** Wilmar Alonso Quiros Usuga · **Taller:** Taller evaluativo 03 — NumPy
**Fecha límite:** 2026-11-01 23:59 · **Versión revisada:** commit `6380e7d`

Muy buen trabajo con NumPy: casi todos los resultados coinciden con los esperados.

## Nota

| Criterio | Puntos |
|---|---|
| Creación y atributos de arreglos (Ej. 1) | 10 / 10 |
| Indexación y slicing (Ej. 2) | 10 / 10 |
| Máscaras booleanas (Ej. 3) | 15 / 15 |
| Vectorización y broadcasting (Ej. 4) | 9 / 15 |
| Estadística por eje y funciones universales (Ej. 5 y 6) | 19 / 20 |
| Integración (Ej. 7) | 8 / 10 |
| Ejecución sin errores | 10 / 10 |
| Documentación | 2 / 5 |
| Entrega correcta | 1 / 5 |
| **Total** | **84 / 100** |
| **Nota (0–5)** | **4.20** |

Este taller aporta **12.6 %** de los 15 % del momento evaluativo.

## 1. Creación y atributos de arreglos (10 / 10)
**Lo que hizo bien:**
- `lecturas_crudas` se creó con `np.array` desde una lista de listas y sus atributos se leyeron del arreglo.
- `dias`, `pendientes` e `interceptos` son correctos.

## 2. Indexación y slicing (10 / 10)
**Lo que hizo bien:**
- Cada resultado sale de una sola expresión y el bloque tiene forma (3, 4).

## 3. Máscaras booleanas (15 / 15)
**Lo que hizo bien:**
- Las dos máscaras están bien hechas, con `&` y paréntesis, sin bucles.
- Quedaron 2 faltantes, 5 lecturas útiles y promedio 27.0.

## 4. Vectorización y broadcasting (9 / 15)
**Lo que hizo bien:**
- Convirtió pendientes e intercepto en columnas (5, 1) y `calibradas` quedó correcta, con la primera fila esperada.
- No modificó `lecturas_crudas`.

**Lo que puede mejorar:**
- Falta la celda de texto que explica por qué multiplicar (5, 7) por (5,) da error.
- `campana_calibrada` se calculó con las 8 lecturas de la campaña (incluidos -999.0 y 600.0) y no con `lecturas_utiles`. Por eso muestra valores absurdos como -1199.3.

**Cómo corregirlo:**
- Agregue antes del ejercicio una celda de texto de dos o tres frases: NumPy compara las formas de derecha a izquierda, 7 contra 5 no coincide, y por eso hay que pasar el vector a forma (5, 1).
- Calcule `campana_calibrada` aplicando `1.2 * lecturas_utiles - 0.5`, y el promedio directamente sobre ella.

## 5. Estadística por eje y funciones universales (19 / 20)
**Lo que hizo bien:**
- Promedios por sensor y por día, máximos y media sobre el límite (43.275) son correctos.
- `excedente`, `desvio_sensor_b` y `en_alerta` usan `np.maximum`, `np.abs`, `np.round` y una copia con máscara; `calibradas` queda intacto y hay 8 celdas en alerta.

**Lo que puede mejorar:**
- El promedio general se redondea con `round` de Python y no con `np.round`, y varios resultados se muestran sin redondear.

**Cómo corregirlo:**
- Use `np.round(..., 2)` al imprimir todos los resultados del Ejercicio 5, incluidos el máximo por sensor y la media sobre el límite.

## 6. Integración (8 / 10)
**Lo que hizo bien:**
- Los conteos (9, 18, 7 y 1) salen de máscaras, suman 35 y `dia_pico` es 5.

**Lo que puede mejorar:**
- La primera línea impresa no coincide carácter por carácter con la pedida: escribió `Buena = 9` con espacios alrededor del signo igual y debía ser `Buena=9`.

**Cómo corregirlo:**
- Quite los espacios alrededor de cada `=` en el texto del primer `print`, para que quede exactamente como en la guía.

## 7. Ejecución sin errores (10 / 10)
**Lo que hizo bien:**
- El notebook corre completo sin errores y la verificación final se imprime.

## 8. Documentación (2 / 5)
**Lo que hizo bien:**
- Los nombres de variables están en `snake_case` y sin tildes.
- Cada ejercicio tiene una celda de texto con su título.

**Lo que puede mejorar:**
- Las celdas de texto solo tienen el título del ejercicio, no explican qué hace.
- Falta la celda inicial con el título del taller, su nombre completo y la fecha.

**Cómo corregirlo:**
- Debajo de cada título escriba una o dos frases sobre qué se calcula en ese ejercicio.
- Agregue al inicio una celda de texto con el título, su nombre completo y la fecha.

## 9. Entrega correcta (1 / 5)
**Incumplimiento de convención.** No siguió la estructura acordada: el notebook debe estar en la carpeta `ejercicios/` con el nombre exacto `taller-evaluativo-03-numpy.ipynb`. Estaba en la raíz del repositorio con el nombre `EJERCICIO_evaluativo_03_— NumPy.ipynb`. Además hay otros notebooks sueltos en la raíz (`numpy.ipynb`, `Formula_temp.ipynb`) que parecen apuntes de clase. El trabajo sí estaba visible en GitHub antes del plazo.

**Cómo corregirlo:**
- Mueva el notebook a `ejercicios/` y cámbiele el nombre a `taller-evaluativo-03-numpy.ipynb`; al guardar desde Colab elija esa carpeta y ese nombre.

## ¿El notebook funciona?
Sí: corre completo sin errores y la celda de verificación imprime "Verificación completada sin errores.". Los resultados coinciden con los esperados; solo difiere el formato de una línea de salida y `campana_calibrada`.

## Para el próximo taller
- Guarde el notebook en `ejercicios/` con el nombre exacto indicado.
- Empiece con una celda de título con su nombre y la fecha.
- Escriba antes de cada ejercicio una explicación breve de lo que hace.
- Copie los textos de salida exactamente como se piden.
- Responda las preguntas de texto de la guía (como la del error de formas) en una celda propia.
