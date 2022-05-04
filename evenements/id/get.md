# Afficher les informations d'une fiche événement

Affiche les informations de la fiche événement dont l'identifiant est passé en paramètre.

**URL** : `/http.api/ezrest/evenements/:id`

**Paramètre** : `id=[integer]` où `id` est l'identifiant de la fiche événement.

**Method** : `GET`

**Authentification requise** : oui

## Retour

Exemple de retour accessible dans le bloc `donnees`.

```json
[{
	"id_evenement": "...",
	"titre": "...",
	"logo": "...",
	"descriptif": "...",
	"date_debut": "...",
	"date_fin": "...",
	"horaire": "...",
	"lieu": "...",
	"adresse": "...",
	"contact": "...",
	"tel": "...",
	"email": "...",
	"web": "...",
	"id_asso": "...",
	"nom_asso": "..."
}]
```
