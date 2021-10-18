# Afficher les informations d'une fiche association

Affiche les informations de la fiche association dont l'identifiant est passé en paramètre.

**URL** : `/http.api/ezrest/assos/:id`

**Paramètre** : `id=[integer]` où `id` est l'identifiant de la fiche association.

**Method** : `GET`

**Authentification requise** : oui

## Retour

Exemple de retour accessible dans le bloc `donnees`.

```json
[{
	"id_asso": "...",
	"titre": "...",
	"categorie": "...",
	"commune": "...",
	"email": "...",
	"tel1": "...",
	"tel2": "...",
	"web": "...",
	"facebook": "...",
	"twitter": "...",
	"mastodon": "...",
	"instagram": "...",
	"objet": ".",
	"description": "...",
	"adresse": "...",
	"rna": "...",
	"siret": "...",
	"presidents": "...",
	"nb_adherents": "...",
	"nb_salaries": "...",
	"antennes": "...",
	"contact1": "...",
	"contact1_tel": "...",
	"contact1_email": "...",
	"contact2": "...",
	"contact2_tel": "...",
	"contact2_email": "...",
	"lon": "...",
	"lat": "...",
	"date_modif": "..."
}]
```
