# Actividad de Clase: Analizando Agentes de IA con Hugging Face Spaces

## Objetivo

Explorar aplicaciones reales de Inteligencia Artificial en **Hugging
Face Spaces** y analizarlas desde la perspectiva de los **agentes
racionales**.

Al finalizar la actividad, los estudiantes deberán ser capaces de:

-   Identificar los componentes **PEAS** de un agente.
-   Clasificar las propiedades del entorno.
-   Proponer qué tipo de programa de agente podría implementarse detrás
    del sistema.
-   Justificar sus respuestas.

------------------------------------------------------------------------

## Instrucciones

1.  Ingresen a **https://huggingface.co/spaces**.
2.  Exploren diferentes Spaces.
3.  Seleccionen uno que les parezca interesante.
4.  Interactúen con el sistema durante algunos minutos.
5.  Completen la siguiente ficha de análisis.

------------------------------------------------------------------------

# Ficha de análisis

## 1. Nombre del Space

**Nombre:** Z Image Turbo

**Enlace:** https://huggingface.co/spaces/mrfakename/Z-Image-Turbo

------------------------------------------------------------------------

## 2. ¿Qué hace el agente?

El agente genera imagenes realistas partiendo de un prompt que el usuario ingresa con las especificaciones para dicha imagen

------------------------------------------------------------------------

## 3. Análisis PEAS

  ----------------- ----------------------------------------------------
  **Performance**   ¿Qué significa que el agente haga bien su trabajo?
                    R:// Que la imagen generada realmente refleje las instrucciones dadas en el prompt y que lo haga de manera rápida
                    
  **Environment**   ¿Con qué interactúa el agente?
                    R:// Con laa interfaz web gráfica de Hugging Face
                    
  **Actuators**     ¿Qué acciones produce?
                    R:// El visualizador de la interfaz que renderiza y presenta en pantalla la imagen generada lista para ser ver o descargar
                    
  **Sensors**       ¿Qué información recibe como entrada?
                    R:// Recibe la instrucción (prompt) por parte del usuario y las configuraciones avanzadas que se realicen

------------------------------------------------------------------------

## 4. Clasificación del entorno

Complete la siguiente tabla y justifique brevemente cada respuesta.

  -------------- ----------------- ---------------
  Observable     Total              Ya que el agente tiene acceso a la información que necesita para actuar y generar la imagen (el prompt, las configuraciones, etc)
  
  Determinista   No                 Ya que si no se fija la semilla, al ser una IA generativa la imagen va a ser diferente cada vez que se genere
  
  Episódico      Sí                 Ya que cada tarea (generar imagen) es un evento o episodio diferente y no se tienen en cuenta prompts pasados
  
  Estático       Sí                 Ya que ni el prompt ni las configuraciones cambian mientras el modelo está generando la imagen
  
  Discreto       Sí                 Ya que sigue el mismo proceso, recibe un prompt y devuelve una imagen
  
  Conocido       Sí                 Ya que el agente trabaja bajo reglas ya predefinidas que le indican como transformar el prompt a la imagen           

------------------------------------------------------------------------

## 5. ¿Qué tipo de programa de agente creen que es?

Seleccione la opción que consideren más adecuada y explique por qué.

-   Agente de reflejo simple
R:// Ya que este agente genera imagenes basándose solamente en el prompt actual ingresado por el usuario, implementando reglas condición-acción que unen la instrucción del usuario (en este caso el prompt) con
      el resultado que entrega el agente (en este caso la imagen generada). También porque el agente no mantiene un estado continuo entre episodios y tampoco aprende del usuario, solamente dado un texto este aplica
      sus reglas ya predefinidas y ejecuta la acción programada (crear la imagen)

------------------------------------------------------------------------

# Reto adicional

Encuentre un Space que pueda clasificarse como:

1.  **Totalmente observable, determinista y episódico.** -> https://huggingface.co/spaces/not-lain/background-removal
R:// es totalmente observable porque toda la información necesaria ya está contenida en los píxeles de la imagen subida, determinista porque procesar la misma foto siempre va a generar exactamente el mismo recorte sin factores de aleatoriedad, y episódico porque eliminar el fondo de una imagen es una tarea independiente que no afecta a las siguientes

2.  **Parcialmente observable, estocástico y secuencial.** -> https://huggingface.co/spaces/agents-course/First_agent_template
R:// Es parcialmente observable porque el agente no conoce toda la información del mundo exterior ni la intención real del usuario si este no ha interactuado lo suficiente, estocástico porque al estar basado en un modelo de lenguaje (LLM) la misma pregunta puede generar respuestas diferentes, y secuencial porque cada paso que da o respuesta que genera depende de las acciones y el historial de la conversación anterior

------------------------------------------------------------------------

# Rúbrica (10 puntos)

| Criterio | Puntos |
|-----------|:------:|
| Descripción correcta del Space | 2 |
| Identificación de PEAS | 3 |
| Clasificación del entorno | 3 |
| Justificación del tipo de agente | 2 |
| **Total** | **10** |

------------------------------------------------------------------------

