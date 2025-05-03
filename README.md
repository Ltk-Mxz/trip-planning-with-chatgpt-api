# Trip Planning with ChatGPT API

Ce projet utilise l'API OpenAI pour créer un assistant conversationnel spécialisé dans la planification de voyages, en se concentrant sur les points d'intérêt touristiques à Paris.

## Fonctionnalités

- Fournit des informations sur les attractions touristiques à Paris.
- Répond à des questions spécifiques sur des lieux célèbres comme la Tour Eiffel, le Louvre et l'Arc de Triomphe.
- Maintient une conversation contextuelle en ajoutant chaque question et réponse dans un historique.

## Technologies utilisées

- **Langage** : Python
- **API** : OpenAI GPT-3.5 Turbo
- **Librairies** :
  - `os` : Pour accéder aux variables d'environnement.
  - `openai` : Pour interagir avec l'API OpenAI.

## Prérequis

- Python 3.7 ou supérieur.
- Une clé API OpenAI valide, enregistrée comme variable d'environnement `OPENAI`.

## Installation

1. Clonez ce dépôt :
   ```bash
   git clone https://github.com/Ltk-Mxz/trip-planning-with-chatgpt-api.git
   cd trip-planning-with-chatgpt-api
   ```
2. Installez les dépendances :

```bash
pip install openai
```

3. Configurez votre clé API OpenAI :

```bash
export OPENAI="votre_clé_api"
```

4. Utilisation
Lancez le script principal :

```bash
python main.py
```

Le script répondra automatiquement à une liste de questions prédéfinies sur des points d'intérêt touristiques à Paris, comme :

Quelle est la distance entre le Louvre et la Tour Eiffel ?
Où se trouve l'Arc de Triomphe ?
Quelles sont les œuvres incontournables au musée du Louvre ?
Les réponses sont affichées dans la console.

Fonctionnement du script
Initialisation de la conversation :
Le script commence par définir le rôle de l'assistant comme étant un guide de voyage concis pour Paris.
Boucle de questions :
Une liste de questions prédéfinies est ajoutée à la conversation.
Chaque question est envoyée à l'API OpenAI pour obtenir une réponse.
Les réponses sont imprimées et ajoutées à l'historique de la conversation pour maintenir le contexte.
Extrait de code
```Python
conversation = [
    {
        "role": "system",
        "content": "You are a travel guide designed to provide information about landmarks..."
    },
    ...
]

response = client.chat.completions.create(
    model="gpt-3.5-turbo",
    messages=conversation,
    temperature=0.0,
    max_tokens=100
)
```
