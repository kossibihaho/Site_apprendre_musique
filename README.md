# 🎵 Site « Apprendre la musique » : déploiement avec Docker

Site web statique (HTML / CSS / JavaScript) **conteneurisé avec Docker et orchestré avec Docker Compose**, puis déployé sur une instance **AWS EC2**. Le projet met en pratique la chaîne complète : conteneurisation, exécution reproductible, versionnement avec Git/GitHub et mise en ligne sur le cloud.

## 🎯 Objectifs

- Conteneuriser un site web pour qu'il s'exécute de la même façon partout
- Décrire l'environnement d'exécution sous forme de code (`Dockerfile`, `docker-compose.yml`)
- Déployer l'application sur une instance AWS EC2
- Documenter la démarche pour qu'elle soit reproductible

## 🛠️ Technologies

`Docker` `Docker Compose` `HTML5` `CSS3` `JavaScript` `AWS EC2` `Git` `GitHub`

## 📁 Structure du projet

```
Site_apprendre_musique/
├── Dockerfile                        # Image du site
├── docker-compose.yml                # Orchestration du conteneur
├── index.html                        # Page principale
├── templatemo-606-string-master.css  # Feuille de style
├── templatemo-606-string-scripts.js  # Scripts du site
├── images/                           # Ressources visuelles
└── Projet_Docker.pdf                 # Documentation détaillée du projet
```

## 🚀 Lancer le projet en local

**Prérequis :** Docker et Docker Compose installés.

```bash
# 1. Cloner le dépôt
git clone https://github.com/kossibihaho/Site_apprendre_musique.git
cd Site_apprendre_musique

# 2. Construire l'image et démarrer le conteneur
docker compose up -d --build

# 3. Vérifier que le conteneur tourne
docker compose ps
```

Le site est ensuite accessible dans le navigateur, sur le port publié dans le fichier `docker-compose.yml`.

Pour arrêter et supprimer le conteneur :

```bash
docker compose down
```

## ☁️ Déploiement sur AWS EC2

1. Lancer une instance EC2 (Linux) et ouvrir dans le groupe de sécurité le port utilisé par le site
2. Se connecter en SSH et installer Docker et Docker Compose
3. Cloner le dépôt sur l'instance
4. Exécuter `docker compose up -d --build`
5. Accéder au site via l'adresse IP publique de l'instance

## 📄 Documentation complète

La démarche détaillée du projet est disponible dans [`Projet_Docker.pdf`](./Projet_Docker.pdf).

## 🙏 Crédits

Le design du site s'appuie sur le template gratuit **TemplateMo 606 String**, de [templatemo.com](https://templatemo.com). L'objectif de ce projet n'est pas le développement web, mais la **conteneurisation et le déploiement**.

## 👤 Auteur

**Kossi BIHAHO**, élève ingénieur en Réseaux, Systèmes et Services Programmables (ENSA Marrakech)
🔗 [GitHub](https://github.com/kossibihaho) · 📩 bihahokossi@gmail.com
