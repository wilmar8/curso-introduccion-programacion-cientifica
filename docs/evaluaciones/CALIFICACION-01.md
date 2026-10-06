# Retroalimentación — Taller evaluativo 01

**Estudiante:** Wilmar Quiros Usuga · **Taller:** Taller evaluativo 01 — Python y estructuras de datos
**Fecha límite:** 2026-10-06 23:59 · **Versión revisada:** commit `ea10231`

## Nota

| Criterio | Puntos |
|---|---|
| Variables, tipos y operadores (Ej. 1 a 4) | 12 / 20 |
| Condicionales y clasificación (Ej. 5) | 13 / 15 |
| Bucles, acumuladores y control de flujo (Ej. 6 a 8) | 24 / 30 |
| Estructuras de datos nativas (Ej. 9) | 14 / 15 |
| Ejecución sin errores | 5 / 10 |
| Documentación en celdas de texto | 3 / 5 |
| Entrega correcta | 1 / 5 |
| **Total** | **72 / 100** |
| **Nota (0–5)** | **3.60** |

Este taller aporta **10.8 %** de los 15 % del momento evaluativo.

## 1. Variables, tipos y operadores (12 / 20)
**Lo que hizo bien:**
- Los tipos de las siete variables del Ejercicio 1 son los correctos.
- En el Ejercicio 2 la conversión y los tres errores salen de operadores, no de valores escritos a mano.
- El Ejercicio 4 da los tres booleanos correctos usando `and` y `not`, sin `if`.

**Lo que puede mejorar:**
- En el Ejercicio 1 no se verificó el tipo con `type()`: se imprimieron las variables envueltas en `str()`, `int()`, etc., lo que no comprueba nada. Además, `altitud_mar` y `num_lecturas` no usan los nombres pedidos (`altitud_m`, `numero_lecturas`).
- En el Ejercicio 3, `horas_sobrantes` está mal: se calculó con `num_lecturas % 24` y debía ser `horas_completas % 24`. Da 17 y debía dar 1.
- En el Ejercicio 2 el primer `print` dice "Lectura convertida" pero muestra el valor en mg/m³.

## 2. Condicionales y clasificación (13 / 15)
**Lo que hizo bien:**
- La cadena `if` / `elif` / `else` clasifica bien las cuatro categorías y da "Dañina para grupos sensibles" para 41.8.

**Lo que puede mejorar:**
- Metió la cadena dentro de otro `if lectura_valida`; si la lectura no fuera válida, `categoria` quedaría sin definir. La guía pedía una sola cadena que cubra todos los casos.

## 3. Bucles, acumuladores y control de flujo (24 / 30)
**Lo que hizo bien:**
- Ejercicio 6: 10 lecturas válidas, 2 descartadas y promedio 22.55, calculado después del `for`.
- Ejercicio 7: máximo 58.3, mínimo 7.5, rango y desviación con dos recorridos y sin `max()`, `min()` ni `sum()`.
- Ejercicio 8: el `while` actualiza la concentración y termina (10 horas).

**Lo que puede mejorar:**
- En el Ejercicio 6 no usó `continue`: envolvió el resto del bucle en un `else`, que es justo lo que la guía pedía evitar. Además, las variables se llamaron `lectura_valida` y `lectura_descartas` en lugar de `lecturas_validas` y `lecturas_descartadas`.

## 4. Estructuras de datos nativas (14 / 15)
**Lo que hizo bien:**
- Accede a todo por clave, desempaqueta las coordenadas en `latitud` y `longitud` y usa `get` con valor por defecto sin errores.

**Lo que puede mejorar:**
- El valor por defecto fue `"no_disponible"` y la guía pedía `"no disponible"`.

## 5. Ejecución sin errores (5 / 10)
**Lo que hizo bien:**
- El notebook corre completo sin errores y sin bucles infinitos.

**Lo que puede mejorar:**
- Falta la celda de verificación final, por lo que no aparece el mensaje "Verificación completada sin errores.". Con los nombres de variables que usó, esa celda habría fallado.

## 6. Documentación en celdas de texto (3 / 5)
**Lo que hizo bien:**
- Hay una celda de título con nombre y fecha, y cada ejercicio tiene su celda previa. Los nombres son en `snake_case`.

**Lo que puede mejorar:**
- Las celdas previas son solo el título del ejercicio; no explican qué hace. En el Ejercicio 6 la celda ni siquiera tiene formato de título.

## 7. Entrega correcta (1 / 5)
- No siguió la estructura acordada: el notebook está en la raíz del repositorio con el nombre `taller_evaluativo_01_calidad_del_aire.ipynb`, y debe estar en la carpeta `ejercicios/` con el nombre exacto `taller-evaluativo-01-calidad-del-aire.ipynb` (con guiones).

## ¿El notebook funciona?
Corre completo y sin errores, y los resultados principales (promedio 22.55, extremos 58.3 y 7.5, categorías) coinciden con lo esperado. Pero falta la celda de verificación final y hay un resultado incorrecto en el Ejercicio 3.

## Para el próximo taller
- Use los nombres de variables que indica la guía; la celda de verificación depende de ellos.
- Copie al final la celda de verificación y confirme que imprime el mensaje final.
- Verifique los tipos con `type()` y revise cada resultado contra lo esperado.
- Siga las instrucciones de control de flujo (`continue`) tal como se piden.
- Guarde el notebook en `ejercicios/` con el nombre exacto y escriba en cada celda previa qué hace el ejercicio.
