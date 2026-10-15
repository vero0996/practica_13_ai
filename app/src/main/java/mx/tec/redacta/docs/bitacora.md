Verónica Paola Zapata Sánchez 
A01199193

Ejercicio 0:
Teléfono. Son conversaciones privadas y las respuestas sugeridas son cortas, justo lo que un modelo chico de 1B hace bien sin comprometer la privacidad.
80 páginas representan decenas de miles de tokens; a ~10 tokens por segundo, solo leerlas tardaría minutos en el teléfono y un modelo chico perdería el hilo o contexto.
Teléfono. Al no haber datos móviles ni internet, la ejecución local en el dispositivo es la única opción.
Ninguno de los dos solo. El modelo no tiene acceso directo en tiempo real al clima ni a la fecha actual. Requiere una API externa para consultar el pronóstico, por lo que necesita red de por medio.

Ejercicio B3: Tokens 8.7 tok/s, 9.0 tok/s, 9.2 tok/s
No del todo. En lugar de limitarse a dar un único texto rediseñado, el modelo generó una respuesta extensa estilo chat de ayuda (con introducción como "Aquí hay algunas opciones...", múltiples sugerencias numeradas, marcas en negrita de Markdown y explicaciones innecesarias al final), lo que alargó el tiempo de respuesta.

Ejercicio C1:
Sobran las introducciones ("Aquí hay algunas opciones..."), la enumeración múltiple con formato Markdown (negritas/comillas) y las explicaciones adicionales al final.
El modelo no está fallando, sino contestando la conversación más probable de su entrenamiento (tipo chat de ayuda). Para evitarlo, el pedido debe:

Enmarcar el texto claramente (p. ej., Texto: «...») para que no crea que el mensaje es para él.

Indicar explícitamente qué NO hacer ("no inventes nada", "escribe solo el texto nuevo", "sin introducciones").

Incluir un ejemplo resuelto (few-shot) para mostrarle el formato exacto de salida.

Ejercicio C3: No. Con textos restrictivos o directos, el modelo suele alucinar o cambiar el sentido (por ejemplo, agregando "El examen será en su casa" en lugar de "Lo que falte lo ven en su casa").
Se cuela la frase "no me envíen solicitudes de prórroga" porque viene del ejemplo resuelto (few-shot) configurado para la regla 3 en la tarea. El modelo chico aprende el formato del ejemplo, pero tiende a copiar fragmentos de su contenido. Por eso la interfaz aclara "Revísalo antes de usarlo": un modelo de 1B sirve para borradores que una persona valida antes de enviar.