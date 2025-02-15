# Explicación de la solución propuesta

> [!NOTE]
> He utilizado un proyecto con todos los contenidos del curso que llevamos hasta este momento, así como mi solución al ejercicio previo. Las instrucciones de comportamiento para el proyecto son:
>
> *Eres un consultor de alumnos de la Academia AI4Devs, una academia cuyo ánimo es potenciar a los ingenieros de software gracias a la inteligencia artificial. Ambos somos ingenieros de software y somos amigos. Te has enterado de que estoy haciendo el curso y me vas a ayudar con cualquier duda que tenga, así como a hacer las tareas entregables que las vamos a hacer juntos.*
>
> *Me vas a hablar de forma clara, directa, sin reiterar en tus mensajes cuál es tu papel.*

El prompt inicial que he utilizado ha sido el siguiente:

> ¿Cómo crees que podríamos abordar el ejercicio definido en el documento "✍️ Creación del Backlog de Producto LTI 🔴" ?

Me ha propuesto un plan de prompting para generar prompts que fueran generando las distintas fases. Me ha parecido una buena idea ir por la técnica del metaprompting por lo que he ido por ese camino. Así que le he dicho:

> Vale. Empecemos por el primer paso

Aquí me ha presentado un [prompt](./pr_01.md) que si bien tenía buena pinta, no me ha terminado de convencer ya que ha planteado un esqueleto, no los detalles. Por ello le he respondido:

> Me gusta la estructura, pero tiene pinta de plantilla nada más no te parece?

Y ahora ha generado un [prompt mucho más detallado](./pr_02.md) enfocado a LTI. Ya que estaba con metaprompting quería que el [prompt generado](./pr_02) tuviera el contexto necesario y la información suficiente para generar buenos casos de uso sin necesidad de tener todo el contenido previo.

Con ese [prompt](./pr_02) me he ido a una conversación virgen y se lo he pegado tal cual. El resultado me ha parecido muy bueno ya que me ha generado los 3 [casos de uso](./uc_0.moc.md) con sus historias de usuario. El único problema ha sido que los ha generado todos juntos y los casos de uso solo tenían el título, por lo que le he pedido lo siguiente:

> Haz una descripción de cada caso de uso. Hazlo en formato markdown, un fichero por cada caso de uso que contenga el título así como la descripción del mismo.

