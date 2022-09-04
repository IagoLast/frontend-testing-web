# Las cosas por sus nombre

Ayer fue la #pulpoCon22, que se ha consolidado como como uno de mis eventos favoritos y que creo que dará mucho de que hablar en el futuro.

Entre otras cosas, tuve la oportunidad de desvirtualizar al gran [@talkingbit1](https://twitter.com/talkingbit1), que me confesó que el secreto del éxito es escribir algo todos los días, y pude asistir a una charla sobre testing de [@nuria_codes](https://twitter.com/nuria_codes) donde entendí que dijo que _los nombres de los tests no importan_ y que dedicamos demasiado esfuerzo y tiempo a ponerle apodos a las cosas en lugar de reflexionar sobre sus características.

En parte estoy de acuerdo y me gustaría recomendar leer las reflexiones del gran Richard Feynman sobre nombrar las cosas vs conocer las cosas.

https://www.youtube.com/watch?v=lFIYKmos3-s


Es cierto que para hablar con alguien de forma efectiva y eficiente es recomendable disponer de un lenguaje común, pero es importante recordar que al menos en cuanto a testing, los nombres son lo de menos. Lo importante es conocer las características, comportamiento y ventajas e inconvenientes de cada tipo de test independientemente del nombre que le demos.

En particular a la hora de hablar de un test me gusta acotar las siguientes características:

- **Sensibilidad**: Probabilidad de fallar si existe un error en el código.
- **Especificidad**: Probabilidad de dar por válido un comportamiento correcto del código.
- **Fragilidad**: Probabilidad de que un test de falsos positivos. Se compone a su vez de:
	- **Estabilidad**: Probabilidad de que un test de el mismo resultado en diferentes ejecuciones.
	- **Flexibilidad**: Tolerancia de un test a cambios en la implementación que no afectan al comportamiento.
- **Precisión**: Mide cómo de complicado es identificar la fuente del error si el test falla.
- **Mantenibilidad**: Mide cómo de complicado es actualizar o modificar el código del test. 
- **Velocidad**: Mide cuánto tiempo tarda el test en ejecutarse.
- **Profundidad**	: Indica el número de componentes y dependencias que se ejecutan en el test.

Con estas características encima de la mesa, creo que uno de los debates más frecuentes es la discusión de qué es un test unitario y qué es un test de integración. Algunos consideran que un test unitario prueba sólo una unidad (profundidad cero) y otros como Fowler [introducen el concepto de test unitarios sociables](https://martinfowler.com/bliki/UnitTest.html) para poder denominar tests unitarios a tests con profunidad N.

Este dogmatismo en cuanto a nombres y "buenas prácticas" hace que algunos se obsesiones con cumplir la máxima de _"la pirámide de tests dice que tenemos que tener muchos test unitarios"_ y llenan la base de código de tests que no sirven absolutamente para nada y jamás probarán un caso de uso completo porque _"esos tests son frágiles y es malo que un test sea frágil"_ 

En resumen, aunque llamar a las cosas por su nombre es una buena idea para tener una conversación fluida, por desgracia todavía no tenemos unos nombres establecidos en la industria. Así que lo mejor será tener en cuenta las ventajas e inconvenientes que tomamos con cada tipo de test y **usar la cabeza para determinar qué es lo mejor en nuestro caso particular**.  