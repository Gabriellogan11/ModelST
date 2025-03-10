Introducción 
La rotación de empleados es un fenómeno que afecta a empresas de diversos sectores y 
tamaños, generando impactos significativos en términos de productividad, costos de 
contratación y estabilidad organizacional. Cuando un empleado deja una empresa, la 
organización no solo pierde talento y experiencia, sino que también incurre en gastos 
adicionales relacionados con el reclutamiento y la formación de nuevos trabajadores. 
Además, la rotación constante puede afectar la moral de los empleados restantes, 
disminuyendo el compromiso y la satisfacción laboral. 
Dada la relevancia de este problema, la predicción de la rotación de empleados ha adquirido 
una gran importancia en la gestión de recursos humanos. La posibilidad de anticiparse a la 
deserción del personal permite a las empresas desarrollar estrategias efectivas para retener 
talento y mejorar el ambiente laboral. En este contexto, la inteligencia artificial se ha 
convertido en una herramienta poderosa para analizar grandes volúmenes de datos y detectar 
patrones que podrían pasar desapercibidos mediante métodos tradicionales. 
Este estudio tiene como objetivo desarrollar un modelo de predicción de la rotación de 
empleados utilizando técnicas de Machine Learning. A través del análisis de un conjunto de 
datos con información laboral y personal de los empleados, se busca identificar los factores 
más influyentes en la decisión de dejar la empresa. Se han evaluado tres modelos diferentes—
 Random Forest, Máquinas de Soporte Vectorial (SVM) y Redes Neuronales—con el 
