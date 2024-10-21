<img width="300px" src="./logotipo-universidad-nebrija.jpg" alt="image_name png" align="center"/>

## tfm
# Trabajo Final del Máster - Máster Data Science

## Título
El título de la propuesta de trabajo final del máster es: “Modelos Predictivos de la Demanda en la Industria del Calzado Deportivo de Centro América”. 

## Contexto del Negocio
Northbay International es una empresa que nace en 1980 como el socio distribuidor de calzado deportivo Nike para Panamá. A pesar de ser un negocio familiar, la organización creció a lo largo del tiempo adquiriendo territorios adicionales, hasta incluir la distribución de Colombia, Venezuela, Centroamérica y Caribe, un territorio que abarca 130 millones de habitantes. 

El modelo del distribuidor de Nike se conoce como Nike Partner. La operación bajo esta modalidad es un espejo de cualquier oficina de Nike a nivel internacional, pero opera bajo su propio riesgo financiero y personal desvinculado de la empresa multinacional. El modelo le permite a Nike penetrar mercados donde el riesgo económico o social (o ambos) harían dificultoso o imposible operar de forma normal sin una alta exposición. El socio (Nike Partner) se convierte en la representación de facto de la marca, actuando en nombre de esta, alineado al plan global, pero con administración y mano de obra local. 

A partir del año 2017 Northbay International implementa el nuevo departamento de DSM (siglas en inglés de Demand and Supply Management). La función de DSM es planificar debidamente la demanda del mercado de la manera más científica posible. Anteriormente a la creación del departamento de DSM, la mayoría de las oficinas de Nike dependían del departamento comercial o el de finanzas para determinar las metas de crecimiento. En el caso de Northbay, las metas eran negociadas con Nike WHQ de manera empírica. El departamento asume la responsabilidad de la planificación de la demanda desde ese punto en el tiempo, sirviendo de brazo analítico del departamento comercial. 

Como muchos departamentos incipientes de analíticas, este comenzó recaudando información del punto de ventas de los principales clientes, y analizando las operaciones en Excel. A partir del año 2019 era evidente que la cantidad de información hacía la recopilación de datos intensiva en mano de obra, y que muchos de los análisis no corrían bien en Excel. A partir del año 2021 comienza la construcción de un sistema automatizado de ingesta de los datos del punto de venta, la implementación de un data lake en la nube utilizando Microsoft Azure, y el uso de analíticas más robustas con Power BI. Dicho proyecto fue asignado a la empresa panameña ISSA, conocida por su trabajo en análisis predictivo en el sector bancario, pero con cero experiencia en el sector del retail. 

En la actualidad, los analistas del departamento siguen estimando la demanda usando las tasas de crecimiento naturales de los clientes, calculando la necesidad basada en los límites máximos de inventario esperados en el mercado y las posibles fechas y cantidades de reposición de producto que reporta la unidad de manufactura de la marca. 

El ciclo de GTM (por sus siglas en inglés Go To Market) es el que regula la periodicidad de lanzamiento de productos en la industria. La marca Nike opera con cuatro colecciones al año, espaciadas en períodos de tres meses llamados temporadas, que reflejan los cambios estacionales. Las cuatro temporadas son primavera, verano, otoño e invierno. La tendencia del ciclo se ve afectada por la época de fin de año, en la cual las ventas se disparan, y tiene un valle en la mitad del año. La estacionalidad de este ciclo puede verse afectada por movimientos económicos y la volatilidad típica de la región, sin embargo a lo largo de los años prevalece una curva más o menos similar a lo largo del tiempo. 

Northbay International sigue una estrategia de negocio similar a la de casa matriz, continuamente eliminando clientes y reduciendo la cartera de cuentas, maximizando el negocio y participación de los retailers más fuertes. El principal cliente en este sentido es Sportline América, una cadena nacida en Panamá que ha expandido sus puertas a más de ocho países, y es la mayor de su tipo en Latino América (no en puertas, pero sí en países en operación). Northbay International cuenta con un equipo comercial exclusivo para Sportline, dada la importancia del retailer. Las ventas en el punto de venta se monitorean semanalmente de manera que se conoce exactamente si se alcanzan o no los objetivos y metas, y cómo esto impacta en los niveles de inventario de cada una de las tiendas. 

