% IntelliJ IDEA AI Assistant
% Adolfo Sanz De Diego
% Diciembre 2024



# Introducción



## ¿Qué es el AI Assistant?

- Herramienta impulsada por **inteligencia artificial** para el desarrollo de software.
- Funcionalidades como explicar código, responder preguntas, generar documentación, y más.

## Consideraciones previas

- El plugin **AI Assistant no viene incluido por defecto** en IntelliJ IDEA y debe ser habilitado manualmente.
- El plugin conecta al usuario con grandes modelos del lenguaje (**LLM**).
- Las solicitudes y fragmentos de código se envían al proveedor del modelo LLM.

## Requisitos del Asistente de IA

- Instalar el plugin **AI Assistant** manualmente.
- Adquirir una licencia del **Servicio de IA de JetBrains**.
- Aceptar los **Términos de Servicio** y la **Política de Uso Aceptable**.



# Instalación y Activación


## Instalación del Plugin


- Haga clic en "**Install AI Assistant**" en la barra de herramientas derecha.
- Alternativamente, vaya a **Settings | Plugins | Marketplace** y busque "**AI Assistant**".
- **Reinicie** IntelliJ IDEA después de la instalación.

## Activación de la Licencia

- Inicie sesión en su cuenta de **JetBrains**.
- Adquiera la licencia o active la **prueba gratuita**.
- Verifique el estado de su licencia en la ventana del Asistente de IA.



# Chat con IA



## Iniciar un nuevo chat

- Haz clic en **AI Assistant** en la barra de herramientas derecha.
- En el campo de entrada, escribe tu pregunta.
- Usa los comandos `/explain` y `/refactor` para ahorrar tiempo al escribir tu consulta.
- Usa el comando `/docs` para hacer preguntas relacionadas con IntelliJ IDEA.

## Adjuntar achivos o funciones

- **#thisFile** hace referencia al archivo abierto.
- **#localChanges** hace referencia a los cambios no comprometidos.
- **#file:** abre un popup con los archivos del proyecto actual.
- **#symbol:** agrega un símbolo a la consulta.
- **#schema:** hace referencia a un esquema de base de datos.

## Gestionar el modo de chat inteligente

- El modo de chat inteligente está habilitado por defecto.
- Este modo permite al Asistente IA enviar detalles adicionales sobre el proyecto y el entorno.
- Para desactivarlo, desmarca la opción "**Enable smart chat mode**" en **Settings | Tools | AI Assistant**

## Conectar el chat del AI Assistant a tu LLM local

- Puedes conectar tu LLM local disponible a través de Ollama.
- Abre la configuración, selecciona **Tools | AI Assistant** y habilita Ollama.
- Especifica la URL del host local y prueba la conexión.
- Al trabajar con el chat, selecciona tu modelo de LLM disponible.



# Uso de prompts predefinidos



## Explicar código, Expresiones Regulares, SQL...

- Selecciona un fragmento de código y haz clic derecho para abrir el menú contextual.
- Alternativamente, selecciona un fragmento de código y presiona `Alt+Enter`.
- Selecciona "**AI Actions**" y luego "**Explain code**"
- La ventana de herramientas de **AI Assistant** se abrirá para ofrecerte una explicación.

## Sugerir Refactorización

- Selecciona un fragmento de código y haz clic derecho para abrir el menú contextual.
- Alternativamente, selecciona un fragmento de código y presiona `Alt+Enter`
- Selecciona "**AI Actions**" y luego "**Suggest Refactoring**".
- La ventana de herramientas de **AI Assistant** se abrirá para ofrecerte sugerencias de refactorización.

## Encontrar Problemas

- Selecciona un fragmento de código y haz clic derecho para abrir el menú contextual.
- Alternativamente, selecciona un fragmento de código y presiona `Alt+Enter`
- Selecciona "**AI Actions**" y luego "**Find Problems**"
- La ventana de herramientas de **AI Assistant** se abrirá para mostrar los problemas potenciales.

## Explicar un Error en Tiempo de Ejecución

- Haz clic en "**Explain with AI**" en la consola.
- La ventana de herramientas de **AI Assistant** se abrirá para ofrecerte una explicación del error y sugerir una solución.



# Indicaciones Personalizadas



## Agregar Indicaciones a la Biblioteca de Indicaciones

- Haz clic derecho en cualquier parte del editor para abrir el menú contextual, luego ve a "**AI Actions | Edit User Prompts**"
- Alternativamente, presiona `Alt+Enter`, selecciona "**AI Actions**", y haz clic en "**Add your prompts**".
- Alternativamente, presiona `Ctrl+Alt+S` para abrir la configuración y luego selecciona "**Tools | AI Assistant | Prompt Library**"
- Haz clic en el botón **+**.
- Escribe tu prompt y edita el nombre.

