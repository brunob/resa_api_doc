# API RESA

Documentation pour l'usage de l'API du site [RESA](https://www.annuaire-associations.net/)

## Format de réponse

Chaque requête renvoie une réponse formatée comme l'exemple ci-dessous.

Seuls les blocs `erreur` et `donnees` vous seront utiles.

Le bloc `erreur` permet d'identifier :
* `status` : le code standard de la réponse HTTP
* `element` : libellé de l’élément concerné par l’erreur
* `valeur` : valeur de l’élément provoquant l’erreur 
* `titre` : texte explicatif court de l'erreur
* `detail`: texte complémentaire fournissant des détails sur l’erreur
ou sa résolution.

Le bloc `donnees` contient les données renvoyées par l'API si aucune erreur n'a été levée, c'est ça qui vous intéresse ;)

```json
{
	"fournisseur": {
		"plugin": "RESA",
		"version": "1.0.0",
		"schema": "0.0.1"
	},
	"requete": {
		"methode": "GET",
		"format": "ezrest",
		"collection": "...",
		"ressource": "...",
		"filtres": {
			"key": "XXXX"
		},
		"format_contenu": "json"
	},
	"erreur": {
		"status": 200,
		"type": "ok",
		"element": "",
		"valeur": "",
		"titre": "...",
		"detail": "..."
	},
	"donnees": [{}]
}
```


## Endpoints disponibles

* tous les endpoints nécessitent de passer une clé d'autorisation dans le paramètre `key` afin d'accéder à leur données
* tous les endpoints utilisent la méthode GET

Pour récupérer une clé personnelle, contactez le [RESAM](https://www.resam.net/)

### Associations

Endpoint pour récupérer les informations des fiches association.

* [Liste des associations](assos/get.md) : `GET /http.api/ezrest/assos/`
* [Informations d'une association](assos/id/get.md) : `GET /http.api/ezrest/assos/:id`

### Matériels

Endpoint pour récupérer les informations des fiches matériel.

* [Liste des fiches](materiels/get.md) : `GET /http.api/ezrest/materiels/`
* [Informations d'une fiche](materiels/id/get.md) : `GET /http.api/ezrest/materiels/:id`

### Missions

Endpoint pour récupérer les informations des fiches mission.

* [Liste des fiches](missions/get.md) : `GET /http.api/ezrest/missions/`
* [Informations d'une fiche](missions/id/get.md) : `GET /http.api/ezrest/missions/:id`

### Catégories

Endpoint pour récupérer les catégories de classement des différents types de fiches.

* **URL** : `/http.api/ezrest/catégories/`
* **Paramètre** : `id_groupe`
  * `1` : catégories des fiches association
  * `2` : catégories des fiches matériel
  * `3` : catégories des fiches mission

**Exemple de contenu**

```json
"donnees": {
    "1": "Association caritative et humanitaire",
    "2": "Art, culture et science",
    "3": "Environnement, patrimoine et histoire"
}
```

### GIS (cartographie)

Endpoint pour récupérer la liste des coordonnées des communes avec le nombre total d'associations liées à chacune d'entre elles.


* **URL** : `/http.api/ezrest/gis/`
* **Paramètre** : `id_secteur`
  * `1` : pour l'antenne du RESAM

**Exemple de contenu**

```json
"donnees": [{
	"lon": "-4.113333225250",
	"lat": "48.530834197998",
	"id_commune": "8748",
	"nom": "Bodilis",
	"count": "26"
}]
```

### Événements (agenda)

Endpoint pour récupérer les informations des événements de l'agenda.

* [Liste des événéments](evenements/get.md) : `GET /http.api/ezrest/evenements/`
* [Informations d'un événement](evenements/id/get.md) : `GET /http.api/ezrest/evenements/:id`