Sportline America invirtió a partir del año 2018 en el paquete Analytical Ways, un potente software que corre encima del ERP SAP para el análisis y administración de la demanda. Lamentablemente dicho software nunca dió resultados satisfactorios. Sin un equipo de científicos de datos, o analistas de datos con experiencia, Sportline no le ha podido sacar provecho, y la decisión de la planificación de la demanda sigue en manos del equipo de compras, utilizando métodos más sencillos (principalmente limitados a estadística descriptiva). 

La solución propuesta por ISSA es un modelo basado en el uso de la librería Prophet, desarrollada por Facebook. Inicialmente la propuesta tuvo buena acogida porque acotaba el error de pronóstico notablemente. Pero la implementación del sistema se extendió de los seis meses programados a más de un año y medio, y los gerentes del departamento de DSM han manifestado una pérdida parcial en la confianza con ISSA, y serios cuestionamientos sobre la efectividad de la metodología de predicción, dada la cantidad de errores generados en la fase de data engineering. El equipo interno de Northbay tuvo que reescribir una gran cantidad de código SQL para lograr la migración e integración de los datos a Microsoft Azure, así como explicar el funcionamiento de los ciclos de GTM (go to market) a ISSA, al punto de cuestionar, quizás un poco tarde en el proceso, si realmente estaban calificados para el proyecto. 

Tanto a Northbay International y Sportline les interesaría apoyar el desarrollo de modelos predictivos de la demanda que no fueran cajas negras, donde hubiera visibilidad en las variables críticas que promueven el crecimiento, y que pudieran utilizarse de forma conjunta para maximizar la precisión de los pronósticos de compra. Northbay utilizará estos modelos como los nuevos estándares de predicción de aprendizaje automatizado, los cuales serían implementados a la par de la infraestructura actual en Azure. Sportline estudiaría el potencial de dichos modelos pero no los implementaría de facto, sino que los utilizaría como proof of concept para la construcción de un sistema más potente. 

Quizás lo más importante, además del interés mostrado por apoyar la investigación y trabajo, es la disposición de aportar grandes cantidades de datos para el mismo. Northbay International aportaría toda la data maestra de los productos, y Sportline una muestra de cerca de medio millón de puntos de datos de POS de su 90+ puertas distribuidas en 8 países de los últimos tres años de ventas.

## Objetivos del Proyecto
El objetivo del proyecto es el estudio y análisis de la data de POS de la marca Nike en las más de 90 puertas de las tiendas SLA, para la construcción de un modelo de predicción basado en técnicas de aprendizaje automatizado que reduzcan la incertidumbre de los pronósticos de venta y maximicen la precisión de los mismos en aras de reducir los niveles de inventario. 

Un objetivo secundario es la transparencia y explicabilidad de los modelos. Un problema que Sportline ha enfrentado es la falta de comprensión de los modelos de predicción caja negra (sea porque realmente son caja negra, como las redes neuronales, o porque el proveedor no da mayor detalle en las razones de las predicciones que arroja el sistema). 

## Resultados Esperados
El departamento de DSM está reportando diferencias en el orden del 10% al 27% entre el pronóstico al momento de preparar el plan y el momento de reportar los datos reales. Evidentemente el uso de heurísticas manuales está arrojando predicciones tan distantes de la realidad que no solo se ha perdido confianza en las mismas, sino que los compradores de Sportline han comenzado a utilizar ajustes arbitrarios a los pronósticos para no comprar producto de más que luego no rote. Esto está trayendo todo tipo de problemas a ambas empresas, con ejemplos bien distribuidos de:

* producto que no se vende, aumentando innecesariamente los índices de inventario en mano semanal,
* y producto que se vende muy bien pero no se puede reponer porque se pronosticó muy por debajo de la venta real. 

A través de un diseño de modelos de predicción basados en aprendizaje automatizado se espera reducir el margen de error por debajo del 10%. 

## Asignaturas y Módulos Relacionados con los Objetivos y Resultados
La propuesta de trabajo refleja perfectamente el quehacer de un equipo de científicos de datos en una empresa de venta al por mayor o minorista, que debe maximizar el potencial del negocio, y guarda una estrecha relación con múltiples materias impartidas en el máster. 