## Modificar las Indicaciones Predefinidas

- Haz clic derecho en cualquier parte del editor para abrir el menú contextual, luego ve a "**AI Actions | Edit User Prompts**"
- Alternativamente, presiona `Alt+Enter`, selecciona "**AI Actions**", y haz clic en "**Add your prompts**".
- Alternativamente, presiona `Ctrl+Alt+S` para abrir la configuración y luego selecciona "**Tools | AI Assistant | Prompt Library**"
- Selecciona la acción para la que deseas modificar.
- Agrega nuevas instrucciones y haz clic en "**Apply**"



# Usar IA en el editor



## Generar código en el editor usando prompts

- Selecciona una pieza de código que desees modificar o coloca el cursor en cualquier lugar del editor y presiona `Ctrl+\`.
- Alternativamente, haz clic derecho en el editor para abrir el menú contextual, selecciona "**AI Actions**"  y luego "**Generate Code**" .
- Si seleccionas un fragmento de código y pides al **AI Assistant** que genere código, solo sugerirá cambios para ese fragmento de código seleccionado.
- Si colocas el cursor en cualquier lugar antes de pedir al **AI Assistant** que genere código, el código generado se insertará en el editor en la posición del cursor.

## Escribir indicaciones para la IA

- En el campo de entrada, escribe tu prompt y presiona `Enter`.
- Espera a que se complete la generación. El código generado se mostrará en la misma pestaña del editor donde invocaste el campo de entrada.
- Si deseas mejorar el código generado, en el mismo campo de entrada, escribe un mensaje de seguimiento con los nuevos requisitos y presiona `Enter`.
- Haz clic en **Accept** para insertar el fragmento generado.

## Revertir y descartar cambios

- Para revertir algunos de los cambios sugeridos, haz clic en **Revert** en la barra lateral.
- Para descartar todos los cambios sugeridos, haz clic en **Discard** en la ventana emergente del campo de entrada.

## Indicaciones mientras escribes

- El **AI Assistant** también puede entender indicaciones mientras escribes directamente en el editor, sin necesidad de invocar el campo de entrada de generación de código.
- Escribe tu prompt directamente en el editor y presiona `Tab`. Para deshacer los cambios, presiona `Ctrl+Z`.



# Sugerencias de nombres



## Obtener ayuda con sugerencias de nombres

- Cuando renombres (`Shift+F6`) un símbolo, el **AI Assistant** sugiere opciones de nombre basadas en su contenido.
- Esta función está habilitada por defecto. Para activarla o desactivarla, revisa la configuración del **AI Assistant**.

## Activar sugerencias de nombres generados por IA

- Presiona `Ctrl+Alt+S` para abrir la configuración y selecciona **Tools | AI Assistant**.
- Usa la casilla de verificación **Provide AI-generated name suggestions**.



# Autocompletado



## Invocar autocompletado con IA

- El autocompletado impulsado por el **AI Assistant** puede autocompletar líneas individuales, bloques de código e incluso funciones completas en tiempo real, basado en el contexto del proyecto.

## Trabajar con autocompletado en el editor

- Las sugerencias se muestran en el editor mientras escribes. También puedes activar el autocompletado presionando `Alt+Shift+\`.
- Para aplicar la sugerencia:
    - Presiona `Tab` para aceptar toda la sugerencia.
    - Presiona `Ctrl+Right` para aceptar la sugerencia palabra por palabra.
    - Presiona `End` para aceptar la sugerencia línea por línea.
- Para rechazar la sugerencia, presiona `Escape`.

## Configurar el autocompletado

- La opción de autocompletado está habilitada por defecto. Puedes configurar su funcionamiento en la configuración.
- Presiona `Ctrl+Alt+S` para abrir la configuración y selecciona **Editor | General | Inline Completion**.



# Corrección de errores



## Corregir errores con IA

- Cuando IntelliJ IDEA detecta código con errores previos a la compilación, sugiere una corrección rápida directamente en el editor.
- El **AI Assistant** puede sugerir correcciones más precisas debido a su conocimiento del contexto.

## Aplicar corrección con IA

- Coloca el cursor en un error destacado en el editor. Luego haz clic en el icono de la bombilla roja o presiona `Alt+Enter` para abrir la lista de sugerencias.
- Haz clic en **Fix with AI**.
- El **AI Assistant** enviará el archivo completo junto con los archivos relacionados al modelo de lenguaje para determinar la corrección más adecuada en este caso específico.
- El código se actualizará directamente en el editor.



# Integración con los Sistemas de Control de Versiones



## Generar mensajes de commit

- Presiona `Alt+0` para abrir la ventana de commits.
- Haz clic en "**Generate Commit Message with AI Assistant**".
- Edita el mensaje si es necesario.

## Personalizar el mensaje de commit

- Presiona `Ctrl+Alt+S` para abrir la configuración.
- Luuego selecciona **Tools | AI Assistant | Prompt Library**.
- Especifica reglas como el número de caracteres requeridos o el idioma.
- Haz clic en **Apply**.

## Editar y mejorar mensajes de commit

- Abre la ventana de control de versiones presionando `Alt+9`.
- Haz clic derecho sobre el commit y selecciona "**Edit Commit Message**".
- Haz clic en "**Improve Commit Message with AI Assistant**".
- Edita el mensaje y haz clic en OK para guardar.

## Explicar commits

- Selecciona uno o varios commits, haz clic derecho y selecciona "**Explain Commit with AI Assistant**".
- **AI Assistant** proporcionará un resumen de los commits seleccionados.

## Generar título y descripción para pull y merge requests

- Al crear un pull request o merge request, haz clic en "**Generate a Title and Description with AI Assistant**" en el campo de descripción.

## Resolver conflictos de Git con AI

- En el diálogo "**Merge Revisions**", haz clic en "**Merge with AI**".
- Revisa el resultado y haz clic en **Apply**.
- Si es necesario, puedes revertir cambios haciendo clic en "**Revert**".



# Generar documentación



## Generar documentación (I)

- Utilizando el **AI Assistant**, puedes generar documentación usando un Gran Modelo de Lenguaje (LLM).
- Coloca el cursor en el fragmento de código deseado y haz clic derecho para abrir el menú contextual.
- Presiona `Alt+Enter`. Selecciona "**AI actions**" y luego "**Write documentation.**".
- El **AI Assistant** generará la documentación para ti.

## Generar documentación (II)

- Alternativamente, en lugar de usar el menú contextual, escribe `/**`, presiona **Enter** y haz clic en "**Generate with AI Assistant**".
- O ve a cualquier función o clase, inicia una nueva línea y escribe `"""`. Presiona **Enter** y haz clic en "**Generate with AI Assistant**".

## Personalización del prompt

- Puedes personalizar el prompt para la acción de "**Write Documentation**" en **Settings | Tools | AI Assistant | Prompt Library | Write Documentation.**.
- Ajusta cómo se genera la documentación en función de tus necesidades específicas.



# Uso de la IA para convertir archivos a otro lenguaje



## Conversión completa de un archivo a otro lenguaje

- Abra el archivo que desea convertir, coloque el cursor en cualquier parte del editor y haga clic derecho para abrir el menú contextual.
- Alternativamente, presione `Alt+Enter`.
- Seleccione **AI Actions** y luego **Convert File to Another Language**.
- En la lista que se abre, elija el lenguaje al que desea convertir el archivo actual.
- Después de la conversión, el archivo convertido se guarda como un archivo separado con una nueva extensión.

## Habilitar la conversión de código a otro lenguaje mediante copiar y pegar

- Presione `Ctrl+Alt+S` para abrir la configuración y luego seleccione **Tools | AI Assistant**.
- Active la opción **Suggest converting pasted code to the language of the target file** y haga clic en **Apply**.
- Ahora puede copiar el fragmento de código que desea convertir y pegarlo en el archivo en el que está trabajando.
- El **AI Assistant** detecta el lenguaje del código pegado y sugiere convertirlo al lenguaje del archivo abierto.
- Si hace clic en **Convert**, el código se convertirá al lenguaje del archivo de destino. El código en el lenguaje original también se pegará, pero comentado.



# Generación de Pruebas



## Generar Pruebas Unitarias

- Ubica el cursor en la **clase o método** para el que deseas generar pruebas.
- Haz clic derecho o presiona `Alt+Enter` para abrir el menú contextual.
- Selecciona **"AI Actions"** y luego **"Generate Unit Tests"**.

## Inspeccionar y Mejorar

- El código generado se abrirá en una pestaña llamada **"AI Diff"**.
- Opciones disponibles:
    - **"Specify"**: Añade nuevos requisitos y presiona `Enter`.
    - **"Regenerate"**: Genera nuevamente las pruebas.
    - **"Customize Prompt"**: Modifica el mensaje para mejorar el resultado.

## Guardar las Pruebas

- Haz clic en **"Accept all"** para guardar el código generado.
- El archivo de prueba:
    - Se ubicará en el módulo de pruebas si existe.
    - Caso contrario, se almacenará junto al archivo fuente.

