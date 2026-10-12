# Projet IA à domicile — BTS SIO 2 SLAM

**Les consignes complètes** (sujets, exigences, déroulé du lundi et du mardi, barème) :
<https://ggaillard.github.io/portail-bts/distance/projet-ia.html>

Séances : 5, 6, 8 et 12 octobre 2026 (le projet), **13 octobre** (séance 24 : le même projet branché sur une IA en ligne, gratuite et sans carte bancaire). Questions et rendu : par e-mail, à l'adresse Gmail habituelle de l'enseignant, objet `[BTS2 Projet IA] NOM Prénom — …`.

## Démarrer en trois gestes

1. En haut de cette page : **Use this template → Create a new repository**, à votre nom, nommé `projet-ia-<prenom>`.
2. Clonez **votre** dépôt, puis `cp .env.example .env` (Windows : `copy .env.example .env`) et remplissez `.env`. Ce fichier ne se commite jamais.
3. Remplissez `README.md` au fil des séances : c'est votre dossier.

### Vous avez créé votre dépôt avant le 13 octobre ? Récupérer la séance 24

Dans votre dépôt, téléchargez les deux nouveaux fichiers, puis suivez la mission 3 de la séance 24 (trois changements dans `main.py`, une ligne dans le `Dockerfile`) :

```bash
curl -O https://raw.githubusercontent.com/ggaillard/BTS2-Projet-IA/main/fournisseurs.py
curl -O https://raw.githubusercontent.com/ggaillard/BTS2-Projet-IA/main/essai_fournisseur.py
```

| Fichier | Rôle |
|---|---|
| `main.py` | l'application FastAPI : page, `/api/demander`, `/sante`, `/a-propos`, code d'accès, limite de requêtes |
| `fournisseurs.py` | qui sert le modèle : Ollama sur votre PC, ou un fournisseur en ligne (OVHcloud, GitHub Models, Groq, Mistral, Google) — et où partent les données |
| `essai_fournisseur.py` | essayer un fournisseur sans lancer l'application |
| `prompt.txt` | la consigne donnée au modèle — à écrire pour votre sujet |
| `static/index.html` | la page — à adapter |
| `Dockerfile`, `compose.yaml` | la mise en production : l'application et le tunnel vers l'URL publique |
| `.env.example` | les réglages, à copier en `.env` |
| `evaluer.py`, `cas.json` | la mesure : rejouer vos cas et compter |
| `README.md` | votre dossier |
| `sujets/` | les six sujets détaillés, avec leurs données d'exemple — [commencez ici](sujets/) |

*Organisations et données des projets : fictives uniquement.*