propósito de determinar cuál ofrece el mejor desempeño en términos de precisión y capacidad 
de generalización. Con base en los resultados obtenidos, se pretende proporcionar 
recomendaciones que puedan ayudar a las empresas a reducir la rotación laboral y mejorar la 
gestión del talento humano. 
Metodología 
El desarrollo del proyecto siguió un enfoque estructurado que abarcó la recopilación, 
procesamiento y análisis de datos, así como la implementación y evaluación de modelos de 
Machine Learning. En primer lugar, se trabajó con un conjunto de datos que contenía 
información detallada sobre los empleados, incluyendo variables como salario, satisfacción 
laboral, edad, antigüedad en la empresa, entre otras. Dado que algunos de estos datos eran 
sensibles, se aplicó un proceso de cifrado para proteger la privacidad de los empleados. Una 
vez asegurada la confidencialidad de la información, se procedió con la limpieza y 
transformación de los datos, convirtiendo variables categóricas en valores numéricos y 
normalizando las características mediante StandardScaler para garantizar una mejor 
convergencia de los modelos. 
Una vez completado el preprocesamiento, se implementaron los modelos de Machine 
Learning para predecir la rotación de empleados. En primer lugar, se utilizó el modelo de 
Random Forest, un algoritmo basado en árboles de decisión que construye múltiples árboles 
y combina sus predicciones para mejorar la precisión y reducir el sobreajuste. Se configuró 
el modelo con 100 árboles de decisión y se ajustaron hiperparámetros clave, como la 
profundidad de los árboles y el número de características consideradas en cada división, con 
el objetivo de optimizar su rendimiento. La principal ventaja de Random Forest es su 
capacidad para manejar grandes volúmenes de datos y su interpretabilidad, ya que permite 
analizar la importancia de cada variable en la predicción de la rotación. 
En segundo lugar, se implementó un modelo de Máquinas de Soporte Vectorial (SVM), que 
utiliza un hiperplano óptimo para separar las clases de empleados que permanecen en la 
empresa y aquellos que la abandonan. Se optó por un kernel lineal, ya que proporciona un 
equilibrio entre interpretabilidad y eficiencia computacional. Además, se ajustó el parámetro 
de penalización C, que regula la tolerancia a errores de clasificación. Aunque SVM es eficaz 
en muchos escenarios, su desempeño puede verse afectado cuando los datos presentan 
relaciones no lineales complejas, lo que representa una de sus limitaciones más relevantes en 
este estudio. 
El tercer modelo desarrollado fue una Red Neuronal Multicapa (MLPClassifier), diseñada 
con dos capas ocultas de 64 y 32 neuronas, respectivamente. Se utilizó la función de 
activación ReLU para mejorar la capacidad de aprendizaje de la red y se implementó el 
algoritmo de optimización Adam, que ajusta dinámicamente la tasa de aprendizaje durante el 
entrenamiento. La red neuronal se entrenó con un máximo de 1000 iteraciones para garantizar 
una convergencia adecuada sin comprometer la eficiencia computacional. A diferencia de los 
otros modelos, la red neuronal es capaz de capturar relaciones no lineales en los datos, aunque 
su principal desventaja radica en la dificultad para interpretar los resultados y en el mayor 
tiempo de entrenamiento requerido. 
Para evaluar el desempeño de los modelos, se emplearon métricas estándar como la precisión 
(accuracy_score), el reporte de clasificación (classification_report) y la matriz de confusión 
(confusion_matrix). Adicionalmente, se realizaron visualizaciones de la frontera de decisión 
en 2D y 3D mediante reducción de dimensionalidad con PCA, lo que permitió analizar cómo 
los modelos clasificaban los datos y qué tan efectiva era la separación entre las clases. 
El proceso de modelado y evaluación se llevó a cabo con un enfoque iterativo, en el que se 
realizaron múltiples pruebas y ajustes en los hiperparámetros para optimizar el rendimiento 
de cada modelo. Además, se analizaron los resultados obtenidos en función del balance de 
clases en los datos, ya que una distribución desigual entre empleados que permanecen y 
empleados que abandonan la empresa podría influir en la precisión de las predicciones. Como 
parte de este análisis, se consideró la posibilidad de aplicar técnicas de balanceo de clases, 
como SMOTE, para mejorar la capacidad del modelo en la detección de empleados con alta 
probabilidad de rotación. 
La metodología aplicada en este proyecto abarcó desde la recopilación y procesamiento de 
datos hasta la implementación y evaluación de modelos de Machine Learning. A través de 
este enfoque riguroso y estructurado, se buscó garantizar la calidad del análisis y la validez 
de los resultados, con el objetivo final de desarrollar una herramienta predictiva que pueda 
ser utilizada en la toma de decisiones dentro de las empresas para mitigar el impacto de la 
rotación laboral. 
Resultados y Análisis  
El proceso de modelado se centró en la evaluación de tres algoritmos de clasificación—
 Random Forest, SVM y una Red Neuronal (MLPClassifier)—para predecir la rotación de 
