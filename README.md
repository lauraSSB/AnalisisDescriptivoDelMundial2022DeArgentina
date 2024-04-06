# Analisis Descriptivo Del Mundial 2022 De Argentina

Este trabajo se basa en responder la siguiente pregunta: ¿cómo se dieron los 
partidos de Argentina (el campeón) en el mundial de Qatar?

Para responder a esta duda vamos a recurrir a dos fuentes de datos bastante 
importantes y completas. La primera de ellas, la página de internet *Fbref*, la cual nos 
brinda estadísticas e información de los partidos de las ligas y competiciones más 
importantes del mundo. En este caso, utilizamos la sección del mundial de Qatar 
2022, más específicamente los partidos de Argentina 
(https://fbref.com/es/comps/1/Estadisticas-de-World-Cup), y se extrajo manualmente 
información sobre los partidos jugados, las estadísticas de los jugadores en cada uno 
de ellos, estadísticas grupales de Argentina y sus respectivos contrincantes, y se 
guardaron las bases en libros de Excel de manera independiente. 
Por otro lado, se utilizó la librería de Python statsbomb para obtener datos 
específicos sobre los eventos del partido, las alineaciones, la competencia, y los 
jugadores. En el siguiente link se puede observar la documentación de las bases de 
datos, las cuales se encuentran en formato json: 
https://github.com/statsbomb/statsbombpy/tree/master/doc.

Para realizar el análisis descriptivo se realizaron todas las visualizaciones desde un notebook de Google Colab, el cual 
se dividió en 6 secciones: 
    1. **Goles Esperados:** desde la base de datos de Fbref de cada partido se tomaron los 
    datos de los goles esperados a anotar y los goles esperados a recibir. Existe un 
    dataset alimentado desde esta página, y se realizaron 3 diagramas de línea para 
    comparar los goles anotados con los goles esperados a anotar, los goles recibidos 
    con los goles esperados a recibir y los goles esperados a anotar y a recibir.
    2. **Análisis de goles y asistencias:** desde Fbref se realizó una base de datos donde se 
    encontraron distintas estadísticas e información de cada jugador en todos los partidos 
    del mundial. Los gráficos utilizados fueron tablas de calor, donde se puede concluir 
    quien fue el goleador, el jugador con más asistencias, y los jugadores con más y 
    menos minutos en todo el torneo.
    3. **Análisis de bloqueos e intercepciones:** con el dataset utilizado en el punto anterior, 
    se hizo un análisis cuantitativo que incluye el número de bloqueos e intercepciones 
    por jugador, así como un gráfico de barras que modelaba la cantidad de pases 
    completados y fallados por jugador. 
    4. **Análisis de los pases durante el partido:** con un dataset proporcionado por fbref 
    que nos indicaba la cantidad de pases por jugador y que cantidad hizo cada uno por 
    sector. En este caso, existen 5 sectores. El tercio defensivo, medio y atacante, y la 
    zona del penal de defensa y de ataque. Se realizó un diagrama de waffle que nos 
    muestra los 9 jugadores con más pases durante todo el partido, y una proporción de 
    cuantos pases hizo en cuales zonas. 
    5. **Análisis de los eventos de pases durante el partido:** con la librería Statsbomb se 
    extrajeron los eventos durante el partido. Se filtraron esos eventos por pases de parte 
    de ambos equipos, y según la posición del jugador se dividieron estos pases. Se hizo 
    un contraste entre ambos equipos para los arqueros, defensas, mediocampistas y 
    delantero. El inicio del pase se representa con un círculo, mientras que su trayectoria 
    es representada por líneas. 
    6. **Mapa de tiros al arco (mapa de calor):** con la librería Statsbomb se extrajeron los 
    eventos durante el partido y se filtraron por tiros de parte de ambos equipos. Se realizó 
    un mapa de ‘calor’ en donde se indica en qué ubicación de la cancha se hizo el tiro, 
    el tamaño del círculo representa la probabilidad de que sea gol (entre más chiquito, 
    menos probabilidad), y los círculos rojos representan los tiros que terminaron dentro 
    de la portería.
