# Utilise l'image officielle Python 3.7
FROM python:3.7-slim

# Définit le répertoire de travail à l'intérieur du conteneur
WORKDIR /app

# Copie le fichier requirements.txt dans le conteneur
COPY requirements.txt .

# Installe les dépendances listées dans requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copie tous les fichiers du répertoire local vers le répertoire de travail dans le conteneur
COPY . .

# Expose le port 8000 pour permettre d'accéder à l'application
EXPOSE 8000

# Démarre l'application FastAPI avec Uvicorn
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
