# Visualiseur des données de l'Observatoire de l'Open Data

Widget de prévisualisation des données issues de fichiers csv de l'Observatoire de l'Open Data - Open Data France.

---

## Résumé

Open Data France possède un site (https://www.observatoire-opendata.fr/) visant à mesurer le déploiement de l'open data en France, à sensibiliser les collectivitées et les acteurs publics à l'open data, et à valoriser ces données sous formes de diverses visualisations. Sont référencés sur ce site différents types de données : organisations, plateformes, etc...

Afin de pouvoir partager et de mettre en valeur toutes les ressources de ce jeu de données il a été proposé de créer un outil numérique de type "widget" : `Datami`. En effet un outil de ce type permet de pouvoir intégrer sur des sites tiers (sites de partenaires ou autres) une sélection plus ou moins large de ressources. Cette solution permet à la fois d'éviter aux sites partenaires de "copier-coller" les ressources, d'afficher sur ces sites tiers les ressources toujours à jour, et de permettre aux sites tiers ainsi qu'au site source de gagner en visibilité, en légitimité et en qualité d'information.

L'autre avantage de cette solution est qu'elle n'est déployée qu'une fois, mais que le widget peut être intégré et paramétré/personnalisé sur autant de sites tiers que l'on souhaite... gratuitement.

La solution proposée et réalisée ici s'appuie sur un projet open source porté par la coopérative numérique [**multi**](https://multi.coop) : le projet [Datami](https://datami.multi.coop).

---

## Démo

- Page html de démo : [![Netlify Status](https://api.netlify.com/api/v1/badges/ef33715e-c076-40e0-beaa-7479afe8a7d1/deploy-status)](https://app.netlify.com/sites/datami-demo-odf-data-ressources/deploys)
- Url de démo :
  - Données observatoire ODF : https://datami-demo-odf-data-ressources.netlify.app/

---

### Documentation

Un site dédié à la doucmentation technique de Datami est consultable ici : https://datami-docs.multi.coop

---

## Crédits

| | logo | url |
| :-: | :-: | :-: |
| **Open Data France** | ![ODF](./images/odf-logo.svg) | https://www.opendatafrance.net/ |
| **coopérative numérique multi** | ![multi](./images/multi-logo.png) | https://multi.coop |

---

## Pour aller plus loin

### Datami

Le widget fait partie intégrante du projet [Dataami](https://gitlab.com/multi-coop/datami)

---

## Mini server for local development

A mini server is writen in the `server.py` to serve this folder's files

To install the mini-server :

```sh
pip install --upgrade pip
python3 -m pip install --user virtualenv
python3 -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

or

```sh
sh setup.sh
source venv/bin/activate
```

### Run local server

To run the server on `http://localhost:8899`:

```sh
python server.py
```

or

```sh
sh run_server.sh
```

The html file `index.html` will be served on `http://localhost:8899`

Files will be locally served on :

- `http://localhost:8899/content/<path:folder_path>/<string:filename>`
- `http://localhost:8899/statics/<path:folder_path>/<string:filename>`
