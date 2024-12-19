#  Herramientsd utilizadas para el analizis 
## NLTK   
### esta herramienta se utilizo para el analizis de emocions de los textos para verificar la veracidad de dichos textos
```csharp
 from nltk.sentiment import SentimentIntensityAnalyzer

sia = SentimentIntensityAnalyzer()

 analizar
file_path = "C:\\Users\\zahid\\Documents\\reforma\\op1.txt"

try:
   
    with open(file_path, "r", encoding="utf-8") as file:
        text = file.read()
    
   
    sentiment_scores = sia.polarity_scores(text)
    
   
    print("Resultados del análisis de sentimiento:")
    print(sentiment_scores)

except FileNotFoundError:
    print(f"El archivo en la ruta '{file_path}' no fue encontrado.")
except Exception as e:
    print(f"Ocurrió un error: {e}")
```

##
## OLLAMA
### Esta herramienta se utilizo para hacer consultas sobre acontecimientos historicos en otros paises relacionadas con las reformas
```csharp
import ollama

Crear un cliente Ollama (sin pasar api_key directamente)
client = ollama.Client()

Enviar consulta
response = client.query("¿Cuáles son las ventajas del aprendizaje supervisado?")
print(response)
```
##
## gensim
```csharp
from gensim import corpora
from gensim.models import LdaModel

# Documentos de ejemplo
documents = [

]

# Preprocesar texto
texts = [[word for word in doc.lower().split()] for doc in documents]

# Crear diccionario y corpus
dictionary = corpora.Dictionary(texts)
corpus = [dictionary.doc2bow(text) for text in texts]

# Entrenar modelo LDA
lda = LdaModel(corpus, num_topics=2, id2word=dictionary, passes=10)

# Mostrar temas
print(lda.print_topics())
```


