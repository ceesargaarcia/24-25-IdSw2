## Examen parcial de programacion 1
### 1. **Nombre de Variable `agujero`**
   - **Línea**: [ExamenCesar.java#L6](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L6)
   - **Problema**: Es ambiguo. No se entiende si representa un agujero físico, una opción del usuario, o un elemento del juego.
   - **Sugerencia**: Cambiar a `opcionAgujero` o `seleccionAgujero`.

---

### 2. **Variables `n1`, `n2`, `n3`, `n4`**
   - **Líneas**: [L10-L13](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L10-L13)
   - **Problema**: Nombres genéricos y crípticos. No explican qué representan estos valores (espacios para el caballo).
   - **Sugerencia**: Usar nombres descriptivos como `espaciosAvance1`, `espaciosAvance2`, etc.

---

### 3. **Variables `probabilidad1`, `probabilidad2`, etc.**
   - **Líneas**: [L28-L31](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L28-L31)
   - **Problema**: No indican a qué agujero corresponden las probabilidades.
   - **Sugerencia**: Usar nombres como `probabilidadAgujero1`, `probabilidadAgujero2`, etc.

---

### 4. **Números Mágicos en Condiciones**
   - **Líneas**: 
     - `posicion = posicion + 4;` → [L53](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L53)
     - `posicion = posicion + 6;` → [L61](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L61)
   - **Problema**: Los valores `4` y `6` son arbitrarios y no se vinculan con los mensajes mostrados ("Avanza 3 casillas", "Avanza 4 casillas").
   - **Sugerencia**: Usar constantes como `AVANCE_AGUJERO_3 = 4` y documentar su relación con la lógica del juego.

---

### 5. **Nombres de Métodos y Estructura**
   - **Línea**: Todo el código está en `main` (desde [L3](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L3)).
   - **Problema**: Falta modularización. Por ejemplo, la impresión del tablero se repite con el mismo código.
   - **Sugerencia**: Crear métodos como `imprimirTablero()` o `procesarTurno()` para mejorar legibilidad.

---

### 6. **Inconsistencia en Avances**
   - **Líneas**:
     - Para agujero 3: Mensaje dice "Avanza 3 casillas", pero el código suma `4` → [L51](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L51).
     - Para agujero 4: Mensaje dice "Avanza 4 casillas", pero el código suma `6` → [L59](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L59).
   - **Problema**: Los nombres de variables y mensajes no coinciden con la lógica.
   - **Sugerencia**: Corregir los valores numéricos o ajustar los mensajes para reflejar la realidad.

---

### 7. **Nombres Engañosos en Strings**
   - **Línea**: `String n4 = "      ";` → [L12](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L12)
   - **Problema**: `n4` sugiere "4 espacios", pero contiene 6.
   - **Sugerencia**: Usar nombres como `espacios6` o relacionar con el avance real (ej: `espaciosAvance4` si corresponde a 6 caracteres).

---

### 8. **Falta de Constantes para Valores Críticos**
   - **Líneas**: 
     - `while(posicion <= 60 && turno <= 50)` → [L71](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L71)
     - `if (posicion >= 60)` → [L72](https://github.com/ceesargaarcia/PRG1-22-23-ExamenParcial/blob/97f71d3457851210c902d0eefe9f6923726163a8/entregas/garciaC%C3%A9sar/ExamenCesar.java#L72)
   - **Problema**: El número `60` aparece como valor mágico. No está claro qué representa (ej: meta del juego).
   - **Sugerencia**: Definir una constante como `POSICION_META = 60`.
   