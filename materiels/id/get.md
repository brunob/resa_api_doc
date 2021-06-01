# Afficher les informations d'une fiche matériel

Affiche les informations de la fiche matériel dont l'identifiant est passé en paramètre.

**URL** : `/http.api/ezrest/materiels/:id`

**Paramètre** : `id=[integer]` où `id` est l'identifiant de la fiche matériel.

**Method** : `GET`

**Authentification requise** : oui

## Retour

Exemple de retour accessible dans le bloc `donnees`.

```json
[{
	"id_materiel": "...",
	"titre": "...",
	"description": "...",
	"categorie": "...",
	"materiel_quantite": "...",
	"materiel_conditions": "...",
	"materiel_conditions_detail": "...",
	"commune": "...",
	"contact_referent": "...",
	"tel": "...",
	"email": "...",
	"id_asso": "...",
	"nom_asso": "..."
}]
```