Lo ha hecho perfecto. Pero dado que quería experimentar con la creación de una wiki [Zettelkasten](https://zettelkasten.de/overview/) para este ejercicio, quería que cada caso de uso tuviera secciones navegables, por lo que le he pedido lo siguiente:

> Podrías generar de nuevo los ficheros markdown pero con un índice de contenidos en los que pueda hacer click y navegue a cada sección?

Y de nuevo lo ha hecho perfecto tal y como podéis ver en la página de [casos de uso](./uc_0.moc.md) entrando en cualquiera de ellos. Cada caso de uso tiene enlazadas sus historias de usuario.

---
> [!NOTE]
> La conversación que mantuve en un chat vírgen funcionó muy bien, pero es verdad que los resultados iniciales no los devolvía en formato markdown fácilmente copiable y tuve que pedirle que regenerara los outputs en formato markdown. Por ello en mi conversación de metaprompting introduje el siguiente prompt:
>
> *Vale. Como nota adicional, a partir de ahora cada prompt que generes tiene que indicar que el output lo genere en markdown. No hace falta ahora generes nada vale? es para que lo tengas en cuenta para futuros prompts*
> 
> A esto me ha respondido que si quería que volviera a generar el prompt indicando el punto del markdown, a lo que le he respondido:
>
> *No, ya he ajustado yo el prompt y lo he ejecutado y me ha generado las historias de usuario.  ¿Quieres ver el markdown que ha generado o continuamos?*
>

A partir de aquí hemos continuado con la generación del backlog. Me ha propuesto una serie de criterios a tener en cuenta a la hora de generar el prompt que me ha parecido bien, por lo que le he dicho que proceda con la generación del [prompt para la generación del backlog](./pr_03.md). Dicho prompt me lo he llevado a una conversación virgen y lo he ejecutado. Siendo el resultado excelente dando una tabla de evaluación del trabajo y un listado ordenador por prioridad.

A pesar de que el resultado me ha parecido muy bueno, le he pedido lo siguiente:

> Genera una tabla de planificación ordenada por prioridad y agrupada por sprints de 2 semanas

Y el resultado ha vuelto a ser muy bueno. Me llevado ambas tablas al fichero de [product backlog](./product_backlog.md) en el que he editado los enlaces y demás para tener una versión más aproximada a la filosofía Zettelkasten.

---
A continuación he vuelto a mi conversación de metaprompting y le he pedido continuar con el ejercicio:

> No. Ya lo tengo. Avancemos con el ejercicio.

> [!NOTE]
> El No viene dado porque en su respuesta previa me preguntaba que si quería que probara ella con el prompt que había generado.

Me ha propuesto un plan para la generación de los tickets y me ha preguntado sobre qué historia de usuario quería desglosar los tickets, a lo que le he respondido:

> Elige tú la que te parezca más difícil

Ha elegido la evaluación de candidatos mediante IA, me ha dado las razones por las que lo ha elegido y me ha propuesto una estrategia de generación de un prompt que considerara los siguientes puntos:

- El servicio de evaluación que definimos en el diagrama C4
- Las integraciones con otros servicios
- Los componentes de IA que necesitamos
- Frontend necesario para visualización
- Tests en todos los niveles

A lo que le he respondido lo siguiente:

> Sí, vamos a ver qué sale. Me preocupa un poco que queramos abordar muchas cosas en un único prompt, pero bueno, podemos empezar así e ir iterando.

Ha estado de acuerdo en mi apreciación y ha generado un [prompt](./pr_04.md) mucho menos ambicioso y más al grano. El nuevo [prompt](./pr_04.md) me lo he llevado a una conversación virgen y el resultado ha sido muy decente, pero ha generado todos los tickets de una tacada. Por lo que he vuelto a iterar:

> Genera un fichero markdown independiente para cada ticket

Aquí lo ha hecho perfecto hasta llegar al ticket 4 que se ha quedado a medias y ha dado error. Por lo que he tirado un nuevo prompt con el objetivo de ahorrar tokens:

> Genera los ficheros markdown de los tickets AI-004 y AI-005

Los ha completado sin problemas. Puedes ver el resultado en el [listado de tareas](./tk_210.moc.md) de la [historia de usuario](./us_21.md) correspondiente.

---

## Fin y conclusiones

Con esto he dado por terminado el ejercicio. Como nota adicional y reflexiones finales, podría haber alcanzado un nivel de detalle muchísimo más elevado si hubiera utilizado todos los diagramas que generé en la sesión previa como contexto adicional en los chats vírgenes y hubiera invertido aún más tiempo, hasta el punto de que la implementación sería prácticamente trivial, y es que pienso que la tendencia va a ser exactamente esto. Iterar en el diseño y la planificación y no tirar ni una línea de código hasta tener un diseño y una planificación muy trabajados. Este trabajo previo ahora se hace, pero no en tanto detalle porque requiere de una enorme cantidad de tiempo que en general no tenemos, y en muchas ocasiones terminamos entregando MVPs que no salen nunca de ese estado, o que requieren de una gran cantidad de tiempo de back and forth en revisones e iteraciones.

Con estas herramientas y metodologías se pueden conseguir diseños y planificaciones con un gran nivel de detalle en una fracción del tiempo hasta el punto que luego las implementaciones podrán ser casi automatizadas.


> [!TIP] Enlaces de interés
> - [Casos de uso](./uc_0.moc.md)
> - [Prompts generados](./pr_00.moc.md)
> - [Product backlog](./product_backlog.md)
> - [Listado de tickets](./tk_210.moc.md)
> - [Zettelkasten](https://zettelkasten.de/overview/)

