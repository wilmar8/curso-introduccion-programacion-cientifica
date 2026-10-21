# Retroalimentación — Taller evaluativo 02: Funciones y POO

**Estudiante:** Wilmar Quiros Usuga · **Taller:** Taller evaluativo 02 — Funciones y POO
**Fecha límite:** 2026-10-21 00:00 · **Versión revisada:** commit `f8f3e52`

## Nota

| Criterio | Puntos |
|---|---|
| Funciones: parámetros, valores por defecto y retorno (Ej. 1 a 3) | 12 / 20 |
| `map`, `filter` y `lambda` (Ej. 4) | 9 / 10 |
| Clases, atributos y métodos (Ej. 5 y 7) | 7 / 15 |
| Encapsulamiento y validación (Ej. 6) | 0 / 15 |
| `__repr__` y `__str__` (Ej. 6 a 8) | 0 / 10 |
| Integración de funciones y clases (Ej. 8) | 0 / 10 |
| Ejecución sin errores | 0 / 10 |
| Documentación | 1 / 5 |
| Entrega correcta | 1 / 5 |
| **Total** | **30 / 100** |
| **Nota (0–5)** | **1.50** |

Este taller aporta **4.5 %** de los 15 % del momento evaluativo.

## 1. Funciones: parámetros, valores por defecto y retorno (12 / 20)
**Lo que hizo bien:**
- `calibrar_lectura` tiene los valores por defecto en la firma y usa `return`.
- `promedio_valido` usa variables locales, devuelve 27.0 para las lecturas de SBC-A y devuelve `None` si no hay lecturas válidas.
- La función de validez descarta bien -999.0 y 600.0.

**Lo que puede mejorar:**
- La función del Ejercicio 2 debía llamarse `es_lectura_valida`; usted la llamó `es_lectura_sbc_a`.
- En el Ejercicio 1, `sin_calibrar` debía ser `calibrar_lectura(10.0)` y `calibrada` debía usar 1.2 y -0.5. Los valores quedaron cambiados (calibrada dio 25.0 en lugar de 11.5).
- Faltaron los docstrings de una línea en las funciones.
- En el Ejercicio 3 la prueba sin lecturas válidas debía ser con `[-999.0, -999.0]`; usted usó `[10.0, -999.0]`, así que no se comprobó el caso de `None`.

## 2. `map`, `filter` y `lambda` (9 / 10)
**Lo que hizo bien:**
- Obtuvo las 5 lecturas calibradas (11.5 la primera, 61.9 la última) y 2 excedencias, usando `filter`, `map` y `lambda` sin bucles.

**Lo que puede mejorar:**
- Se apoya en la función con nombre distinto al pedido (ver punto 1).

## 3. Clases, atributos y métodos (7 / 15)
**Lo que hizo bien:**
- `Lectura` guarda sus tres datos con valores por defecto, `a_microgramos` da 25.2 y `es_dato_faltante` reconoce el centinela.

**Lo que puede mejorar:**
- La clase `Estacion` (Ejercicio 7) no está en el notebook.
- Faltan los docstrings de la clase y sus métodos.

## 4. Encapsulamiento y validación (0 / 15)
**Lo que puede mejorar:**
- El Ejercicio 6 no se desarrolló: la celda solo contiene el título copiado y no hay clase `Sensor`.

## 5. `__repr__` y `__str__` (0 / 10)
**Lo que puede mejorar:**
- No hay `__repr__` ni `__str__` en ninguna clase.

## 6. Integración de funciones y clases (0 / 10)
**Lo que puede mejorar:**
- Los Ejercicios 7 y 8 (`categoria_pm25`, `InformeEstacion`) no están en el notebook.

## 7. Ejecución sin errores (0 / 10)
**Lo que puede mejorar:**
- El notebook se detiene en el Ejercicio 6, donde el texto del título quedó en una celda de código y genera un error de sintaxis.
- No está la celda de verificación final.

## 8. Documentación (1 / 5)
**Lo que hizo bien:**
- Hay celdas de texto antes de los Ejercicios 1 a 6 y los nombres usan `snake_case` y `PascalCase`.

**Lo que puede mejorar:**
- Faltan los ejercicios 7 y 8 con su texto previo, y ninguna función o clase tiene docstring.
- La celda inicial tiene el nombre y la fecha, pero sin el título del taller.

## 9. Entrega correcta (1 / 5)
No siguió la estructura acordada: el notebook debe estar en la carpeta `ejercicios/` con el nombre exacto `taller-evaluativo-02-funciones-y-poo.ipynb`. Su trabajo está en la raíz del repositorio con el nombre `Ejercicio_evaluativo_02_—_Funciones_y_POO.ipynb`. Dentro de `ejercicios/` solo está `Clase1ejercicios.ipynb`.

## ¿El notebook funciona?
No corre completo: se detiene con un error en el Ejercicio 6 y los Ejercicios 7 y 8 no existen. La celda de verificación no está incluida. Los resultados de los Ejercicios 1 a 5 son en su mayoría correctos.

## Para el próximo taller
- Entregue el notebook en `ejercicios/` con el nombre exacto indicado.
- Complete todos los ejercicios y ejecute "Reiniciar y ejecutar todas" antes de entregar.
- Use los nombres de funciones y los datos de prueba tal como los pide la guía.
- Agregue un docstring de una línea a cada función, clase y método.
- Copie al final la celda de verificación, sin modificarla.
