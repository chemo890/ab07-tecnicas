# Tarea: Mi prompt avanzado

## Tarea elegida

Elegí una tarea relacionada con **generar casos de prueba para un registro de usuarios**.

La idea es pedirle a la IA que ayude a crear casos de prueba para comprobar si un formulario de registro funciona correctamente.

## Version 1: prompt basico
```text
Genera casos de prueba para un formulario de registro de usuarios.
```

**Técnica agregada:** Ninguna. Es un prompt básico y directo.

**¿Por qué?**
Quise empezar con una instrucción sencilla para ver qué respuesta daba la IA sin darle muchas indicaciones.

**¿Qué mejoró?**
La IA pudo generar algunos casos de prueba, pero la respuesta fue muy general y no tenía un formato específico.

## Version 2

```text

Actúa como un desarrollador encargado de probar un formulario de registro de usuarios.

Genera casos de prueba para comprobar:
- Nombre
- Correo electrónico
- Contraseña
- Confirmación de contraseña

Divide los casos entre datos correctos y datos incorrectos.

Presenta la respuesta en una tabla con:
- Caso
- Datos ingresados
- Resultado esperado
```

**Técnica agregada:** Role prompting y prompt estructurado.

**¿Por qué?**
Agregué un rol específico para que la IA se enfoque en las pruebas de software. También indiqué cómo quería recibir la respuesta.

**¿Qué mejoró?**
La respuesta fue más ordenada y los casos de prueba estuvieron más relacionados con la tarea.

## Version 3: prompt final

```

Actúa como un tester de software encargado de revisar un formulario de registro de usuarios de una aplicación web.

Tu objetivo es crear casos de prueba sencillos pero completos.

Primero, divide el problema en estas partes:
1. Revisar los campos obligatorios.
2. Revisar el formato del correo.
3. Revisar la contraseña.
4. Revisar la confirmación de contraseña.
5. Revisar casos donde los datos sean incorrectos.

Ejemplos:
- Si el correo es "usuario@gmail.com", debe aceptarse.
- Si el correo es "usuario.com", debe rechazarse.
- Si las contraseñas coinciden, el registro debe continuar.
- Si las contraseñas no coinciden, debe mostrarse un mensaje de error.

Después de analizar los casos, revisa tu propia respuesta y comprueba que no falte ningún caso importante.

Entrega la respuesta usando esta tabla:

| Nº | Caso de prueba | Datos | Resultado esperado |
|---|---|---|---|


Al final agrega una sección llamada "Casos importantes" con los 3 casos que consideres más necesarios de probar.
```


**Técnicas agregadas:** Role prompting, few-shot, descomposición, prompt estructurado y autocrítica.

**¿Por qué?**
Agregué ejemplos para que la IA entienda mejor el tipo de casos que necesito. También dividí la tarea en pasos y le pedí que revise su respuesta antes de entregarla.

**¿Qué mejoró?**
La respuesta final fue más completa, organizada y fácil de revisar. También se redujo la posibilidad de olvidar casos importantes.

## Tecnicas usadas en el prompt final

| Técnica             | Parte del prompt                              |
| ------------------- | --------------------------------------------- |
| Role prompting      | "Actúa como un tester de software..."         |
| Descomposición      | Los 5 pasos para revisar los diferentes casos |
| Few-shot            | Los ejemplos de correos y contraseñas         |
| Prompt estructurado | La tabla con los campos definidos             |
| Autocrítica         | "Revisa tu propia respuesta..."               |

## Evaluacion del resultado

| Criterio                                    | Sí / No |
| ------------------------------------------- | ------- |
| El prompt tiene un rol específico           | Sí      |
| Incluye ejemplos                            | Sí      |
| La tarea está dividida en pasos             | Sí      |
| Tiene un formato de respuesta definido      | Sí      |
| La IA revisa su propia respuesta            | Sí      |
| Los casos de prueba son fáciles de entender | Sí      |

## Por que elegi estas tecnicas

Elegí estas técnicas porque mi tarea necesita que la respuesta sea ordenada y que no se olviden casos importantes. El **role prompting** ayuda a que la IA se enfoque en las pruebas, los **ejemplos** ayudan a explicar qué tipo de resultados espero y la **descomposición** permite revisar cada parte del registro por separado. También usé un formato estructurado porque una tabla hace que los casos de prueba sean más fáciles de leer. Finalmente, agregué una revisión de la respuesta para intentar detectar casos que puedan faltar.
