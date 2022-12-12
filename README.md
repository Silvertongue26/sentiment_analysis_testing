
<br />
<div align="center">
  <h3 align="center">Comparativos de métodos para el análisis de sentimientos en twitter </h3>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Contenido</summary>
  <ol>
    <li><a href="#intro">Introducción</a></li>
    <li><a href="#pre">Preprocesamiento y EDA</a></li>
    <li><a href="#lstm">Redes LSTM</a></li>
    <li><a href="#svc">Linear SVC</a></li>
    <li><a href="#robertuito">Robertuito</a></li>
    <li><a href="#textblob">TextBlob</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## Sobre el proyecto
<span id="#intro">
En este cuaderno se estarán probando diversos métodos para el análisis de sentimientos, para determinar el método que se estaría implementando en el proyecto de tesis para el análisis de sentimientos de los tweets.

 
<br><b>Se estarán probando 4 casos diferentes:</b>
1. Redes LSTM
2. Linear SVC
3. Robertuito
4. TextBlob<br><br>

<b>Consideraciones a tomar:</b><br>
   <i>Se es consiente que el dataset utilizado es un dataset pequeño debido a que se obtuvo de la página que posee datasets con enfoque político: http://tass.sepln.org/ , y se quiso utilizar algo con mayor enfoque a lo que se estaría manejando</i><br><br> 
   <i>La dimensión influye en los resultados, así como la región del español que se habla</i><br><br> 
   <i>Todavía hace falta métodos de preprocesamiento de la información para poder mejorar los resultados y en reunión con la maestra Olivia Gutu, se están viendo estos métodos.</i><br><br> 
   <i>No todos los métodos van a ser utilizados y en su mayoría solo se deben considerar como casos de prueba</i><br><br> 
   <i>Se están revisando factores y opciones para mejorar los resultados de algunos casos</i><br><br> 
   <i>El etiquetado de los tweets fue a criterio de la institución TASS y no siempre concuerdo con ellos.</i><br><br> 


## Preprocesamiento y EDA
<span id="#pre">
En esta sección se implementarán diversos métodos para la limpieza de la información para poder realizar un EDA básico a los datos, obtener un wordcloud para las diferentes polaridades y poder obtener las distribuciones así como una conclusión interesante.<br><br>

<i><b>Observaciónes:</b> En la sección de gráficos se pueden observar un fenómeno curioso pero lógico. En la distribución positiva, los tweets están compuestos de un menor número de palabras, en al neutral se encuentra bastante orientado al centro y en los tweets negativos la distribución se inclina a la derecha, mostrando así que este tipo de tweets tienden a tener más palabras, lo que determina que alguien enojado... Tiene más que decir.</i>

## Redes LSTM
<span id="#lstm">
Este caso vamos a estar creando una red LSTM, tomando en cuenta que todavía se requieren diversos ajustes, así como un corpus más robusto, de enfoque político en español y de mayor cantidad para poder obtener mejores resultados. <br><br>

<b>Nota:</b> Este no es el modelo seleccionado para implementar en la plataforma, hasta que se optimice y en su caso pueda arrojar mejores resultados que robertuito

<b>Conclusión:</b> Los parámetros faltan de ajustarse a su forma óptima, la red muestra que estaba mejorando poco a poco, sin embargo, es un factor determinante el tener un dataset más grande y balanceado, reitero este dataset se agarró como prueba sin intención de usarse para entrenar el modelo final.


## Linear SVC
<span id="#svc">
Este caso manejan los SVC lineares, sin embargo, presenta la misma situación que el model anterior al tener un dataset limitado. Asimismo, la publicación original carece de muchas justificaciones para el uso de ciertas técnicas, por lo cual este caso se debe tomar como un caso de experimentación más para aprender y de curiosidad, que cualquier otro motivo.<br><br>

<b>Conclusión:</b> Este modelo no responde de manera tan negativa sin embargo al faltar mucha documentación sobre el tema y ser solo para clasificar entre negativo y positivo, limita mucho la intención del proyecto, por lo cual no se considera para modelo final.



## Robertuito
<span id="#robertuito">
<b>Conclusión:</b> Muy probablemente este modelo vaya a ser el que se seleccione, debido a su precisión y curiosamente concuerdo más con la clasificación que el modelo asigna, que el mismo que algunas etiquetas del dataset original contiene.<br><br> 

<b>Nota:</b> A futuro ver la posibilidad de realizar transfer learning.

## TextBlob
<span id="#textblob">
<b>Conclusión:</b> Al ser un sistema por bolsa de palabras, no se considera como modelo final y presenta una precisión baja, pues no toma en contexto el resto del sentido del tweet.


