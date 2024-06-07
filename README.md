
# Producto Machine Learning (MVP) - Sistema de Recomendacion de Restaurantes

Se desarrollo un sistema de recomendacion de  restaurantes que se basa en la comparacion de las reseñas de un usuario con las de los otros usuarios registrados en el sistema y, mediante tecnicas de Machine Learning, determina cuales son los usuarios con gustos mas parecidos, y en base a esta similitud le recomienda uno (o mas restaurantes) de cualquier categoria o de solo una categoria especificada por el usuario

Ver el Sistema en Funcionamiento: [Sistema de Recomendación de Restaurantes](https://pfyelpml-upkwe29phjyawezvqffu6s.streamlit.app/)

## Herramientas de desarrollo 

El algoritmo de recomendacion se desarrollo en Python utilizando la biblioteca open-source de Machine Learning Scikit-learn, y principalmente hace uso de dos de sus funciones TfidfVectorizer y Cosine_similarity. Adicionalmente, se utilizaron las bibliotecas de Python NLTK/SentimentIntensityAnalyzer para el analisis de sentimientos de las reseñas y fuzzywuzzy para la homologacion de las categorias, y finalmente Streamlit para el desarrollo de la la interfaz web interactiva.
