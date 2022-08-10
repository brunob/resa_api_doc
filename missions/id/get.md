# Afficher les informations d'une fiche mission

Affiche les informations de la fiche mission dont l'identifiant est passé en paramètre.

**URL** : `/http.api/ezrest/missions/:id`

**Paramètre** : `id=[integer]` où `id` est l'identifiant de la fiche mission.

**Method** : `GET`

**Authentification requise** : oui

## Retour

Exemple de retour accessible dans le bloc `donnees`.

```json
[{
	"id_mission": "...",
	"titre": "...",
	"logo": "...",
	"description": "...",
	"mission_horaires": "...",
	"mission_utile": "...",
	"mission_accessible": "...",
	"categorie": "...",
	"mission_type": "...",
	"commune": "...",
	"contact_referent": "...",
	"tel": "...",
	"email": "...",
	"id_asso": "...",
	"nom_asso": "...",
	"date": "..."
}]
```