empleados. Cada uno de estos modelos fue sometido a un riguroso proceso de entrenamiento 
y validación, permitiendo comparar sus métricas y entender cómo cada uno aborda el 
problema de clasificación. 
En primer lugar, es importante señalar que el análisis se realizó mediante diversas métricas: 
precisión (accuracy), sensibilidad (recall), precisión por clase (precision) y f1-score. A esto 
se sumaron las visualizaciones de la matriz de confusión y los gráficos de fronteras de 
decisión en 2D y 3D, obtenidos mediante Análisis de Componentes Principales (PCA), lo 
cual enriquece la evaluación de cada modelo al ofrecer una representación gráfica de cómo 
se separan las clases. 
El modelo de Random Forest se destacó desde el inicio, presentando una precisión global 
de aproximadamente 0.87. Este algoritmo, basado en la combinación de múltiples árboles de 
decisión, demostró ser muy robusto ante la variabilidad de los datos. El análisis de la matriz 
de confusión reveló un comportamiento equilibrado, en el que la clase “Yes” (empleados con 
rotación) alcanzó un f1-score cercano a 0.86, mientras que la clase “No” (empleados sin 
rotación) se situó alrededor de 0.88. Estos resultados no solo confirman la capacidad del 
modelo para minimizar tanto falsos positivos como falsos negativos, sino que también 
evidencian que las relaciones no lineales entre las variables se capturan de forma eficaz. La 
claridad de las fronteras de decisión en los gráficos de PCA respalda estos hallazgos, 
mostrando zonas bien definidas para cada clase y escaso solapamiento entre ellas. 
El análisis del SVM (Máquinas de Vectores de Soporte), que utiliza un kernel lineal, reveló 
una precisión de aproximadamente 0.85. Los reportes de clasificación indicaron un f1-score 
de alrededor de 0.83 para la clase “Yes” y 0.86 para la clase “No”. La fortaleza del SVM 
reside en su capacidad para definir un hiperplano óptimo que maximiza el margen de 
separación entre las clases. Sin embargo, la matriz de confusión evidenció algunas 
dificultades en la clasificación de casos marginales, donde la separación entre clases no es 
tan evidente. Los gráficos de fronteras de decisión mostraron zonas de solapamiento, lo cual 
sugiere que el modelo, a pesar de su rendimiento sólido en general, podría beneficiarse de 
ajustes adicionales en los hiperparámetros o de la exploración de otros kernels para mejorar 
la clasificación en las áreas límite. 
Por su parte, la Red Neuronal (MLPClassifier), con una arquitectura configurada en dos 
capas ocultas de 64 y 32 neuronas respectivamente, obtuvo una precisión de alrededor de 
0.84. El reporte de clasificación mostró un f1-score aproximado de 0.82 para la clase “Yes” 
y de 0.85 para la clase “No”. Estos valores indican que, si bien la red neuronal tiene la 
capacidad de capturar patrones complejos y no lineales en los datos, su desempeño resulta 
sensible a la configuración de los hiperparámetros, como la tasa de aprendizaje y el número 
de iteraciones. Los gráficos de fronteras de decisión en 2D y 3D evidenciaron que, en algunas 
áreas del espacio reducido mediante PCA, existen zonas de transición donde las regiones de 
decisión se traslapan. Esto sugiere la necesidad de una optimización más fina para mejorar 
la separación y, en consecuencia, la capacidad de la red para clasificar de forma más precisa 
los casos límite. 
Además de las métricas tradicionales, se hace relevante considerar otras herramientas de 
evaluación que, aunque no se implementaron en este estudio, podrían complementar el 
análisis. Por ejemplo, la curva ROC (Receiver Operating Characteristic) y el AUC (Area 
Under the Curve) ofrecen una perspectiva adicional para medir la capacidad de 
discriminación del modelo a diferentes umbrales de decisión. Asimismo, la evaluación del 
índice de Cohen’s Kappa permitiría cuantificar la concordancia entre las predicciones y la 
clasificación real, proporcionando otro ángulo desde el cual interpretar el desempeño del 
modelo. 
Finalmente, resulta esencial no solo evaluar la precisión predictiva, sino también considerar 
aspectos prácticos como el tiempo de entrenamiento y la estabilidad computacional. Mientras 
que Random Forest y SVM mostraron tiempos de entrenamiento razonables, la Red Neuronal 
requirió mayores recursos computacionales, lo que puede ser determinante en aplicaciones a 
gran escala o en entornos de tiempo real. 
En resumen, el análisis integral de las métricas y de las visualizaciones evidencia que los tres 
modelos presentan un desempeño competitivo, con f1-scores que oscilan entre 0.82 y 0.88. 
Random Forest se destaca por su robustez y capacidad para capturar relaciones complejas 
con un equilibrio notable entre ambas clases, mientras que el SVM ofrece una buena 
separación en escenarios de baja ambigüedad, a pesar de presentar algunas dificultades en 
los casos marginales. La Red Neuronal, por otro lado, muestra un gran potencial para modelar 
patrones complejos, aunque su eficacia depende en gran medida de una optimización 
detallada de sus hiperparámetros. 
Este enfoque multidimensional—que combina métricas cuantitativas y análisis visual—
 permite obtener una visión completa del comportamiento de cada modelo, facilitando la toma 