### Impacto y Valor del Big Data
Extraer conocimiento y poder tomar decisiones críticas de grandes volúmenes de datos es vital en el mundo del Big Data. Las empresas de venta al detal generan grandes volúmenes de datos de forma diaria, pero no siempre esta data se comparte con los proveedores para crear una alianza ganar-ganar, donde tanto el distribuidor mayorista como el minorista optimizan su pronóstico comercial y construyen planes de crecimiento alrededor de data concreta. Este modelo de generación de valor agregado compartido de data analytics puede resultar interesante para cualquier otro par de empresas que decidan construir un data ops pipeline compartido, donde ambos hagan uso extensivo, abierto, y común de la data, dividiendo los costos de mantenimiento de la infraestructura y explotando a su mejor ventaja los conocimientos adquiridos. 

### La Ciencia de Datos: Técnicas de Análisis, Minería y Visualización
La construcción de modelos predictivos estará apoyada en el análisis exploratorio de la data inicial. Solo la mente humana puede crear atributos (features) como regresores de la data que tengan sentido comercial y humano, y que permitan derivar del modelo cuáles son las variables críticas que impactan la demanda del consumidor. La materia es cuestión es la columna vertebral del trabajo final del máster, porque en sí, es la que mejor recoge la esencia del Business Analytics y la aplicación de la ciencia de datos en un entorno de negocio. 

### Estadística para Científicos de Datos
Sin haber hecho el análisis EDA inicial, es evidente que la data comercial tiene la clara forma de una serie de tiempo aditiva. El análisis de las series de tiempo involucra un claro entendimiento de la estadística descriptiva y la estadística inferencial. Todo lo aprendido en la materia se ampliará con textos especializados, sobre todo el libro “Forecasting: principles and practices” de Robert Hyndman y George Athanasoupulos. 

### Aprendizaje Automático
Todo lo aprendido en la materia de aprendizaje automático será ampliado en el trabajo final, combinando métodos muy específicos de machine learning al estudio de series de tiempo, el uso de métodos ensamblados como herramienta potencial para la mejora progresiva de pronósticos, y la aplicación de librerías de programación que automaticen la aplicación, ejecución, y comparación de diferentes algoritmos de modelos predictivos para escoger el mejor en cada caso. 

### El Big Data en la Empresa
De la materia en cuestión se utilizará la aplicación de métodos ágiles para administrar el desarrollo del trabajo final. Más precisamente, se utilizará la metodología SCRUM para determinar historias del usuario, dividir la tarea en épicas, crear una pila de producto, y definir una hoja de ruta de versiones con miras, si bien no a trabajar en todas, allanar el camino para un equipo futuro de científicos de datos. 

Esto es importante para Sportline, quien no implementará de lleno ninguno de los resultados del trabajo, sino que utilizará el mismo para la construcción de un sistema robusto pero que incluya otras necesidades (recordemos que Sportline maneja múltiples marcas como tienda al detal, y no conocemos el alcance y apoyo que reciba de estas en cuanto a metodologías de análisis y predicción). 

## Tecnologías y Herramientas Big Data
El sistema en creación de Northbay para su futura data ops pipeline utiliza Spark como motor para el análisis en un entorno distribuido de grandes cantidades de datos. No es claro al comienzo de este trabajo cuanto acceso se tendrá al data lake de Northbay, o si se trabajará con la data en crudo provista por Sportline. Lo ideal sería lo primero, pero esto restringe el aprendizaje de Sportline, quien no tiene acceso a la data procesada en el data lake en Azure y gestionada por Spark. 

Tampoco queda claro si la cantidad de datos (medio millón de registros) es una cantidad tan impresionante que los equipos modernos de computación no puedan manejar con facilidad. Sin embargo es interesante para Northbay poder contar con modelos fácilmente migrables a Spark en Azure, si quisiera en algún momento comparar, evaluar, o inclusive reemplazar el modelo diseñado por el proveedor ISSA. 

