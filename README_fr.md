# Magasin d'applications pour Cosmos

Ce repo est un magasin d'applications pour Cosmos lié a mes besoins.

# Comment l'utiliser

Forkez ce repo, puis configurez le fichier config.json avec vos propres données. Ceci utilise les actions github et les pages github pour déployer le site web. Assurez-vous que ces actions et pages sont activées dans votre dépôt. Les deux URLs dans la configuration sont des URLs vers vos pages Github.

Vous pouvez ajouter votre propre application dans le dossier, soit en utilisant les fichiers cosmos-compose.json, soit les fichiers docker-compose.yml.

Par exemple, ce repo est `https://github.com/McFlyPartagesr/mcfly-cosmos-marketplace` mais les pages sont sous `https://McFlyPartages.github.io/mcfly-cosmos-marketplace`. Afin d'ajouter ce repo à Cosmos, vous devez ajouter `https://McFlyPartages.github.io/mcfly-cosmos-marketplace/servapps.json` à la liste des sources dans les paramètres de Cosmos.