de decisiones en la selección y optimización de la solución de inteligencia artificial más 
adecuada para la predicción de la rotación de empleados. 
Conclusiones y Recomendaciones 
El análisis realizado demuestra que la integración de diversas técnicas de modelado permite 
abordar de manera efectiva la problemática de la rotación de empleados, ofreciendo 
soluciones robustas y adaptables a distintos escenarios empresariales. A partir de los 
resultados obtenidos, se pueden extraer las siguientes conclusiones: 
En primer lugar, el modelo de Random Forest se presenta como una opción confiable y 
robusta, especialmente en contextos donde la variabilidad de los datos y la presencia de 
interacciones complejas requieren de una solución que minimice el sobreajuste. Su capacidad 
para manejar datos ruidosos y su facilidad de interpretación lo convierten en una herramienta 
de gran utilidad para la toma de decisiones en recursos humanos. 
El modelo SVM, por su parte, destaca por su precisión en la separación de clases mediante 
la maximización del margen, lo que resulta particularmente útil cuando las fronteras entre las 
clases son definidas y se dispone de un conjunto de datos con menos ruido. No obstante, es 
importante considerar que su desempeño puede verse afectado en presencia de outliers o en 
escenarios donde la separación entre clases no es tan nítida. 
La Red Neuronal ofrece un enfoque altamente flexible y capaz de aprender patrones no 
lineales complejos, lo cual es crucial en entornos donde las interacciones entre variables no 
son triviales. Sin embargo, se requiere un proceso de ajuste minucioso de sus hiperparámetros 
para evitar problemas de convergencia y garantizar un rendimiento óptimo. Esta 
característica sugiere que, aunque la Red Neuronal posee un alto potencial, su 
implementación exitosa demanda recursos computacionales adicionales y una validación 
cruzada más exhaustiva. 
Con base en estos hallazgos, se proponen las siguientes recomendaciones: 
1. Optimización 
de 
Hiperparámetros: 
Es imperativo realizar una búsqueda sistemática de hiperparámetros, especialmente 
en el caso de la Red Neuronal, para identificar la configuración óptima que maximice 
la precisión sin comprometer la estabilidad del modelo. Técnicas como la búsqueda 
en cuadrícula o la optimización bayesiana pueden ser herramientas efectivas en este 
sentido. 
2. Ampliación 
y 
Enriquecimiento 
del 
Conjunto 
de 
Datos: 
Considerar la integración de variables adicionales y el uso de datos históricos más 
amplios podría mejorar significativamente la capacidad de generalización de los 
modelos. Un conjunto de datos más diverso ayudaría a capturar matices y variaciones 
que actualmente pueden estar subrepresentadas, fortaleciendo la robustez de las 
predicciones. 
3. Implementación 
de 
Validación 
Cruzada: 
Adoptar métodos de validación cruzada ayudaría a evaluar de manera más precisa la 
estabilidad y generalización de los modelos. Esta práctica reducirá el riesgo de 
sobreajuste y asegurará que las métricas obtenidas reflejen de forma fiable el 
comportamiento del modelo en datos no vistos. 
4. Monitoreo 
Continuo 
y 
Actualización 
Periódica: 
Dado el dinamismo del entorno empresarial, es recomendable establecer un proceso 
de monitoreo constante del desempeño de los modelos. La actualización periódica del 
pipeline, integrando nuevos datos y reajustando los parámetros de los modelos, 
garantizará que las predicciones sigan siendo relevantes y precisas a lo largo del 
tiempo. 
En conclusión, la evaluación de los modelos de IA implementados ofrece una perspectiva 
amplia y detallada sobre las capacidades y limitaciones de cada enfoque en la predicción de 
la rotación de empleados. La combinación de métodos tradicionales y avanzados permite 
desarrollar un sistema robusto y adaptable, cuya optimización continua y enriquecimiento de 
datos constituyen claves fundamentales para mejorar la toma de decisiones en la gestión del 
capital humano. Las recomendaciones expuestas buscan no solo perfeccionar el desempeño 
de los modelos, sino también fomentar un enfoque proactivo que se alinee con las 
necesidades dinámicas del entorno empresarial actual.