### Métodos, Materiales, y Tecnologías de Uso Potencial
El alumno cuenta con una serie de herramientas para elegir a su disposición, pero no ha decidido en la aplicación final de las mismas. Los siguientes son comentarios e ideas para evaluar con el tutor de TFM. 

### Metodología Scrum y Repositorios 
El alumno utilizará un repositorio Github para el manejo del código a utilizar, al cual puede tener acceso el profesor tutor para hacer comentarios, verificar la originalidad del trabajo, y hacer un seguimiento en tiempo real del progreso. 

El uso actual de Github con el cambio de clave a token SSH y GPG ha complicado (a criterio del alumno innecesariamente) el acceso a Github a través del CLI. Sin embargo se espera que el sistema funcione bien al momento de comenzar el TFM, sin cambios por parte de Github en cuanto a su funcionamiento. 

Adicionalmente, el alumno utilizará la funcionalidad de Github para registrar e implementar de manera digital el proceso SCRUM que administre el TFM. Los tableros de progreso se combinarán con la generación de páginas Wiki dentro de Github que registre todos los pasos, procesos, diccionarios de datos, y decisiones de diseño del TFM.

### Lenguajes de Programación
El alumno es fluido en R y Python, pero le gustaría estandarizar el TFM en uno solo para optimizar el tiempo y la especialización resultante del esfuerzo. 

También se ha analizado el uso de Julia y la excusa del TFM como razón para hacer una implementación utilizando dicho lenguaje (y afianzar el conocimiento de Julia en el camino). Se entiende que Julia no es parte del currículum oficial de la IMF/Universidad de Nebrija y que quizás no sea una opción para este caso. 

### Entornos de Programación
No se descarta el uso de IBM Watson como entorno de desarrollo de ciencia de datos. Su uso no solo permitiría el manejo de Python Notebooks en la nube, sino la utilización de DB2 como base de datos SQL, y templates de modelos de predicción pre-armados para acelerar la investigación. 

### Editor
El alumno propone utilizar LaTeX para la redacción del trabajo final del máster. 

### Juegos de Datos
El trabajo utiliza dos juegos de datos: 

1. Un juego de datos maestros del producto, con la descripción detallada de cada uno de los SKU en la base de datos de la empresa Northbay, representando cada uno de los modelos disponibles en los últimos cinco años en el mercado. Dicho juego de datos incluye alrededor de cinco mil puntos de datos, limitados a solamente calzado deportivo.  
2. Un juego de datos de transacciones, provistos por Sportline, detallando una muestra de medio millón de puntos de datos de ventas de las diferentes 90 puertas ubicadas en siete países, incluyendo información como precio de venta, día de venta, locación, ciudad, país, etc. Sportline trabajará con el alumno para asegurar que la muestra es robusta y muestreada de tal forma que no haya sesgo en la información y distribución de los datos (por ejemplo, si todos los años tienen la misma cantidad de puntos de datos, la muestra no cumpliría ningún objetivo). 

Adicionalmente:

Por motivos de seguridad, ninguna de las empresas otorgará acceso a las bases de datos, sino que se recibirá la información en un archivo plano para que el alumno haga todo el trabajo en un entorno de desarrollo totalmente desconectado de los sistemas.  
Sportline pudiera estar en condición de liberar no una muestra, sino la totalidad de datos de los últimos tres años de la marca Nike, lo que pudiera suponer un aumento drástico del volumen de la información. 

## Notas Adicionales
### La Crisis de la Pandemia
Los datos de POS de SLA incluyen el impacto de la crisis de la pandemia del Covid-19 en los diferentes países de la región. Algunos solo estuvieron cerrados por breves meses, como Colombia. Otros, como Panamá, vieron cierres estrictos por más de medio año. La caída en las ventas durante la pandemia, y el aumento del volumen de ventas tras ella, puede tener serias carencias al momento de entrenar los datos y resultar en modelos cuya precisión y grado error los haga obsoletos. 

El alumno piensa que es posible introducir en la construcción del modelo un aprendiz binario para identificar si en un país y mes en particular existía una condición de cierre por pandemia o no, y de esa forma entrenar correctamente el juego de datos para que el algoritmo de cada modelo interprete la condición especifica del volumen de ventas en un momento dado del tiempo. 

