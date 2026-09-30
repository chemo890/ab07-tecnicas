# Bitacora de tecnicas avanzadas
Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: (escribe aqui cual usaste)
## Ejercicio 2: Zero-shot, one-shot y few-shot
| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) | 
|------|-----------------|-------------------------|-----------------------------------| 
| Zero-shot | 5 aciertos| con iconos de colores  | si | 
| One-shot |5 aciertos | con guiones y lista ordenada | si | 
| Few-shot | 5 aciertos | con lista  comillas y flechas| si | 

## Ejercicio 3: Chain of Thought
| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) | 
|--------|--------------------|---------------------------|------------------| 
| Directo | 318.60 | no | si | 
| Paso a paso | 318.60| si | si | 

## Ejercicio 4: Role prompting
| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas | 
|---------|-------------------------------|-----------------------|---------------------| 
| A. Sin rol |sencillo | si| estudiante | 
| B. Rol docente | sencillo | si | estudiante | 
| C. Rol senior |tecnico | si | estudiante de software | 

## Ejercicio 5: Descomposicion
### Registro de pasos

##  Pedido por pasos

### Paso 1

**Qué me entregó la IA:**
Me dio 5 requisitos principales para crear el sistema de inventario.

**Comparación:**
Al hacerlo por pasos, la respuesta fue más directa y se enfocó solo en lo que pedí. En el pedido de una sola vez, la respuesta fue más general y extensa.

### Paso 2

**Qué me entregó la IA:**
Me indicó qué clases debía crear y qué información tendría cada una.

**Comparación:**
La respuesta fue más ordenada porque se basó en los requisitos del paso anterior. En el pedido de una sola vez, todo se presentó junto.

### Paso 3

**Qué me entregó la IA:**
Me dio el código de la clase `Producto`, incluyendo sus datos, el constructor y los métodos necesarios.

**Comparación:**
El código estuvo relacionado con lo que se había definido en los pasos anteriores. Esto hizo que el resultado fuera más claro que el pedido de una sola vez.

### Paso 4

**Qué me entregó la IA:**
Revisó el código de `Producto` y me dio 3 sugerencias para mejorarlo.

**Comparación:**
La revisión fue más específica porque la IA ya conocía el código creado en los pasos anteriores. En el pedido de una sola vez, todo se habría generado al mismo tiempo.

## Ejercicio 6: Prompt estructurado y autocritica
| Qué revisar | Cumple (Sí / No) |
|---|---|
| ¿Tiene las 4 columnas pedidas? | Sí |
| ¿Incluye el bloqueo después de 3 intentos? | Sí |
| ¿Incluye casos con campos vacíos? | Sí |
| ¿Indica qué casos agregó en la autocrítica? | Campos vacíos, correo sin @, contraseña con espacios, límite exacto de 3 intentos fallidos |
| ¿Hay algún caso repetido o que no tenga sentido? | Sí, intentos de inicio de sesión |
 

```text 
<rol>Actua como analista de pruebas de software.</rol> <contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto> <tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea> <formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>
|------------------------------------------------------------------------------|
Revisa tu tabla: faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```
