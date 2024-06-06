# Producto Machine Learning (MVP) - Sistema de Recomendación de Restaurantes

Se desarrollò un sistema de recomendaciòn de  restaurantes que se basa en la comparaciòn de las reseñas de un usuario con las de los otros usuarios registrados en el sistema y, mediante tècnicas de Machine Learning, determina cuales son los usuarios con gustos más parecidos, y en base a esta similitud le recomienda uno (o mas restaurantes) de cualquier categorìa o de sòlo una categorìa especificada por el usuario

Ver el Sistema en Funcionamiento: [Sistema de Recomendación de Restaurantes](https://pfyelpml-upkwe29phjyawezvqffu6s.streamlit.app/)

Herramientas de desarrollo 

El algoritmo de recomendación se desarrolló en Python utilizando la biblioteca open-source de Machine Learning Scikit-learn, y principalmente hace uso de dos de sus funciones TfidfVectorizer y Cosine_similarity. Adicionalmente, se utilizaron las bibliotecas de Python NLTK/SentimentIntensityAnalyzer para el análisis de sentimientos de las reseñas y fuzzywuzzy para la homologaciòn de las categorías, y finalmente Streamlit para el desarrollo de la la interfaz web interactiva.

Scikit-learn 
TfidfVectorizer: se utilizó para el procesamiento de lenguaje natural (NLP) para transformar el texto de las reseñas en vectores nùmericos que fueron utilizadas en el algoritmo de similitud.
Cosine_similarity: se utilizó para calcular la similitud (mediante el algoritmo de la similitud del coseno) entre todos los vectores numéricos que representan las reseñas de los usuarios.
NLTK (Natural Language Toolkit)
SentimentIntensityAnalyzer: se utilizó para evaluar el tono emocional de las reseñas y obtener una puntuación de sentimiento que refleja la positividad, negatividad, neutralidad del sentimiento expresado en las reseñas.
Fuzzywuzzy: se utilizó para comparar las categorías de ambos set de datos, Google y Yelp, y obtener una puntuación de similitud que va del 0% al 100%, donde una puntuación del 100% indica que las cadenas son idénticas; esto se hizo para generar un listado reducido y estandarizado de categorías 
Streamlit: se utilizó para crear interfaz web interactiva que permite el ingreso de los datos y las selecciones de los usuarios y mostrar el resultado del sistema de recomendaciòn  


Datos de Entrada:
El sistema permite al usuario ingresar y seleccionar los siguientes paramètros para pedir la recomendación:
1. Identificador ùnico del usuario en la base de datos
2. El número de recomendaciones que desea - Disponible: de 1 al 10
3. El estado donde desea la recomendaciòn - Disponible: todos los estados de Estados Unidos 
4. La categoría de restaurantes en la que desea la recomendaciòn - Disponible: todas las categorías y la opción All (recomienda sin discriminar la categorìa)     

Datos de Salida:
1. Nombre(s) de restaurantes recomendados y para cada uno muestra:
La categoría del restaurante
Una reseña - imprime a manera de muestra la reseña que obtiene el mayor puntaje positivo obtenido con un algoritmo de anàlisis de sentimiento 
Rating - el puntaje otorgado al restaurante por el cliente que emitiò la reseña mostrada 
 

Caso de Uso
Valores de entrada:
cliente_id = '118267217160812717861'
número de recomendaciones: 3
estado: Florida
categoria: Italian restaurant

 
 
