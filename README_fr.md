# Magasin d'applications pour Cosmos

Ce repo est un magasin d'applications pour Cosmos lié a mes besoins.

# Comment l'utiliser

Forkez ce repo, puis configurez le fichier config.json avec vos propres données. Ceci utilise les actions github et les pages github pour déployer le site web. Assurez-vous que ces actions et pages sont activées dans votre dépôt. Les deux URLs dans la configuration sont des URLs vers vos pages Github.

Vous pouvez ajouter votre propre application dans le dossier, soit en utilisant les fichiers cosmos-compose.json, soit les fichiers docker-compose.yml.

Par exemple, ce repo est `https://github.com/McFlyPartagesr/mcfly-cosmos-marketplace` mais les pages sont sous `https://McFlyPartages.github.io/mcfly-cosmos-marketplace`. Afin d'ajouter ce repo à Cosmos, vous devez ajouter `https://McFlyPartages.github.io/mcfly-cosmos-marketplace/servapps.json` à la liste des sources dans les paramètres de Cosmos.


## Liste des applications

Shynet :

`"ALLOWED_HOSTS=example.com",` A adpater a votre url menant a Shynet ou tester avec `*.example.com` 
`"CSRF_TRUSTED_ORIGINS=https://shynet.mcflypartages.fr",` Mettre l'URL d'acces a votre Shynet
`DJANGO_SECRET_KEY` est a generer apres le lancement du conteneur SEULEMENT si vous compter gerer des compte via DJANGO. Pour generer le code lancer la commande `python3 -c "import secrets; print(secrets.token_urlsafe())"` depuis l'interieur du conteneur ou depuis la machine avec le code suivant `docker exec -it shynet_main python3 -c "import secrets; print(secrets.token_urlsafe())"`

Creation du compte admin au lancement. Soit depuis le conteneur via la comman,de `./manage.py registeradmin <your email>` ou alors depuis la machine avec la commande suivante `docker exec -it shynet_main ./manage.py registeradmin <your email>`


